# The billing system as it runs today

What Glenn knows about the system his floor uses every night. He lives with this list. He does not recite it. He uses it to tell whether the person across from him has looked.

## What it does well

- Bills about 300,000 standard accounts a month without anyone touching them.
- Posts payments, handles deposits and late fees.
- Has not missed a print deadline in 14 months. That is his team's doing, and he knows the count.

## Billing: what it can't do, and what his people do instead

1. **Solar customers (net metering).** About 6,400 accounts. About 900 of them are on a solar tariff that closed to new customers in 2011 and pays out banked credit in cash every April. The system can't carry a banked credit from one month to the next. Denise and one other analyst calculate those bills in a spreadsheet and key the results in. About three working days every month.
2. **Budget billing true-up.** About 38,000 accounts pay a level amount and get trued up once a year. The system computes the true-up wrong for any account that changed rate during the year. The team reviews all 38,000 by hand each spring. Six weeks, four people, led by Curtis.
3. **Rate changes.** A new rate has to be loaded into configuration tables the last vendor built and never documented. The last rate change took 19 weeks to load and test. The commission's effective date passed while they were still testing. Result: three cycles billed at the old rate and about 46,000 bills had to be corrected.
4. **Time-of-use rates.** The system cannot bill them at all. The commission has ordered a time-of-use option for residential customers by January 1, 2029. The current system has no way to meet that date. It is the reason the board approved a replacement.
5. **Correcting bills in bulk.** Cancel and rebill works one account at a time. A bad meter read file means days of keying. Those 46,000 corrections took twelve working days with the whole floor on it.
6. **Reports.** Aging, unbilled revenue and the exceptions report were in the contract and never delivered. Marcus built those three outside the system, and eleven more that finance uses at month-end. Fourteen in-house reports in all. Month-end close depends on queries only he understands.
7. **The nightly run.** A cycle starts at 9:00 p.m. and takes about seven hours. If it fails any time after 11:00 p.m. there is not enough night left to run it again before the 6:00 a.m. print deadline. Someone from his floor is on call every billing night.

## Notices and collections: where it gets the rules wrong

The commission sets a path every unpaid bill has to walk before service can be shut off: a reminder, a written shutoff notice, a waiting period, then a final contact attempt. Each step has a minimum number of days. A customer can dispute a bill at any step. The company has to assume any shutoff may be challenged later, so every notice and every date has to be provable.

The notices come out of the billing system, so they land on Glenn's floor even though the Collections group works the accounts.

8. **The clock restarts.** Each unpaid bill is supposed to walk the path on its own clock. The system keeps one clock per account. When a customer already on the path gets a new past-due bill, the whole account goes back to day one. A customer who is late every month never reaches the end. About 4,300 accounts have been on the path for more than a year. Together they owe about $6.1 million.
9. **Duplicate notices.** When an account has more than one unpaid bill, the system sends a separate shutoff notice for each one. Some customers get three notices in a week with three different amounts. They call. Last year about 140 commission complaints named confusing notices.
10. **Third-party copies.** About 5,200 customers have named someone else to receive a copy of any shutoff notice: a relative, a caseworker. The commission requires that copy to go out. The system stores the name and never generates the letter. Lorraine pulls a list every morning and mails the copies by hand.
11. **Business mailing addresses.** The system holds one mailing address per account and has no attention line. About 1,900 commercial accounts need the bill sent to a different address than the service location, addressed to a named person or department. Bea types the name into the second address line. The print vendor's software sometimes cuts it off, and the bill sits in a mailroom until it is late.

## What that costs

- By Glenn's count, roughly four of his nine people do nothing but cover what the system can't do.
- None of the manual procedures existed in the vendor's documentation. His team wrote all of them.
- Items 8 through 10 are the ones that worry him most. A billing error gets corrected. A notice error can end up in front of the commission.
- The manual procedures work. They are slow and they are correct. Very few bills go out wrong.
