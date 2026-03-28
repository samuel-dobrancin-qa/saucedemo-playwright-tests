Sauce Demo — Playwright UI Test Suite
A simple UI automation project built using Playwright and
Playwright Codegen on the Sauce Demo e-commerce practice app.

Honest context
I'm a manual QA engineer with 4+ years of enterprise experience.
I built this to get hands-on exposure to UI automation — not to
claim I'm an automation engineer.
I used Playwright Codegen to record the initial test flows, then
cleaned up the generated code, removed the noise, and added
meaningful assertions at each step. I can read and understand
the test code, explain what each assertion is doing and why,
and run the suite from the terminal. What I don't have yet is
the ability to build complex automation architecture from scratch
or debug deeply failing tests without guidance.
I'm adding this to my portfolio because I think it's important
to show real progress honestly rather than pretend expertise
I don't have.

What's being tested
The target is Sauce Demo — a
practice e-commerce app built for QA training.
Three test scenarios:
1. Complete purchase flow — happy path
Full end-to-end flow from login through product selection,
cart, checkout form, and order confirmation. Assertions verify
each step produced the expected result — not just that the
clicks worked, but that the right pages loaded and the right
content appeared.
2. Login fails with wrong password
Negative test. Verifies the app correctly blocks access and
shows an error message when wrong credentials are used.
This is the kind of test most beginners skip — I included
it because negative scenarios catch real bugs.
3. Checkout blocked with empty cart
Verifies the cart is genuinely empty before proceeding.
Tests the boundary condition between browsing and purchasing.

Test results
9 tests passing across 3 browsers (Chromium, Firefox, WebKit)
Runtime: ~10 seconds

What I learned from this
The biggest thing wasn't the code — it was understanding what
makes a test actually useful versus just a script that clicks
through a flow.
The raw Codegen output recorded my typos, my hesitations,
every redundant click. Cleaning it up meant understanding what
the test was actually supposed to prove, then keeping only the
actions and assertions that proved it. That's a manual testing
mindset applied to automation — and it's where I think my
background adds something.
The assertions matter more than the actions. Anyone can record
clicks. What makes a test suite reliable is verifying that
each action produced the right outcome.

How to run
bash# Install dependencies
npm install

# Run all tests
npx playwright test tests/saucedemo.spec.js

# View HTML report
npx playwright show-report

Stack

Playwright — UI automation framework
Playwright Codegen — initial test recording
Node.js


About
Samuel Dobrančin — Quality Engineer
4+ years manual and API testing, currently building automation exposure.
GitHub ·
LinkedIn
