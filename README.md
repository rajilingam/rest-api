# rest-api
Contributing
Please read CONTRIBUTING.md for details on our code of conduct, and the process for submitting pull requests to us.

License
This project is licensed under the MIT License - see the LICENSE.md file for details.
""".format(repo_name=repo_name, repo_description=repo_description)
#Heading 1
Initialize PyGithub client
g = Github(ACCESS_TOKEN)

*one star on each side*
_This text is also italic_
Use three asterisks (or three underscores) to wrap your word or phrase.

Create a new repository
user = g.get_user()
repo = user.create_repo(repo_name, description=repo_description, auto_init=True, license_template="mit")

Create README file in the repository
repo.create_file('README.md', 'Initial commit', readme_content, branch=repo_default_branch)

print("Repository created successfully.")

Make sure you have installed PyGithub library (`pip install PyGithub`) and replace `'your_access_token'`, `'your_repo_name'`, and `'Your repository description'` with your actual GitHub access token, repository name, and description, respectively.

This code will create a new GitHub repository with the specified name and description, initializes it with a README file containing some basic content, and uses the MIT License template. You can customize the README content according to your needs.

