# Listings App

This app contains the booking functionality with Celery background tasks for email notifications.

## Files

- `tasks.py` - Contains the `send_booking_confirmation_email` shared task
- `views.py` - Contains the `BookingViewSet` that triggers email tasks on booking creation
