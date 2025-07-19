# NCE IT Club (Mentor Hub)
# Code by Nikesh Jung Shrestha
This is a repo containing the backend handling code. These are the activities that has been completed till the recent commit:

1. A virtual environment setup where all the necessities were installed first.
2. I cloned saas-Frontend repo containing the sign in page and used the cloned repo folder as an app-level folder in my Django project.
3. To use the react app as a page to render using django, first I changed the template directory setting using: os.path.join(BASE_DIR, 'saas-Frontend/build').
4. I also changed the static file settings in the settings.py file. (File is in the repo).
5. Then, in urls.py, I included a path that views the page which I have set as a template designed using react. (File is in the repo). 