# Capstone Product Plan
The second deliverable for the capstone is your product plan.

## Product Plan Components
1. __Personal Learning Goals__: A list outlining the major things that you want to focus on learning in this project.
- Kirsten:
 -Leti:

1. __Problem Statement__: A clear, concise statement describing the problem your project will solve. Re-use the problem statement from the concept write-up or update if you've made adjustments.
Ada instructors, staff, and students do not have a centralized classroom app that meets all of their needs. They would benefit from an web-based application that helps them view assignment submissions, provides a clear layout of lectures for that day/week, and supports other features (such as a centralized hub for documents and non-lecture resources like Charles's reviews and internship information). In addition, thorough testing is needed to ensure the most reliable site as possible for users. Ultimately, the goal is of this capstone project is to produce a working classroom management application that provides a solid foundation for future versions of the app.

1. __Market Research__: Outline the key insights from your research, including:
    - your application’s competition - what alternatives are already out there (competing apps and/or non-app solutions)
    - research from users on why these alternatives do not effectively address the problem.
    - differentiation: what makes your idea/product different
    
    Google Classroom, Canvas, BlackBoard, and Schoology are different learning management systems (LMS) and classroom management systems (CMS). These do address a number of needs Ada has. For example, Canvas allow instructors to restrict access to the class's site to invited users, prohibits students from accessing instructors-only areas, manages assignments, allows assigning of groups, tracks attendance, has a calendar, and provides some basic information about grade trends. Most of the other previously-provided list of apps have similar functionality.
    
    But these apps do not meet all of Ada's needs. First, the program's use of Github RP for assignments and grading does not work well with these traditional classroom apps. Ada needs an app that is smoothly works with the GitHub API, integrating much of the information it provides throughout the site (such as for the graphs). Secondly, having their own application allows them to have much more flexibility as needs change. Finally, Ada has a tight operating budget and most CMS apps have fees to access all features. The free Google Classroom, which is arguably the best free CMS, is very limited in features and mainly acts as just an centralized access point of other Google products, such as Drive.

1. __User Personas__: A summary of your main target user group(s). What are their key characteristics? How do those characteristics factor into project/app/idea?
- **Students**
  - Wants
    - Access to feedback in one place
    - View feedback on group projects, regardless of which group member submits the pull request
    - View progress over time/by unit (graphs)
    - View calendar
    - Ideally would have other information (attendance, document hub, Panopto, etc) - **not MVP features**
  - Considerations
    - May belong to more than one cohort
 - **Instructors**
   - Wants
        - Access to feedback in one place
        - View what they've graded and what they need to grade
        - View grades over time/by unit and be able to filter by cohort, class, and student (graphs)
        - View calendar
        - Assign people to groups
        - Manage student permissions/invites and assigning students to cohorts, and invites
        - Ideally would have other information (attendance, document hub, Panopto, etc)
   - Considerations
     - May be staff (Charles, Alexandra, etc) and want their own pages - **not a MVP feature**

1. __Trello Board__:
      [Trello Board](https://trello.com/b/MTc8B8yP)

1. __Technology selections__:
    - **Front-end**
        - React and Redux
        - D3
        - HTML, CSS, and Material UI
    - **Back-end**
        - Rails
        - OAuth (GitHub) and CanCan
        - GitHub API
        - Google Calendar API
        - Mock API with Postman
        - RSpec and Factory Girl
        - Jest
        - Panopto API (**not a MVP feature**)
    - **Infrastructure - Deployment or Code**
        - AWS
        - GitHub page

1. __Wireframes__:
    - https://balsamiq.cloud/sjwmnb1/py1s3xn

## Format
Since the Product Plan is part of your final deliverable and should be included in your repository, it would be easiest to do this initial draft in a markdown format for easy transferability to GitHub.
