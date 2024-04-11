# rest-api
Contributing
Please read CONTRIBUTING.md for details on our code of conduct, and the process for submitting pull requests to us.

License
This project is licensed under the MIT License - see the LICENSE.md file for details.
""".format(repo_name=repo_name, repo_description=repo_description)

Initialize PyGithub client
g = Github(ACCESS_TOKEN)

Create a new repository
user = g.get_user()
repo = user.create_repo(repo_name, description=repo_description, auto_init=True, license_template="mit")

Create README file in the repository
repo.create_file('README.md', 'Initial commit', readme_content, branch=repo_default_branch)

print("Repository created successfully.")
