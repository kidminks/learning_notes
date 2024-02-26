![[notification_service.drawio.png]]This is system design to handle notification which is based on cron jobs and is less likely linked with users.

The concurrency limiter and rate limiter is implemented to secure FCM push.

Kafka message is marked consumed first and then the message is processed to cope with the slow processing

We send around 10-15 Lakh Lakh notification per minute which was earlier only 2 - 4 Lakh Per minute earlier
Around 70 Lakh notification goes which now takes 5-6 minutes and earlier it used to took 25-20 minutes.



