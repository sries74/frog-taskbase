# Bug Killa - Task List

**Agent:** Bug Killa (QA/Testing)  
**Role:** Quality Assurance, Test Architect  
**Current Focus:** FROG Phase 1 Testing  
**Status:** READY TO START

---

## Active Tasks

### FROG Phase 1 - QA & Testing

#### TASK 1: Database Validation [WEEK 1]
- **Project:** [[../Projects/FROG/Phase 1 Tasks]]
- **Developer:** Logic G (creates DB) → You (validate)
- **Status:** BLOCKED until DB created
- **Est. Hours:** 2-3 hours

**Checklist:**
- [ ] Database connects without errors
- [ ] All 14 tables exist with correct schema
- [ ] Seed data populated (4 users, 7 agents, 42 tasks)
- [ ] Foreign key constraints working
- [ ] Database backup is valid

**Validation Queries:**
```sql
SELECT COUNT(*) FROM users;        -- Should be 4
SELECT COUNT(*) FROM agents;       -- Should be 7
SELECT COUNT(*) FROM tasks;        -- Should be 42
SELECT * FROM information_schema.tables WHERE table_schema='public';
```

---

#### TASK 2: Auth System Tests [WEEK 1]
- **Project:** [[../Projects/FROG/Phase 1 Tasks#TASK 3 Auth System]]
- **Developer:** Logic G (code) → You (tests)
- **Subtask:** 3.5 Testing Auth
- **Status:** READY
- **Est. Hours:** 8-10 hours

**Checklist:**
- [ ] SUBTASK 3.5.1: Unit Tests
  - [ ] hashPassword() returns different hashes for same input
  - [ ] comparePassword() validates correctly
  - [ ] generateTokens() creates valid JWT
  - [ ] verifyToken() validates signature
  - [ ] registerUser() rejects duplicate emails
  - [ ] loginUser() rejects invalid passwords
  - Coverage target: 95%+
  
- [ ] SUBTASK 3.5.2: Integration Tests
  - [ ] POST /api/auth/register (success + duplicate)
  - [ ] POST /api/auth/login (success + wrong password)
  - [ ] POST /api/auth/refresh (valid + expired token)
  - [ ] POST /api/auth/logout (clears session)
  - [ ] Protected route with/without token
  - Coverage target: 90%+
  
- [ ] SUBTASK 3.5.3: Postman Collection
  - [ ] Create `FROG_Auth.json`
  - [ ] Include examples for all 4 endpoints
  - [ ] Pre/post scripts for token chaining
  - [ ] Document expected responses
  - [ ] Cleanup scripts (reset DB)

**Test Command:**
```bash
npm run test -- --coverage
# Target: 85%+ overall
```

---

#### TASK 3: API Endpoint Validation [WEEK 1]
- **Project:** [[../Projects/FROG/Phase 1 Tasks]]
- **Developer:** Logic G (endpoints) → You (validate)
- **Status:** READY (after TASK 2)
- **Est. Hours:** 4-5 hours

**Checklist:**
- [ ] GET /health returns { status: "ok" }
- [ ] POST /api/auth/register validates input
  - [ ] Email format required
  - [ ] Password strength (min 8 chars)
  - [ ] Name required
  - [ ] Returns user + tokens
  - [ ] 400 on duplicate email
  
- [ ] POST /api/auth/login
  - [ ] Returns 401 on invalid credentials
  - [ ] Returns user + tokens on success
  - [ ] Rate limiting active (5 attempts/min)
  
- [ ] POST /api/auth/refresh
  - [ ] Returns 401 on invalid token
  - [ ] Returns new access token on valid refresh token
  
- [ ] POST /api/auth/logout
  - [ ] Invalidates session
  - [ ] Returns 204 No Content

**Test Script:**
```bash
#!/bin/bash
# Full auth flow validation
curl -X POST http://localhost:3000/api/auth/register ...
curl -X POST http://localhost:3000/api/auth/login ...
curl -H "Authorization: Bearer $TOKEN" http://localhost:3000/api/users/me
```

---

#### TASK 4: Coverage Report [WEEK 1]
- **Project:** [[../Projects/FROG/Phase 1 Tasks]]
- **Status:** READY (after tests pass)
- **Est. Hours:** 1-2 hours

**Checklist:**
- [ ] Generate coverage report: `npm run test:coverage`
- [ ] Create `coverage/COVERAGE_REPORT.md`
  - [ ] Unit test coverage %
  - [ ] Integration test coverage %
  - [ ] Overall coverage (target: 85%+)
  - [ ] List uncovered lines (if any)
  - [ ] Recommend next tests
- [ ] Verify no console.errors/warnings in logs
- [ ] Document any known issues

---

## Testing Standards

**All code must have:**
- ✅ Unit tests (happy path + error cases)
- ✅ Integration tests (API endpoints)
- ✅ Error handling tests (400, 401, 500)
- ✅ Input validation tests
- ✅ 85%+ coverage (target for FROG)

**Test Command:**
```bash
npm run test -- --coverage --watch
```

---

## Blockers to Resolve

- [ ] Testing framework ready? (Jest/Mocha?)
- [ ] Test database separate from dev?
- [ ] Redis available for session tests?

---

## Code Review Checklist

Before approving any PR from Logic G:
- [ ] All tests pass locally
- [ ] Coverage >= 85%
- [ ] No hardcoded secrets
- [ ] Error messages are helpful
- [ ] Logging is at appropriate levels
- [ ] TypeScript strict mode happy
- [ ] Commit messages are clear

---

## Next Phase

After Phase 1 testing complete: Core APIs testing (Week 2)

---

## Linked

- Master: [[../Master Task List]]
- Project: [[../Projects/FROG/Phase 1 Tasks]]
- Dev Partner: [[Logic G Tasks]]
