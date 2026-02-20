# Logic G - Task List

**Agent:** Logic G (Backend/Systems/API)  
**Role:** Backend Developer, Architecture Specialist  
**Current Focus:** FROG Phase 1 Backend  
**Status:** READY TO START

---

## Active Tasks

### FROG Phase 1 - Backend Development

#### TASK 1: Database Setup [WEEK 1]
- **Project:** [[../Projects/FROG/Phase 1 Tasks#TASK 1 Database Setup]]
- **Subtasks:** 4 (1.1, 1.2, 1.3, 1.4)
- **Duration:** 2 days (Mon-Tue)
- **Status:** READY
- **Est. Hours:** 8-10 hours

**Checklist:**
- [ ] Subtask 1.1: PostgreSQL + PgBouncer setup
- [ ] Subtask 1.2: Prisma schema creation
- [ ] Subtask 1.3: Migrations & seeding
- [ ] Subtask 1.4: Backup & validation

**Deliverables:**
- PostgreSQL database with 14 tables
- 4 users, 7 agents, 42 test tasks seeded
- Database backup file
- Connection string documented

---

#### TASK 2: Backend Scaffold [WEEK 1]
- **Project:** [[../Projects/FROG/Phase 1 Tasks#TASK 2 Backend Scaffold]]
- **Subtasks:** 4 (2.1, 2.2, 2.3, 2.4)
- **Duration:** 1.5 days (Tue-Wed)
- **Status:** READY
- **Est. Hours:** 6-8 hours

**Checklist:**
- [ ] Subtask 2.1: Express + TypeScript project init
- [ ] Subtask 2.2: Project structure & .env
- [ ] Subtask 2.3: Config (logging, CORS, rate limit)
- [ ] Subtask 2.4: /health endpoint check

**Deliverables:**
- Express server running on :3000
- /health endpoint responsive
- Proper project structure
- Environment config template

---

#### TASK 3: Auth System [WEEK 1]
- **Project:** [[../Projects/FROG/Phase 1 Tasks#TASK 3 Auth System]]
- **Subtasks:** 6 (3.1-3.6, with 3.5 by Bug Killa)
- **Duration:** 3 days (Wed-Fri)
- **Status:** READY
- **Est. Hours:** 12-15 hours

**Checklist:**
- [ ] Subtask 3.1: Password hashing & JWT utilities
- [ ] Subtask 3.2: Auth middleware
- [ ] Subtask 3.3: Auth service layer (register, login, refresh, logout)
- [ ] Subtask 3.4: API routes + validation
- [ ] (Bug Killa) Subtask 3.5: Tests + Postman collection
- [ ] Subtask 3.6: Full integration check

**Deliverables:**
- 4 auth endpoints working
- JWT token system functional
- Session management with Redis
- Postman collection with examples
- OpenAPI documentation

---

## Testing Workflow

**Standard Pattern (TDD #4):**
1. You (Logic G) write code ✏️
2. Bug Killa writes/runs tests 🧪
3. Deep Dive documents 📝
4. E2E validation before merge ✅

---

## Code Checklist

- [ ] TypeScript strict mode enabled
- [ ] Error handling middleware in place
- [ ] Logging for all functions
- [ ] No hardcoded secrets/keys
- [ ] Git commits after each subtask
- [ ] Code review before merge
- [ ] 85%+ test coverage

---

## Blocking Issues

- [ ] Which PostgreSQL setup? (Local vs Docker?)
- [ ] GitHub repo location for frog-api?
- [ ] Redis for session storage ready?

---

## Next Phase

After Phase 1 complete: [[../Projects/FROG/Phase 1 Tasks]] → TASK & AGENT APIs (Week 2)

---

## Linked

- Master: [[../Master Task List]]
- Project: [[../Projects/FROG/Phase 1 Tasks]]
- QA Partner: [[Bug Killa Tasks]]
