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


# Authenticating via Token - HTTPS

In this tutorial, we will cover the process of authenticating via token to access GitHub repositories using HTTPS. Authentication via token is a secure and recommended practice for accessing remote repositories, providing an additional layer of security compared to using simple passwords.

## Generate Personal Access Tokens

To get started, follow these steps to generate a personal access token:

1. Access your profile settings on GitHub.
2. Go to "Settings" > "Developer settings" > "Personal access tokens".
3. Select "Tokens (classic)".
4. Click on "Generate new token".
5. Provide a descriptive name for the token and select the necessary scopes according to your needs.
6. Click "Generate token" to create the token.
7. Copy the generated token. **It is important to store it securely as it cannot be retrieved later.**

## View Generated Tokens

You can view all generated personal access tokens by following these steps:

1. Access your profile settings on GitHub.
2. Go to "Settings" > "Developer settings" > "Personal access tokens".
3. Select "Tokens (classic)" to see a list of the generated tokens.

## Save Credentials on the Local Machine

After generating your personal access token, you can configure Git to store your credentials on the local machine. This allows Git to automatically access the token for authentication whenever necessary.

You can set this up using the following Git commands:

```bash
git config --global credential.helper cache
```

This command configures Git to temporarily store your credentials in memory.

```bash
git config --global credential.helper store
```
This command configures Git to store your credentials permanently in an unencrypted text file. **Please note that this may be less secure than using a password management tool.**

## Verify Credential Helper Settings

To verify Git's credential helper settings, you can use the following command:

```bash
git config --global --show-origin credential.helper
```

This command will show the origin of Git's global credential helper configuration.

By following these steps, you'll be ready to authenticate yourself on GitHub repositories using HTTPS securely and effectively.

