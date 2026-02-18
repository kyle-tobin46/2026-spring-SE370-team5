# Adaptive Gym Training App  
## Agile Project Plan

---

# 1. Project Overview

This project follows an Agile approach using:
- Epics
- User Stories
- Acceptance Criteria
- Incremental Sprint Delivery

The goal is to build an adaptive gym workout app that:
1. Collects user data
2. Generates a personalized workout plan
3. Tracks workouts and difficulty
4. Adjusts future workouts
5. Displays progress over time

---

# 2. Product Backlog (Agile Format)

---

# EPIC 1 — User Onboarding

---

## User Story 1.1 — Create Profile  
**Story Points:** 3  

**User Story**  
As a new user, I want to enter my personal details so that the app can personalize my workout plan.

**Acceptance Criteria**
- User can input age, gender, height, and weight
- Inputs are validated (no negative or empty values)
- Data is saved locally

**Tasks**
- Design onboarding UI
- Implement input validation
- Create User data model
- Store profile data

---

## User Story 1.2 — Select Fitness Goal  
**Story Points:** 2  

**User Story**  
As a user, I want to select my fitness goal so that my workouts align with what I want to achieve.

**Acceptance Criteria**
- User can select goal (strength, bodybuilding, etc.)
- Goal is saved
- Goal influences workout generation logic

**Tasks**
- Create goal selection UI
- Store selected goal
- Connect goal to workout logic

---

## User Story 1.3 — Set Weekly Availability  
**Story Points:** 3  

**User Story**  
As a user, I want to select which days I can work out so that my plan fits my schedule.

**Acceptance Criteria**
- User can select days of the week
- At least one day must be selected
- Selection is saved

**Tasks**
- Build calendar/day selector
- Validate minimum selection
- Save availability

---

# EPIC 2 — Workout Plan Generation

---

## User Story 2.1 — Perform Baseline Test  
**Story Points:** 5  

**User Story**  
As a user, I want to input baseline performance data so that the app can calculate appropriate starting weights.

**Acceptance Criteria**
- User can input weight and reps
- App calculates estimated 1RM
- Starting working weight is generated

**Tasks**
- Create baseline input screen
- Implement 1RM calculation formula
- Store baseline results

---

## User Story 2.2 — Generate Weekly Plan  
**Story Points:** 8  

**User Story**  
As a user, I want the app to generate a weekly workout schedule so that I know what to do each day.

**Acceptance Criteria**
- Workouts are assigned to selected days
- Each workout includes exercises, sets, reps, and weight
- Muscle groups are displayed

**Tasks**
- Create simple exercise database
- Build routine generation algorithm
- Assign exercises per day
- Display weekly plan UI

---

# EPIC 3 — Workout Tracking

---

## User Story 3.1 — Log Workout Completion  
**Story Points:** 5  

**User Story**  
As a user, I want to log whether I completed my workout so that the app can track my consistency.

**Acceptance Criteria**
- User can mark workout complete
- Completed workout is stored
- Workout history updates

**Tasks**
- Create workout session UI
- Add completion toggle
- Save session data

---

## User Story 3.2 — Rate Exercise Difficulty  
**Story Points:** 5  

**User Story**  
As a user, I want to rate the difficulty of exercises so that future workouts can adjust accordingly.

**Acceptance Criteria**
- User can select difficulty (easy, moderate, hard, failed)
- Rating is stored per exercise
- Ratings are accessible to adaptation logic

**Tasks**
- Add difficulty selector UI
- Store difficulty data
- Connect ratings to adjustment engine

---

# EPIC 4 — Adaptive Adjustment Logic

---

## User Story 4.1 — Increase Weight After Easy Workout  
**Story Points:** 5  

**User Story**  
As a user, I want weights to increase when workouts feel easy so that I progressively improve.

**Acceptance Criteria**
- If difficulty = easy → weight increases next session
- Updated weight appears in next week's plan

**Tasks**
- Implement progression rule (+5 lbs)
- Modify weekly plan generator
- Test progression logic

---

## User Story 4.2 — Reduce Weight After Failed Set  
**Story Points:** 5  

**User Story**  
As a user, I want weights reduced if I fail a set so that future workouts are achievable.

**Acceptance Criteria**
- If difficulty = failed → weight decreases
- Adjustment persists in future plans

**Tasks**
- Implement regression rule (-5 lbs)
- Integrate into adaptation logic
- Test edge cases

---

# EPIC 5 — Progress Tracking

---

## User Story 5.1 — View Strength Progress  
**Story Points:** 5  

**User Story**  
As a user, I want to see how my lifting weight changes over time so that I can measure improvement.

**Acceptance Criteria**
- Workout data is stored historically
- App displays weight progression chart
- Chart updates after each workout

**Tasks**
- Store historical workout data
- Implement simple chart view
- Connect chart to stored data

---

# 3. Sprint Plan

---

## Sprint 1 — User Setup (Week 1)
- User Story 1.1 — Create Profile
- User Story 1.2 — Select Fitness Goal
- User Story 1.3 — Set Weekly Availability

**Deliverable:**  
User can complete onboarding and save profile data.

---

## Sprint 2 — Plan Generation (Week 2)
- User Story 2.1 — Baseline Test
- User Story 2.2 — Generate Weekly Plan

**Deliverable:**  
User receives a full weekly workout plan.

---

## Sprint 3 — Workout Tracking (Week 3)
- User Story 3.1 — Log Workout Completion
- User Story 3.2 — Rate Exercise Difficulty

**Deliverable:**  
User can complete and log workouts.

---

## Sprint 4 — Adaptation & Progress (Week 4)
- User Story 4.1 — Increase Weight
- User Story 4.2 — Reduce Weight
- User Story 5.1 — View Progress

**Deliverable:**  
App adapts workouts and displays progress charts.

---

# 4. Definition of Done

A user story is considered complete when:
- All acceptance criteria are met
- Functionality works without errors
- Data is saved and retrievable
- Feature is testable through UI
- Code compiles and runs successfully

---

# 5. Agile Principles Applied

- Work is delivered incrementally
- Features are user-centered
- Each sprint produces usable functionality
- Feedback from workout logging improves future plans
- Adaptation logic reflects iterative development
