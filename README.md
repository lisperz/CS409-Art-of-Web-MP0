# MP 0: The Basics
### Due: Tuesday, Sep 9, 11:59PM

## Table of Contents
1. [Assignment](#assignment)
2. [Environment Setup](#environment-setup)
3. [Grading Breakdown](#grading-breakdown)
4. [Rules](#rules)
5. [Submission Details](#submission-details)
6. [Large Language Model (LLM) Usage Policy](#large-language-model-llm-usage-policy)

## Assignment
This assignment designed to help you set up your development environment. You will build a simple card using only HTML/CSS. The card will look like [this example](http://i.imgur.com/aeKrEga.png) except with your own details.

#### Requirements
1. The webpage should mirror the layout shown in the example (colored card on white webpage background.)
2. Elements: You should use at least one of all the following: image (`<img>`), link (`<a>`), paragraph (`<p>`), heading (`<h1>, <h2>, ...`).
3. Layout: The image, heading, and link must all be horizontally centered. The biography text can be either left-aligned or horizontally centered.
4. Styling: All styling must lie within the CSS file. (No inline styling!)
5. The image should have a height and width of 150px.

#### Optional
If you'd like to get some hands-on experience with Javascript before the next MP, you may attempt to recreate [this example](https://cs409-fa25.github.io/fa-25/images/mp0.gif). Although this will not be graded, understanding this early-on will make your life significantly easier for the next MP! :)

To get started, follow the [environment setup](#environment-setup).

## Environment Setup
1. Make sure you have [Node.js](https://nodejs.org/en/) and [git](https://git-scm.com/) installed.
2. Create an account on [GitHub](https://github.com/).
3. Clone this repository:
`git clone https://github.com/cs409-fa25/mp0` or `git@github.com:cs409-fa25/mp0.git`, then `cd mp0`
4. Install dependencies:
`npm install`
5. Start the dev server:
`npm start`

If the web browser does not open automatically, go to `http://localhost:8080/` to view your page. Note that if for some reason your port 8080 is occupied, it will default to 8081. If you can see "Hello World!", then you are all set!

You should now be able to edit the files in the `src` folder and see the changes in your browser (upon saving changes and refreshing your page).

You will need to submit your code as a GitHub repository and deploy it as a website. The steps below will guide you on how to do it.

#### Set Up a Github Repository
You will need to create a GitHub repo and make us collaborators.
1. [Create a public repository on GitHub.](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository) Make sure "Initialize this repository with a README" is **not** checked.
2. Change the remote url for your local mp0 directory to the url of the new public repository you created.
```
git remote rename origin old-origin
git remote add origin git@github.com:<your-github-username>/mp0.git
# run `git remote -v` to check your origin 
```

### Deploying the MP
In order for us to view and grade your MP, you will be deploying your webpage with GitHub's pipelines. This should happen automatically after pushing to your repository, through Github Actions deployment pipeline.

You will need to do some additional to properly deploy the website. There are a few settings you will need to change in your GitHub repository.
1. Set GitHub Pages Deployment Source to Github Actions
   - In your Github repo, go to Settings > Pages > Build and Deployment > Source > Select "GitHub Actions"
<!-- 3. Set GitHub Pages Visibility to **public**, otherwise your deployed url will be randomized. -->

`.github/workflows/static.yml` file automatically makes a GitHub CI pipeline run to build and deploy your code as a website. After the pipeline finishes, your site should be live at `https://<your-github-username>.github.io/mp0`. **It may take up to 10-30 minutes for the site to go live after the first deployment.**

### Pushing Code Changes
Commit and push your local changes to this new repository.
```
git add . # "." adds all changed files, can also add specific files too
git commit -m "[my-commit-message]" # message should be clear and meaningful
git push origin main
```

## Grading Breakdown
This assignment is worth 5% of your final grade. Breakdown is as follows:
1. Correct HTML tags and content (2%)
2. Correct CSS styling (2%)
3. Correct deployment and submission (1%)

## Rules
- This is an individual assignment. No collaboration is permitted.
- It is not permitted to copy/paste code that is not your own. You are, however, free to look at different code sources for inspiration and clarity. All sources (code as well as reading material) that you reference to complete this assignment must be declared in the submission.
- There must be no use of any library.
- There should be no use of inline styling.
- No inline script tags should be used.
- HTML tables cannot be used for layout.
- If you think something you’re doing might not be acceptable, please ask on Piazza.

## Submission Details
After you have completed the assignment and have a deployed website, fill out and submit the form [here](https://docs.google.com/forms/d/e/1FAIpQLSdZfmF6IsyH2hKBegp9voMGalZYFHnALKMQAVg_p7OTA4EILg/viewform?usp=sharing&ouid=103731398038409469401).

## Large Language Model (LLM) Usage Policy

We acknowledge the transformative potential of LLMs in generating code; however, we are still in the nascent stages of understanding how to embed LLMs in developer workflows to write code more efficiently while maintaining quality. Therefore, we will not be teaching students directly how to use LLMs to develop web applications.

As part of this class, we *do* encourage students to experiment with LLM services such as OpenAI's ChatGPT to generate source code for MPs. If LLMs are used to generate code for an MP, students *must* (1) submit their chatlogs along with their source code, and (2) answer survey questions related to their experience using LLMs in the grading form. Failure to do this will be a violation of the academic integrity policy of this course.
