# alx_travel_app_0x03 - Celery with RabbitMQ

## Background Task Management with Celery and Email Notifications

This project implements background task management using Celery with RabbitMQ as the message broker, and includes email notification functionality for bookings.

## Setup

### 1. Install RabbitMQ:
```bash
sudo apt-get install rabbitmq-server
sudo service rabbitmq-server start
```

### 2. Install Python Dependencies:
```bash
pip install celery django-celery-beat
```

### 3. Run Celery Worker:
```bash
celery -A alx_travel_app worker --loglevel=info
```

### 4. Run Celery Beat (for scheduled tasks):
```bash
celery -A alx_travel_app beat --loglevel=info
```

## Project Structure

- `alx_travel_app/settings.py` - Django settings with Celery and email configuration
- `alx_travel_app/celery.py` - Celery app configuration
- `listings/tasks.py` - Celery tasks for email notifications
- `listings/views.py` - BookingViewSet that triggers email tasks
