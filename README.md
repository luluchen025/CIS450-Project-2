# CIS450-Project-2
Files modified in xv6 to implement a simplified O(1) scheduler.

Goal: Implement a simplified O(1) scheduler in xv6 using three FIFO queues:
- FQ (First-time Queue): new processes start here with a short quantum (10 ms)
- AQ (Active Queue): normal work queue with a longer quantum (30 ms)
- EQ (Expired Queue): processes that used up their AQ quantum are placed here. When AQ empties and EQ is non-empty, switch AQ and EQ.
