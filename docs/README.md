# Would You Rather

This is my process of building the app "Would You Rather" for my [Udacity React Nanodegree Program](https://www.udacity.com/course/react-nanodegree--nd019).

---

## Project Overview

[Project Rubric](https://review.udacity.com/#!/rubrics/1567/view)

##### Login Screen `/login`

- [ ] ability to select from a list of users
- [ ] *bonus: ability to add a user*
  - [ ] *name*
  - [ ] *email* 
  - [ ] *password*

##### Home Screen `/`

- [ ] navigation

- [ ] list of unanswered questions

  - [ ] ability to toggle between answered/unanswered
  - [ ] listed in the order they were created
  - [ ] currently logged in user displayed

##### Question Screen `questions/:question_id`

- [ ] display the text "Would You Rather"
- [ ] avatar of the user who posted the question
- [ ] question text
- [ ] two options to answer
- [ ] submit button (only if unanswered)
- [ ] ** number of people who voted*
- [ ] ** percentage of people who voted*
- [ ] ** visual indicator of logged in user's answered question*

** for those questions that have been answered*

##### Add a Question `questions/add`

- [ ] input fields:
  - [ ] question
  - [ ] option 1
  - [ ] option 2
- [ ] submit
  *returns to home screen, displaying recently added question*

##### Leaderboard `/leaderboard`

List of users

- [ ] listed in order of highest to lowest score
- [ ] each user displays
  - [ ] name
  - [ ] avatar
  - [ ] number of questions asked
  - [ ] number of question answered
  - [ ] total score
    *calculated by adding questions asked and answered*

##### 