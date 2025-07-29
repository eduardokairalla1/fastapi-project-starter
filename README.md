# 🚀 FastAPI Project Starter

Jumpstart your development with this production-ready FastAPI project template! This starter kit uses **Copier** to generate a new service with a standardized structure, saving you time on setup and letting you focus on building features.

## ✨ Key Features

  * **Fast & Modern:** Built on the high-performance FastAPI framework.
  * **Ready to Go:** Includes a basic, working API that you can run immediately after creation.
  * **Standardized:** Ensures all your new services follow the same battle-tested structure and best practices.
  * **Easily Updatable:** Keep your projects current with the latest template improvements using a single command.

-----

## 🏁 Getting Started

Follow these two simple steps to generate your new application.

### 1. Install Copier

First, you need **Copier**, the tool that powers this template. The recommended way to install it is with `pipx` to keep its dependencies isolated.

```bash
# First, install pipx (if you don't have it)
python3 -m pip install --user pipx
python3 -m pipx ensurepath

# Then, use pipx to install copier
pipx install copier
```

> **Note:** If you use a different package manager like `dnf` on Fedora or `brew` on macOS, you can also use that to install `pipx`. If you prefer not to use `pipx`, you can install Copier directly with `pip install copier`.

### 2. Create Your New Project

Now you're ready to create your service!

1.  Create a **new and empty** Git repository for your project.

2.  Navigate into the empty project directory in your terminal.

3.  Run the Copier command, pointing it to this template's repository:

```bash
copier copy git+ssh://git@github.com/eduardokairalla1/fastapi-project-starter.git .
```

4.  Copier will then ask you a series of questions to customize your new project. Provide answers that fit your needs:

    ```text
    🎤 What is the project name?
       my-awesome-api
    🎤 What is the project description?
       A modern API for managing widgets.
    🎤 ...
    ```

That's it! All the necessary files and directories for your FastAPI service have been generated. **Commit these files to your repository** and start building your application!

-----

## ⬆️ Updating Your Project

One of the best features of using Copier is that you can easily pull in updates from the template (e.g., security patches, updated CI files, new build scripts).

To update a project that was previously created from this template, navigate to its root directory and run:

```bash
copier update
```

Copier will apply the latest changes from the template while respecting the modifications you've already made. You can then review and commit the updates.

-----

## 🤔 How It Works: The Magic Behind the Curtain

This template works like a "Mad Libs" for your code. It combines your answers with a set of predefined templates to generate a complete project.

  * **`copier.yml`**: This is the master file. It defines all the **questions** Copier will ask you and any other settings.
  * **`.jinja` Files**: Any file ending in `.jinja` (e.g., `README.md.jinja`) is a template. Your answers from the `copier.yml` prompts are used to fill in the blanks inside these files. For example, `{{ name }}` might be replaced with `my-awesome-api`.
  * **Other Files**: Any file or directory that *doesn't* end in `.jinja` is copied over exactly as-is.

This system allows for the creation of highly customized files and even custom file/directory names based on your input.

-----

## 🔧 For Template Developers

This section is for those who want to **contribute to or modify this template itself**.

### Customizing File Content

To create a file whose contents are customized, add the `.jinja` extension to its name (e.g., `main.py.jinja`). Inside the file, use the Jinja2 templating syntax to insert variables that correspond to the questions in `copier.yml`.

**Example:**

```python
# In main.py.jinja
app = FastAPI(title="{{ name }}")
```

### Customizing File & Directory Names

You can also use Jinja2 variables directly in file or directory names. This allows you to, for example, create a main application directory that matches the project's name.

**Example directory structure:**

```
template/
├── pyproject.toml.jinja
└── {{ project_slug }}/
    └── main.py.jinja
```

### 🤝 How to Contribute

Contributions are welcome! If you'd like to improve this template, please follow this general workflow.

1.  **Propose Your Idea (Optional but Recommended):** For major changes or new features, please [open an issue](https://github.com/eduardokairalla1/fastapi-template/issues) first to discuss what you would like to change. For small fixes, feel free to just submit a pull request.

2.  **Develop on a New Branch:** Fork the repository and create a descriptive branch for your feature (e.g., `feat/add-testing-library`). As you work, try to use **atomic commits** for better organization and easier review.

    > *Learn more about atomic commits [in this great article](https://medium.com/@krystalcampioni/advanced-git-guide-part-1-mastering-atomic-commits-and-enforcing-conventional-commits-1be401467a92).*

3.  **Submit a Pull Request:** Once your changes are ready, open a Pull Request against the `main` branch. Provide a clear title and description of the improvements you've made.

4.  **Release a New Version:** After a Pull Request is approved and merged, i will create a new Git tag to release the changes.

    > **Important:** A new version of the template is not "live" or available to users via `copier update` until a new tag (e.g., `v1.1`, `v2.0`) is pushed to the repository. Simply merging to `main` is not enough.

-----

## 📚 Resources

To learn more about the tools used in this template, check out their official documentation:

  * **Copier:** [https://copier.readthedocs.io/](https://copier.readthedocs.io/)
  * **Jinja2:** [https://jinja.palletsprojects.com/](https://jinja.palletsprojects.com/)
