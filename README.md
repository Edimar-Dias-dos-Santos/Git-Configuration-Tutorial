```
# Git Configuration Tutorial

## Setting up User Information

To configure Git with your user information, follow these steps:

1. Set your Git username:
    ```bash
    git config --global user.name "Your Name"
    ```
   Replace `"Your Name"` with your actual name. This name will be associated with your commits.

2. Set your Git email address:
    ```bash
    git config --global user.email "youremail@example.com"
    ```
   Replace `"youremail@example.com"` with your actual email address. This email will be associated with your commits.

## Retrieving User Information

To retrieve your configured user information, you can use the following commands:

- To get your configured username:
    ```bash
    git config --global user.name
    ```

- To get your configured email address:
    ```bash
    git config --global user.email
    ```

## Default Branch Configuration

Git now commonly uses "main" as the default branch name instead of "master". To set this as your default branch for new repositories, use the following command:

```bash
git config --global init.defaultBranch main
```

To retrieve your configured default branch name for new repositories, use:

```bash
git config --global init.defaultBranch
```

## Viewing Global Configuration

To view all your global Git configurations, including user information and default branch settings, use the following command:

```bash
git config --global --list
```

This will display a list of all your global Git configurations.
```
