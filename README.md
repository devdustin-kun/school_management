# School Management System (Django + PostgreSQL)

Production-minded Django project for a School Management System with:
- Custom user model and role-based access
- Admin, Teacher, and Student dashboards
- Student records and enrollment history
- Schedule and class offerings
- Teacher grade entry and student grade viewing
- Assignments and announcements
- Confidential end-of-term teacher evaluations
- DRF APIs for selected read/write flows

## Quick start

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements/dev.txt
cp .env.example .env
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

## Apps
- `apps.accounts` - auth, roles, profiles
- `apps.academics` - terms, subjects, sections, rooms, classes
- `apps.students` - student records and enrollment history
- `apps.teachers` - teacher records
- `apps.scheduling` - schedule slots and calendars
- `apps.grades` - assessments, gradebook, final grades
- `apps.learning` - announcements, assignments, submissions
- `apps.evaluations` - confidential teacher evaluations
- `apps.api` - DRF serializers, permissions, viewsets

## Notes
- Media files are configured for local development; use S3 or another object store in production.
- Evaluation confidentiality is implemented using eligibility tokens separate from response bodies.
- Add Celery/Redis later if you want background notifications or reports.
