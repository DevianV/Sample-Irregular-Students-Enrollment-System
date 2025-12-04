# PLM Irregular Student Enrollment System

## Overview
A web application to allow *Irregular* students to enroll in subjects. The system authenticates existing student records (no account creation), supports subject selection with validations (prereq, coreq, schedule conflict, unit checks), and finalizes enrollment producing a printable SER.

## Features
- Student-only login (Irregular-only access)
- Dashboard: Personal Info, Grades, Taken Subjects
- Subject selection with real-time validations
- Draft enrollment and Finalize (permanent) flow
- SER generation & printing

## Getting started
1. Copy `.env.example` to `.env` and configure DB and JWT secret.
2. Run migrations: `npm run migrate` or `python manage.py migrate`
3. Seed students & subjects via the provided seed script.
4. Start backend: `npm start` or `python manage.py runserver`
5. Start frontend: `npm run dev`

## API
See `/docs/api.md` for endpoints and examples.

## Tests
Run unit tests:

