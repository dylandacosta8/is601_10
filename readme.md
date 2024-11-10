### <h1 align=center>Homework 10</h1>
<div align=center>

This repository contains fixes for several issues as per instructor videos and course material.

</div>

---
<div align=>

### The Homework meets the following goals:

1. Fixes several issue found throughout the codebase.
2. Passes all the tests during the GitHub Actions Workflow <b>> </b><a href="https://github.com/dylandacosta8/is601_10/actions"><b>here</b></a>
3. Successfully runs the CI pipeline and pushes the built and scanned image to DockerHub <b>> <a href="https://hub.docker.com/repository/docker/dylan08/is601_10/tags">here</a></b>
4. The codebase includes extensive test coverage as high as 91% including tests for fixes made during the assignment.
5. Follows best practices for Git and GitHub using branching, pull requests, code reviews, GitHub Issues, GitHub Actions, etc.
6. Includes clear documentation with links to closed issues.
7. Maintains well structured Issue tracking and explanations.

</div>

---
### Closed Issues (8):

* <b><u> Username(Nickname) Validation: </u></b>
    <br>
    1. **Description:** Nickname committed to the user table using the /register/ API was replaced by an autogenerated one.\
    **Issue Link:** <a href="https://github.com/dylandacosta8/is601_10/issues/2"> here </a>\
    **Resolution:** Replaced the generate_nickname() method with the nickname passed in as a part of the user data.
    2. **Description:** /register/ API allowed creation of users with elevated privileges such as admin, root and superuser.\
    **Issue Link:** <a href="https://github.com/dylandacosta8/is601_10/issues/4"> here </a>\
    **Resolution:** Added a validator for nickname in place that checks if the nickname is one of the above.\
    3. **Description:** No validation to cap the length of the nickname.\
    **Issue Link:** <a href="https://github.com/dylandacosta8/is601_10/issues/6"> here </a>\
    **Resolution:** Added a max_length attribute to the nickname field for registration and creation and capped it at 20 characters.\
    4. **Description:** Nickname uniqueness not enforced.\
    **Issue Link:** <a href="https://github.com/dylandacosta8/is601_10/issues/8"> here </a>\
    **Resolution:** Added additional logic to guarantee a unique nickname on top of the existing logic to check for uniqueness of email.\
    <br>
* <b><u> Instructor Video Issue: </u></b>
    <br>
    1. **Description:** Swagger UI default endpoint data mismatch.\
    **Issue Link:** <a href="https://github.com/dylandacosta8/is601_10/issues/10"> here </a>\
    **Resolution:** Replaced all instances of generate_nickname() method with static nicknames for all API endpoints.\
    <br>
* <b><u> Password Validation: </u></b>
    <br>
    1. **Description:** No password requirements enforced.\
    **Issue Link:** <a href="https://github.com/dylandacosta8/is601_10/issues/12"> here </a>\
    **Resolution:** Added validation in place for passwords so that they have a minimum length of 6 characters, include at least one capital letter, include at least 1 number and include at least 1 special character.\
    <br>
* <b><u> Profile Field Edge Cases: </u></b>
    <br>
    1. **Description:** No validation to verify if profile_picture_url link includes images in an acceptable image format.\
    **Issue Link:** <a href="https://github.com/dylandacosta8/is601_10/issues/14"> here </a>\
    **Resolution:** Added validation in place for profile_picture_url so that it only accepts links that end in a valid image format such as .jpg, .jpeg and .png\
    <br>
* <b><u> Additional Issues: </u></b>
    <br>
    1. **Description:** Missing test fixtures and mismateched conftest data.\
    **Issue Link:** <a href="https://github.com/dylandacosta8/is601_10/issues/16"> here </a>\
    **Resolution:** Created fixtures to generate user, admin and manager tokens as well as fixed issues with standardization of data in conftest.py.\
    <br>
* <b><u> Note: </u></b>There were many other issues that could be addressed but as the assignment required me to close only 5 and the 1 from the instructor video. I chose to close no more than 8.
---

### Assignment Reflection:

Working on an assignment and fixing issues from a QAs point of view was very interesting and challenging at the same time. Going step by step through the user lifecycle on the event manager application and finding issues helped me understand the codebase and allowed to me write code to tackle it with the help of new functions or making use of existing ones.

It was also pretty fun working with Docker compose and seeing how the various services communicate with each other over their internal network and learning to resolve interal hostnames while connecting to posgres using pg-admin.

Writing comprehensive test cases for newly created logic and enhancing the coverage for the existing codebase helped me get even deeper into the functionality of the code and by the end of the assignment I was almost familiar with what was where and where changes need to be made in order to fix something.