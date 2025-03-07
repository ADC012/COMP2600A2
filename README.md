# COMP2600A2
This will show you how to have your resume on your own static generated site hosted on GitHub.
For people with no knowledge of using Git, static site generators, or forges.    
This is done with Linux operating system.
## Prerequisites
You have a markdown file containing a resume.  
You have a text editor.  
You know how to run commands on the command line.  
You have a GitHub account.
### Software Requirements
- Python  
    - [Download Python here](https://www.python.org/downloads/)  
- Git  
    - [Download git here](https://git-scm.com/downloads)  
- pelican  
    - You can install pelican on the command line with `python -m pip install "pelican[markdown]"`  
- ghp-import  
    - You can install ghp-import on the command line with `python -m pip install ghp-import`

## Instructions
Follow these step-by-step instructions below.  
(The instructions are split up into topics following Etter's recommendation to divide up the writing into bite-sized pieces.)
### Creating a repository on GitHub
1. Click on the + sign at the top right of the page.  
2. Click on "New repository" from the dropdown menu.
3. Enter a name for your repository in the field.
4. Check the box for "Add a README file"
5. Click the green "Create repository" button.  
- **RESULT**: You now have a repository with the name you gave.  

(All command lines are written in code blocks following Etter's recommendation to offset important text with styles.)
### Making a copy of your repository for your local machine
6. Click the green "<> Code" buton found on your repository page.
7. Copy the link shown from the dropdown menu that appeared.
8. Enter `git clone [put the copied link here]` into the command line.
- **RESULT**: You have a copy of your GitHub repository on your local machine.
9. Enter `cd [name of your repository]` into the command line.  
- **RESULT**:  You are now in the directory of your repository.
### Using Pelican to create a website
10. Enter in the command line `pelican-quickstart`  
- **RESULT**: You will receive the prompt `Where do you want to create your web site? [.] `
#### Going through the Pelican quickstart process
11. Hit the enter key.  
- **RESULT**: You will receive the prompt `What will be the title of this web site? `
12. Enter the title you want for your website.  
- **RESULT**: You will receive the prompt `Who will be the author of this web site? `
13. Enter your name.  
- **RESULT**: You will receive the prompt `What will be the default language of this web site? [en]`
14. Hit the enter key.  
- **RESULT**:  You will receive the prompt `Do you want to specify a URL prefix? e.g., https://example.com  (Y/n)`
15. Hit the enter key. 
- **RESULT**: You will receive the prompt `What is your URL prefix? (see above example; no trailing slash)`
16. Enter `https://username.github.io/repositoryName`
    - **username** is your GitHub account name
    - **repositoryName** is the name of your repository  
- **RESULT**: You will receive the prompt `Do you want to enable article pagination? (Y/n)`
17. Hit the enter key. 
18. Hit the enter key again.
- **RESULT**: You will receive the prompt `What is your time zone? [Europe/Rome]` 
19. Enter in the time zone you want in the format given
20. Hit the enter key for the rest of the prompts.  
- **RESULT**:  You will receive a message that your project is availabe in the directory you are in.  You should now have a bunch of new files in your current directory. 
21. Enter `git add .` into the command line.
22. Enter `git commit -am "First commit"`  
- **RESULT**: Your new files are now ready to be added your repository on GitHub which will be done at a later step.

### Adding your resume
21. Open your resume in the text editor of your choice.
22. Add the following at the very top of the file:
    - _title: Resume_
23. Add the following on the next line of the file:
    - -_date: the date_ where the date is in the format _YYYY-MM-DD_
24. Save your resume.
25. Move your resume file into the directory named **content** inside your repository directory on your local machine.
26. Enter `pelican content -s publishconf.py` into the command line.  
- **RESULT**: You have a directory named **output** that contains the files for your newly generated static site.

### Hosting your website on GitHub
27. Enter into the command line `ghp-import output -b gh-pages`
28. Enter into the command line `git push origin gh-pages`  
- **RESULT**: your repository on GitHub will be updated with all the files generated for your static site.
29. Enter the URL you specified for your site into your web browser.  

You should now have your new website with your resume showing up in your web browser.

## Example site
[click here](https://ADC012.github.io/COMP2600A2/)
## Further Resources/Readings
[Markdown guide](https://www.markdownguide.org/)  
[Pelican documentation](https://docs.getpelican.com/en/latest/index.html)  
[Git documentation](https://git-scm.com/doc)  
[Git guide](https://github.com/git-guides)  

## FAQs
#### Why is Markdown better than writing raw HTML?  
Markdown has simpler syntax compared to using raw HTML, making it much easier to read.  
#### Why don't I see any changes to my website when I update the Markdown version of my resume?
The changes you made to the Markdown version of your resume are only for your local machine.  You still need to push your changes to your GitHub repository.


## Credits
**Alex Choy** - *author of this README*  
**Jennifer Hoffman** - *original author of the example resume hosted on the site* 
