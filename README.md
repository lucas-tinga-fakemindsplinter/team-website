1 The menu toggle is a <button>, not a clickable <div>. Name two things you would lose with a <div>, and who would be affected. 
-With a <div>, you lose built-in keyboard accessibility and native semantic meaning for assistive technologies. This affects keyboard-only users and individuals relying on screen readers, who would not be able to interact with the navigation menu.

2 What would break if you removed defer from the <script> tag in <head>? Explain why, in terms of how the browser parses HTML.
-Without defer, the browser pauses HTML parsing to download and execute the script immediately while still inside the <head>, before any <body> elements exist. Consequently, DOM selection methods return null, breaking event listeners and preventing dynamic features like the footer year and project cards from rendering.
  
3 renderProjects uses textContent rather than innerHTML. What could go wrong with innerHTML if project titles were typed in by visitors?
-innerHTML parses strings as live HTML and JavaScript rather than plain text. If unescaped visitor input were rendered using innerHTML, a malicious user could execute Cross-Site Scripting (XSS) attacks by injecting unauthorized scripts or malicious elements into other visitors' browsers.

4 Your form checks its input with JavaScript. Why will the server still need to validate the same data once the form is connected to one?
-Client-side JavaScript validation can easily be bypassed by users disabling JavaScript, modifying the frontend code, or sending HTTP requests directly via tools like Postman or curl. Because the server cannot trust incoming client data, it must re-validate everything to ensure data integrity and security.

5 Your theme choice follows you from Home to Contact, but not from a double-clicked file to Live Server. Explain this using the idea of an origin.
-localStorage is scoped by origin. Live Server serves files under a consistent local origin, sharing the same storage across pages, whereas double-clicking files opens them under isolated file:// origins with separate storage contexts.

6 Name something duplicated across your HTML pages. What problem does that duplication cause, and how might it be avoided?
-The navigation <header> and <footer> elements are duplicated across all HTML pages. This duplication makes site-wide updates tedious and error-prone since a change requires editing multiple files manually, which can be avoided using server-side includes, static site generators, or component-based architectures.

ByteForge — CSC 216 Lab 2

Building Ideas. Creating Solutions.

1. Project Description

ByteForge is a collaborative, responsive three-page website developed by two Computer Science students as part of CSC 216 Lab 2.

The project demonstrates our understanding of HTML, CSS, JavaScript, Git and GitHub collaboration. It provides information about our team, showcases our projects and allows visitors to contact us through a contact form.

2. Team Details

Role     |      Name          | GitHub Username
Partner A| Lucas Baraka Tinga | lucas-tinga-fakemindsplinter
Partner B| Neymar Osoro       | Neonino

Team Name: ByteForge

Tagline: Building Ideas. Creating Solutions.

3. Repository and Live Website

GitHub Repository: gh repo clone lucas-tinga-fakemindsplinter/team-website

Live Website: https https://github.com/lucas-tinga-fakemindsplinter/team-website.git

4. Project Structure

team-website/
│
├── index.html
├── projects.html
├── contact.html
├── README.md
│
├── css/
│   └── styles.css
│
├── js/
│   └── script.js
│
└── images/
    ├── lucas.jpg
    └── neymar.jpg

5. Technologies Used

- HTML5 — Provides the structure and content of the website.
- CSS3 — Handles styling, layouts and responsiveness.
- JavaScript — Adds interactivity and dynamic functionality.
- Git — Tracks changes and manages project versions.
- GitHub — Hosts the repository and supports collaboration.

6. Website Features

The website contains three main pages:

Home Page

- Introduction to ByteForge.
- Team member profiles.
- Team member photographs.
- Navigation links.
- Responsive navigation menu.
- Light and dark mode.

Projects Page

- Displays team projects.
- Organises projects into categories.
- Allows visitors to filter projects.

Contact Page

- Contact form.
- Name and email fields.
- Message field.
- Input validation.
- Live message character counter.

Additional Features

- Semantic HTML structure.
- Responsive CSS Grid and Flexbox layouts.
- Accessible navigation labels.
- Keyboard-friendly controls.
- Dynamic footer year.
- Persistent theme preference.

7. Team Personalisation

The original website template was personalised to represent ByteForge.

Team Members

Lucas Baraka Tinga — Frontend Developer

Interested in web development, programming and creating user-friendly interfaces.

Neymar Osoro — Backend Developer

Interested in software development, problem-solving and building functional applications.

Team Branding

- Team Name: ByteForge
- Tagline: Building Ideas. Creating Solutions.
- Primary Colour: #2563EB
- Dark Colour: #101827
- Background Colour: #F8FAFC
- Success Colour: #16A34A


1. Extension Challenge

Extension Challenge Completed: Real photos

Description: images

Testing: successful

10. Git and GitHub Collaboration

Git and GitHub were used to manage the development process and track changes.

Our collaboration involved:

- Creating a shared GitHub repository.
- Cloning the repository locally.
- Creating and organising project files.
- Making commits to track changes.
- Pushing changes to GitHub.
- Reviewing and coordinating contributions.

Both partners' contributions and commit authorship should accurately reflect the work each person completed.

11. Driving Log



12. Testing Checklist

The following tests should be completed before submission:

- [ ] Open all three pages using Live Server.
- [ ] Check all navigation links.
- [ ] Validate all HTML pages using the W3C Markup Validator.
- [ ] Check the browser console for errors.
- [ ] Test keyboard navigation using Tab, Shift + Tab, Enter and Space.
- [ ] Test the mobile layout at 375px viewport width.
- [ ] Test dark mode and theme persistence after refreshing.
- [ ] Test every project category filter.
- [ ] Test empty, invalid and valid contact form submissions.
- [ ] Run Lighthouse and aim for an Accessibility score of at least 90.
- [ ] Confirm the GitHub Pages deployment works.

13. Deployment

The website is deployed using GitHub Pages.

Deployment steps:

1. Push the completed project to the main branch.
2. Open the GitHub repository.
3. Navigate to Settings.
4. Select Pages.
5. Choose Deploy from a branch.
6. Select the main branch.
7. Select the /(root) folder.
8. Save the settings.
9. Wait for GitHub Pages to publish the website.
10. Open and test the published website.
