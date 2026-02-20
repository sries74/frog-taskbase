# FROG - Phase 1 Tasks (Weeks 1-2)

**Project:** THE FROG (Team Task Dashboard)
**Phase:** 1 - Backend Foundation & Authentication
**Duration:** 2 weeks
**Team Lead:** Run CMD
**Developers:** Logic G
**QA:** Bug Killa
**Research/Docs:** Deep Dive

---

## MILESTONE: Backend Foundation Ready

### TASK 1: Database Setup (Mon-Tue) — Assigned to: **Logic G**

- [ ] SUBTASK 1.1: PostgreSQL Environment
  - [ ] Install PostgreSQL 15 locally OR Docker
  - [ ] Create database `frog_dev`
  - [ ] Create user `frog_user`
  - [ ] Verify connection
  - [ ] Install PgBouncer
  
- [ ] SUBTASK 1.2: Prisma Schema
  - [ ] Install Prisma
  - [ ] Create `.env` file
  - [ ] Copy schema from team-task-dashboard
  - [ ] Review 14 tables
  
- [ ] SUBTASK 1.3: Migrations & Seeds
  - [ ] Run Prisma migrations
  - [ ] Create seed script (4 users, 7 agents, 42 tasks)
  - [ ] Seed database
  - [ ] Verify with Prisma Studio
  
- [ ] SUBTASK 1.4: Backup & Validation
  - [ ] Create database dump
  - [ ] Store in backups/
  - [ ] Test restore
  - [ ] Document connection string

**Status:** READY  
**Assigned to:** Logic G  
**Estimate:** 2 days  
**Acceptance Criteria:** `npx prisma studio` shows all 14 tables populated

---

### TASK 2: Backend Scaffold (Tue-Wed) — Assigned to: **Logic G**

- [ ] SUBTASK 2.1: Express Project
  - [ ] Create directory
  - [ ] Initialize Express + TypeScript
  - [ ] Install core deps
  - [ ] Create tsconfig.json
  
- [ ] SUBTASK 2.2: Project Structure
  - [ ] Create src/ folders (config, controllers, middleware, etc.)
  - [ ] Create .env.example
  - [ ] Create .env.local (git-ignored)
  
- [ ] SUBTASK 2.3: Configuration
  - [ ] Environment variables
  - [ ] Logging (Pino)
  - [ ] Error handling
  - [ ] CORS setup
  - [ ] Rate limiting
  
- [ ] SUBTASK 2.4: Server Check
  - [ ] Run `npm run dev`
  - [ ] Test `/health` endpoint
  - [ ] Verify response

**Status:** READY  
**Assigned to:** Logic G  
**Estimate:** 1.5 days  
**Acceptance Criteria:** `curl http://localhost:3000/health` returns status OK

---

### TASK 3: Auth System (Wed-Fri) — Assigned to: **Logic G**

- [ ] SUBTASK 3.1: Password Hashing & JWT
  - [ ] Install bcryptjs + jsonwebtoken
  - [ ] Create auth utils (hash, compare, token gen)
  - [ ] Test locally
  
- [ ] SUBTASK 3.2: Auth Middleware
  - [ ] Create auth middleware
  - [ ] Create error handler
  - [ ] Test token validation
  
- [ ] SUBTASK 3.3: Auth Service
  - [ ] registerUser function
  - [ ] loginUser function
  - [ ] refreshTokens function
  - [ ] logoutUser function
  - [ ] Error handling
  
- [ ] SUBTASK 3.4: Auth Routes
  - [ ] POST /api/auth/register
  - [ ] POST /api/auth/login
  - [ ] POST /api/auth/refresh
  - [ ] POST /api/auth/logout
  - [ ] Input validation
  
- [ ] SUBTASK 3.5: Testing Auth — Assigned to: **Bug Killa**
  - [ ] Unit tests for auth service
  - [ ] Integration tests for endpoints
  - [ ] Coverage target: 85%+
  - [ ] Create Postman collection
  
- [ ] SUBTASK 3.6: Integration Check
  - [ ] Full auth flow test
  - [ ] Verify all 4 endpoints work
  - [ ] Generate OpenAPI docs

**Status:** READY  
**Assigned to:** Logic G (dev) + Bug Killa (tests)  
**Estimate:** 3 days  
**Acceptance Criteria:** Full auth flow working (register → login → refresh → logout)

---

## Success Criteria (EOW Week 1)

- ✅ PostgreSQL seeded with data
- ✅ Express server running :3000
- ✅ /health endpoint responds
- ✅ Auth system fully tested
- ✅ 4 endpoints working
- ✅ Postman collection created
- ✅ OpenAPI docs generated
- ✅ 85%+ test coverage
- ✅ Code committed to GitHub

---

## Linked Tasks

- [[../../../Agents/Logic G Tasks]]
- [[../../../Agents/Bug Killa Tasks]]
- [[../Master Task List]]
