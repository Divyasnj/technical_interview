## 1. Explain one technical concept you learned recently that initially confused you.

### JWT authentication and protected routes initially confused me. I understood login and signup, but I did not clearly understand how the token is generated, stored, and verified on every request. While working on my Expense Tracker and Cable Operator Management System, I learned how JWT works end-to-end—how the backend generates a token after login, how it is sent in headers, and how middleware verifies it to protect routes. Implementing it practically cleared my confusion.

## 2. When something works locally but fails later in production, what are the first 3 things you would check?
```
Environment variables (API URLs, database URLs, secrets)

API/network issues such as CORS or incorrect backend endpoints

Build or deployment differences like missing dependencies or incorrect build configuration
```
3. Describe your step-by-step approach when you face a problem you don’t know how to solve.

First, I clearly understand the problem and reproduce the issue.
Second, I break it into smaller parts and identify what I already know.
Third, I check documentation, error messages, and logs.
Then I try small experiments or test cases.
If needed, I ask for help with specific questions after trying on my own.

4. What does “writing good quality code” mean to you? Give few examples.

Good quality code means readable, maintainable, and reliable code.
Examples:

Using meaningful variable and function names

Keeping functions small and focused

Handling errors properly instead of ignoring them

Writing reusable components in React instead of duplicate code

5. What is one mistake you made in a project and what did you learn from it?

In one project, I did not plan the database schema properly and later faced issues while adding new features. I had to refactor many parts. I learned the importance of designing data models carefully before implementation and thinking about future requirements.

6. Which technology or technical tool or language are you most uncomfortable with, and why?

I am least comfortable with advanced DevOps concepts like deployment pipelines and cloud configuration because I have limited hands-on experience with them. However, I am actively trying to improve by learning deployment basics and environment management.

7. How do you usually learn a new technology? (steps)

Understand the basic concepts and use cases

Go through official documentation or beginner tutorials

Build a small project or feature using it

Debug errors and explore edge cases

Apply it in a larger project for better understanding

8. If you break something in a shared environment, what would you do next?

I would immediately inform the team, explain what happened honestly, and try to fix it as soon as possible. If I cannot fix it alone, I would ask for help and ensure it does not happen again by understanding the root cause.

9. Describe a project you are proud of. What part did you personally own?

I am proud of the Expense Tracker project. I personally handled JWT authentication, protected routes, backend APIs, and frontend integration. I also worked on CRUD operations, filtering, and PDF export features. It helped me understand full-stack development practically.

10. When you disagree with someone’s technical approach in a team, how would you handle it?

I would first listen to their reasoning, then calmly explain my perspective with technical points. If needed, I would suggest testing both approaches. I believe respectful discussion leads to better solutions.

11. What kind of problems do you enjoy solving the most, and why?

I enjoy solving logical and real-world problems, especially those involving backend logic, data handling, and algorithms. They challenge my thinking and improve my problem-solving skills.

12. Where do you want to improve the most in the next 1 year, and how will you work on it?

I want to improve my system design understanding and production-level development skills. I plan to work on larger projects, learn deployment, improve code quality, and practice more real-world scenarios.

13. If you have to build your old project today, what would you do differently?

I would design the database and project structure more carefully, write cleaner reusable code, add better error handling, and improve security and performance from the beginning.

14. What is one bad decision you made in your projects?

One bad decision was rushing implementation without fully understanding requirements. This caused rework later. I learned to spend more time on planning and understanding before coding.

15. What feedback did you receive on your projects, and how did you respond to it?

I received feedback to improve UI consistency and code structure. I took it positively, refactored components, improved responsiveness, and followed better coding practices.

16. If this project were used in a real company, what risks or issues would you worry about first?

Security, data privacy, scalability, and proper error handling would be my main concerns. I would also worry about performance and proper access control.

17. If all your team members oppose you in a situation, how would you respond and continue working effectively?

I would listen carefully to their opinions, understand their concerns, and reassess my approach. If they are correct, I would adapt. If not, I would suggest validating with data or experiments. Team success is more important than being right.
