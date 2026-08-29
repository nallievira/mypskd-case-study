# MyPSKD — School Learning Management System

A portfolio case study of **MyPSKD**, a full-stack Learning Management System (LMS) developed collaboratively for school learning, assessment, communication, and classroom management across mobile and web.

> **Case study note**
>
> This repository documents the project, product decisions, and my contribution. The original application source code is maintained in the team development repository and is intentionally not duplicated here.
>
> **Original team repository:** https://github.com/Elvan1210/SoftwareDevelopment-Project-Kelompok9

## Project Snapshot

- **Project period:** February–June 2026
- **Context:** Academic Software Development capstone
- **Team:** 3-person core development team
- **Platforms:** Mobile and web from a shared Flutter codebase
- **Primary users:** Students, teachers, and administrators
- **Development approach:** Scrum across 7 sprints

## The Problem

School learning workflows are often fragmented across separate tools for assignments, attendance, grades, announcements, communication, meetings, and examinations. MyPSKD was designed as a unified school platform that brings these workflows into one role-based system.

## The Solution

MyPSKD supports three primary roles — **Student, Teacher, and Admin** — with different permissions and workflows. The system combines everyday classroom management with digital assessment and communication features in one product.

### Core Capabilities

- Join classes using class codes
- Share and access learning materials
- Create, submit, and manage assignments
- Record and review attendance
- Manage grades and teacher feedback
- Publish announcements
- Support class discussions and channels
- Run digital examinations and quizzes
- Auto-save examination progress
- Monitor active examinations from the teacher side
- Detect and record tab-switch behavior during examinations
- Export examination results
- Provide private and group messaging
- Support teacher-created online meetings

## My Role & Contributions

This was a **collaborative team project**. My contribution evolved throughout development rather than staying within a single fixed role.

I initially focused heavily on **Flutter frontend implementation and UI/UX**, particularly responsive teacher-facing and classroom workflows. As development progressed, I also worked across **backend routes, Firestore integration, messaging behavior, notifications, and feature integration**, while helping coordinate and refine the product across iterations.

Selected contributions visible in the original repository include:

- Redesigned and refined the **Teacher Dashboard and teacher classroom views**
- Improved responsive Flutter behavior across **mobile and web**, including navigation, overflow handling, class views, quizzes, learning materials, attendance, and grading interfaces
- Extended the messaging system with **message unsend, per-user clear chat, leave-group behavior, polling, and Socket.IO integration fixes**
- Improved assignment workflows so newly created assignments could be **posted to the selected class channel** and generate **student notifications**
- Implemented backend/Firestore behavior for teacher announcements, including **student notifications and channel posting**
- Refined teacher workflows for class access requests, assignments, grades, announcements, and classroom navigation
- Participated in testing, debugging, integration, and feature refinement throughout development
- Helped prepare the working product for final demonstration and exhibition

### Contribution Evidence

The original team repository retains merged pull requests under my GitHub account (`nallievira`), including:

- [PR #67 — Messaging: unsend, clear chat, leave group, polling, and socket fixes](https://github.com/Elvan1210/SoftwareDevelopment-Project-Kelompok9/pull/67)
- [PR #68 — Responsive UI and teacher workflow improvements, including assignment notifications](https://github.com/Elvan1210/SoftwareDevelopment-Project-Kelompok9/pull/68)
- [PR #81 — Teacher Dashboard and teacher classroom UI redesign](https://github.com/Elvan1210/SoftwareDevelopment-Project-Kelompok9/pull/81)
- [PR #89 — Teacher classroom views, access workflow, and assignment UI](https://github.com/Elvan1210/SoftwareDevelopment-Project-Kelompok9/pull/89)

These links are included to make my individual contribution to the collaborative codebase directly traceable.

## Technology Stack

| Layer | Technologies |
| --- | --- |
| Client | Flutter / Dart — shared mobile and web application |
| Backend | Node.js, Express |
| Database | Firebase Firestore |
| Authentication & authorization | JSON Web Tokens (JWT), Role-Based Access Control (RBAC) |
| Real-time communication | Socket.IO |
| File/media handling | Cloudinary |
| Online meetings | Jitsi Meet integration |
| Deployment | Vercel |

## System Architecture

At a high level, MyPSKD uses a shared Flutter client for mobile and web, connected to Node.js/Express services and Firebase Firestore.

```text
                 ┌── Flutter Mobile
Flutter Client ──┤
                 └── Flutter Web
                         │
                  REST API / Socket.IO
                         │
                  Node.js + Express
                         │
            JWT authentication + RBAC
                         │
                 Firebase Firestore
```

The role-based structure was important because students, teachers, and administrators interact with the same school data differently. Authentication and authorization therefore had to be treated as part of the application architecture rather than only as a login screen.

## Product & Engineering Decisions

### Role-based workflows

Instead of exposing the same interface to every user, MyPSKD separates workflows by role. Teachers manage learning activities and assessment, students access and submit learning work, while administrators handle higher-level system management.

### Examination monitoring

The examination feature was designed as more than a static question form. It includes randomized questions, auto-save, teacher-side monitoring, result export, and tab-switch event detection. The tab-switch mechanism should be understood as **behavioral monitoring**, not as a guarantee that cheating can be prevented.

### Shared Flutter product across mobile and web

Using Flutter for both mobile and web allowed the project to share a substantial portion of its application structure while still requiring responsive behavior for different screen sizes and interaction patterns. Several development iterations therefore focused specifically on adapting classroom workflows between mobile and browser layouts.

### Real-time and asynchronous communication

Communication features combine Socket.IO behavior with persistent data in Firestore. During development, messaging workflows also had to account for mobile behavior, conversation state, message history, group membership, and user-specific actions such as clearing a conversation.

## Development Process

The project was developed using **Scrum over 7 sprints**. Features were implemented and refined iteratively rather than built as a single final release.

This process required the team to repeatedly coordinate UI behavior, data structure, backend logic, role permissions, and feature dependencies as the product became more complex.

## Testing & Quality

The project included:

- **Black-box testing** for application functionality
- **User Acceptance Testing (UAT)**
- Software-quality evaluation informed by **ISO/IEC 9126** quality characteristics

Testing was used not only to verify individual functions but also to identify integration issues between features, platforms, and user roles.

## Outcome

MyPSKD reached a demonstrable end-to-end product state and was presented at a university project exhibition. Feedback at the exhibition included encouragement to explore **commercializing the system**, which showed that the project was understandable as a potential product rather than only as a classroom prototype.

## What I Learned

This project gave me experience beyond implementing isolated features. I learned how technical decisions interact with product scope, team communication, user roles, and delivery constraints.

Key takeaways included:

- Building software across frontend, backend, and database boundaries
- Translating school workflows into role-based product features
- Developing responsive product behavior across mobile and web
- Working with real-time communication and persistent application state
- Working in an iterative multi-person development process
- Communicating across responsibilities when project needs changed
- Debugging integration problems rather than only local code issues
- Thinking about usability and technical implementation together
- Evaluating a working system through testing and user acceptance

## Repository Purpose

This repository is intentionally a **case study**, not a duplicate of the original team source repository. It exists to document the product, the engineering context, and my individual contribution clearly for portfolio review.

The original source code and contribution history remain available in the linked team repository. Screenshots, architecture visuals, and verified demo references can be added here as the remaining project documentation is organized.
