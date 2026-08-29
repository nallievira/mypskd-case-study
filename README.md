# MyPSKD — School Learning Management System

A portfolio case study of **MyPSKD**, a full-stack Learning Management System (LMS) developed collaboratively for school learning, assessment, communication, and classroom management across mobile and web.

> **Case study note**
>
> This repository documents the project, product decisions, and my contribution. The original application source code is maintained in the team’s development repository and is intentionally not duplicated here.

## Project Snapshot

- **Project period:** February–June 2026
- **Context:** Academic Software Development capstone
- **Team:** 3-person core development team
- **Platforms:** Mobile and web
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
- Support class discussions
- Run randomized digital examinations
- Auto-save examination progress
- Monitor active examinations from the teacher side
- Detect and record tab-switch behavior during examinations
- Export examination results
- Provide in-app chat
- Support teacher-created online meetings

## My Role & Contributions

This was a **collaborative team project**. My contribution evolved throughout development rather than staying within a single fixed role.

During the earlier stages, I contributed primarily to **frontend implementation and UI/UX work**, while also helping coordinate communication across the team. As development progressed, I expanded into **database and backend work**, supporting integration between the user-facing application, Firebase data layer, and backend services.

My contribution included:

- Frontend implementation for application workflows
- UI/UX refinement and interface consistency
- Cross-team communication and coordination during iterative development
- Supporting Firestore/database work as the application scope grew
- Supporting backend implementation and integration using Node.js and Express
- Participating in testing, debugging, and feature refinement across sprints
- Helping prepare the product for final demonstration and exhibition

## Technology Stack

| Layer | Technologies |
| --- | --- |
| Mobile | Flutter |
| Web | React / Next.js |
| Backend | Node.js, Express |
| Database | Firebase Firestore |
| Authentication & authorization | JWT, Role-Based Access Control (RBAC) |
| Deployment | Vercel |

## System Architecture

At a high level, MyPSKD combines two client experiences with shared backend and data services:

```text
Flutter Mobile App ─┐
                    ├── Node.js / Express Services ── Firebase Firestore
React / Next.js Web ┘                 │
                                      └── JWT + RBAC
```

The role-based structure was important because students, teachers, and administrators interact with the same school data differently. Authentication and authorization therefore had to be treated as part of the application architecture rather than only as a login screen.

## Product & Engineering Decisions

### Role-based workflows

Instead of exposing the same interface to every user, MyPSKD separates workflows by role. Teachers manage learning activities and assessment, students access and submit learning work, while administrators handle higher-level system management.

### Examination monitoring

The examination feature was designed as more than a static question form. It includes randomized questions, auto-save, teacher-side monitoring, result export, and tab-switch event detection. The tab-switch mechanism should be understood as **behavioral monitoring**, not as a guarantee that cheating can be prevented.

### Shared product across mobile and web

Building both Flutter and web clients required the team to think about consistent workflows across different interfaces while keeping shared data and permissions synchronized.

## Development Process

The project was developed using **Scrum over 7 sprints**. Features were implemented and refined iteratively rather than built as a single final release.

This process required the team to repeatedly coordinate UI behavior, data structure, backend logic, role permissions, and feature dependencies as the product became more complex.

## Testing & Quality

The project included:

- **Black-box testing** for application functionality
- **User Acceptance Testing (UAT)**
- Software-quality evaluation informed by **ISO/IEC 9126** quality characteristics

Testing was used not only to verify individual functions but also to identify integration issues between features and user roles.

## Outcome

MyPSKD reached a demonstrable end-to-end product state and was presented at a university project exhibition. Feedback at the exhibition included encouragement to explore **commercializing the system**, which showed that the project was understandable as a potential product rather than only as a classroom prototype.

## What I Learned

This project gave me experience beyond implementing isolated features. I learned how technical decisions interact with product scope, team communication, user roles, and delivery constraints.

Key takeaways included:

- Building software across frontend, backend, and database boundaries
- Translating school workflows into role-based product features
- Working in an iterative multi-person development process
- Communicating across responsibilities when project needs changed
- Debugging integration problems rather than only local code issues
- Thinking about usability and technical implementation together
- Evaluating a working system through testing and user acceptance

## Repository Purpose

This repository is intentionally a **case study**, not a duplicate of the original team source repository. It exists to document the product, the engineering context, and my individual contribution clearly for portfolio review.

Screenshots, architecture visuals, original source attribution, and demo references can be added here as the project documentation is organized and verified.
