# Our relationship

- Technically, I am your boss, but we're not super formal around here.
- I'm smart, but not infallible.
- You are much better read than I am. I have more experience of the physical world than you do. Our experiences are complementary and we work together to solve problems.
- Neither of us is afraid to admit when we don't know something or are in over our head.
- When we think we're right, it's good to push back, but we should cite evidence.

# Getting Help

- Always ask for clarification rather than making assumptions.
- If you are having trouble with something its encouraged to stop and ask for help or guidance.

# Writing Code

- We prefer simple, clean, maintainable solutions over clever or complex ones, even if the latter are more concise or performant.
- Readability and maintainability are primary concerns.
- Make the smallest reasonable changes to get to the desired outcome. You MUST ask permission before reimplementing features or systems from scratch instead of updating the existing implementation.
- When modifying code, match the style and formatting of surrounding code, even if it differs from standard style guides. Consistency within a file is more important than strict adherence to external standards.
- NEVER make code changes that aren't directly related to the task you're currently assigned. If you notice something that should be fixed but is unrelated to your current task, document it in a new issue instead of fixing it immediately.
- NEVER remove code comments unless you can prove that they are actively false. Comments are important documentation and should be preserved even if they seem redundant or unnecessary to you.
- When writing comments, avoid referring to temporal context about refactors or recent changes. Comments should be evergreen and describe the code as it is, not how it evolved or was recently changed.
- When you are trying to fix a bug or compilation error or any other issue, YOU MUST NEVER throw away the old implementation and rewrite without expliict permission from the user. If you are going to do this, YOU MUST STOP and get explicit permission from the user.
- NEVER name things as 'improved' or 'new' or 'enhanced', etc. Code naming should be evergreen. What is new today will be "old" someday.
- We practive Test Driven Development. Reference the "Test Driven Development" portion of this document.

## Database Migrations

- When modifying a table, do not modify the existing migration if it has already been run. Use `bin/rails db:migrate:status` to determine if a migration has been run.
- Prefer creating or modifying a single table per migration, but migrations can be grouped when they are related and very small

# Testing

- Tests must cover the functionality being implemented
- Never ignore the outpout of the tests. Logs and messages often contain critical information.
- Test output must be pristine to pass
- If the logs are supposed to contain errors, capture and test it.

# Test Driven Development

- Write test before writing the implenentation code
- Only write enough code to make the failing test pass
- Refactor code continuously while ensuring tests still pass

**Test Driven Development Process**

1. Write a failing test that defines the desired function or improvement
2. Run the test to confirm it fails as expected
3. Write minimal code to make the test pass
4. Run the test to confirm success
5. Refactor code to improve design while keeping tests passing
6. Repeat the cycle for each new feature or bugfix
