# Mappy boi is easy to break

This is an an app for citizens to report abandoned bicycles to their municipality.

## Tasks

> Before starting, read the code! 🤓
>
> - As a developer, you won't only be spending time writing code, but also **reading** existing code
> - Try and understand what it is doing

> Answer the questions below, and write your answers in the `README.md`

You can switch to the relevant folder or even open it directly in a new VS Code.

- BACKEND

  - `$ cd backend`
  - `$ npm i`
  - `$ npm run dev`

- FRONTED
  - `$ cd frontend`
  - `$ npm i`
  - `$ npm run start`

### Task 1

When you run the frontend, you'll notice it gives an error.

This is because the backend is sending malformed data! It looks like someone was able to save broken data into the "database"!

1. Thinking as the hacker, how would you have tried to save this malformed data?
   a. A hacker could possibly send data to our backend which has missing or extra fields by bypassing our front end.
2. Thinking as the backend developer, how could you prevent this from happening?
   a. Add validation in the POST/reports route that can make a check on the data that is coming in if it has valid lat, langitu, and description fields!
3. Thinking as the frontend developer, how could you prevent the page from crashing from this malformed data?
   a.Add defensive coding to handle the cases where we dont get valid lt or lng .
   We can make a check(in this case I used the && operator and the ternary operator which say if the report has valid lng lt the give them the data but if they don' have it return to them null)

### Task 2

Delete the broken object and reload the page.

- Does the page work now?
  Yes, the frontend loads correctly.

### Task 3

We have another issue. Automated bots can easily submit multiple false reports.

> Research: What is a captcha?
> CAPTCHA (Completely Automated Public Turing test to tell Computers and Humans Apart) is used to distinguish between human users and automated bots by presenting challenges that are easy for humans but difficult for bots, such as recognizing distorted text or identifying objects in images.(the thing that keeps asking you if you are a robot on websites before sending data)

1. How would you try to make this form only accept entries from humans?
   Math CAPTCHA: Add a simple question like “What is 3 + 5?” to the form and verify the answer on the backend.
2. Explain how would you design a captcha for this form
   Checkbox CAPTCHA: A checkbox labeled “I am not a robot” could also be added, though this is simpler and may be easier to bypass by advanced bots.

## Bonus Tasks

1. Implement a captcha for this form without using any extra npm dependencies
2. Make the frontend look 𝓖𝓸𝓸𝓭
