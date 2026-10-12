# Vagtplanen

A personal tool for one worker to record the shifts they work across their jobs and check each payslip against what those shifts should have earned.

## Language

### Work

**Job**:
One employment the worker holds, with its own pay rules and pay period.
_Avoid_: Employer, workplace, position

**Archived Job**:
A Job the worker no longer holds. It is read-only, it appears only in the archive, and it cannot be un-archived.
_Avoid_: Deleted job, inactive job, old job

**Shift** (Danish: _vagt_):
A continuous stretch of time actually worked at one Job, recorded after it happened. There are no planned or scheduled shifts.
_Avoid_: Vagt, work session, scheduled shift

**Unpaid Break**:
A length of time inside one Shift that is not paid. It is recorded as a duration, not a time of day.
_Avoid_: Pause, break deduction

### Pay

**Hourly Rate** (Danish: _timeløn_):
The base amount a Job pays per hour worked. It can change over time, and each value applies from a given date onward.
_Avoid_: Wage, salary

**Supplement** (Danish: _tillæg_):
Extra pay per hour, added on top of the Hourly Rate, for time worked on certain weekdays, inside a time-of-day window, or both (e.g. Sunday; 23:00–06:00; Saturday from 15:00). If a window crosses midnight, it belongs to the day it starts. At most one Supplement applies to any hour worked, and it is the highest-paying one. Its amount can change over time, and it can end from a given date.
_Avoid_: Bonus, allowance, tillæg, day supplement, time supplement

**Gross Pay** (Danish: _bruttoløn_):
Pay before any deductions: hours times Hourly Rate, plus Supplements.
_Avoid_: Total, salary

### Payslips

**Pay Period** (Danish: _lønperiode_):
The date range one Payslip covers for one Job. It runs monthly from the Job's start day and is named after the months it spans, e.g. "January/February". A Shift belongs to the Pay Period in which it starts.
_Avoid_: Month, billing period

**Payslip** (Danish: _lønseddel_):
The itemised statement an employer issues for one Pay Period of one Job. The worker compares it by hand with the Pay Summary.
_Avoid_: Paycheck, lønseddel, salary slip

**Pay Summary**:
Vagtplanen's calculated breakdown for one Pay Period of one Job: a line for base pay and a line for each Supplement, each showing hours and amount, which add up to the Gross Pay.
_Avoid_: Expected pay, pay estimate, payslip
