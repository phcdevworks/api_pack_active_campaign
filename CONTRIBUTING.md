# Contributing to RubyApiPackActiveCampaign

Thank you for considering contributing to our Active Campaign API integration project! We appreciate your help in improving this project and following these guidelines to maintain code quality and consistency.

## Table of Contents

1. [Project Setup](#project-setup)
2. [Code Standards](#code-standards)
3. [Commit Messages](#commit-messages)
4. [Pull Requests](#pull-requests)
5. [Testing](#testing)
6. [Reporting Issues](#reporting-issues)
7. [Code of Conduct](#code-of-conduct)

## Project Setup

To contribute, please follow these steps to set up the development environment.

### 1. Fork the Repository

First, fork the repository to your GitHub account and clone it locally.

```bash
git clone git@github.com:your-username/ruby_api_pack_active_campaign.git
cd ruby_api_pack_active_campaign
```

### 2. Install Dependencies

Install the required dependencies using `bundler`.

```bash
bundle install
```

### 3. Set Up Active Campaign Credentials

You'll need valid Active Campaign API credentials to run the application. Configure these credentials using the gem's configuration block:

```ruby
RubyApiPackActiveCampaign.configure do |config|
  config.ac_api_url = '<YOUR_ACTIVECAMPAIGN_API_URL>'
  config.ac_api_token = '<YOUR_ACTIVECAMPAIGN_API_KEY>'
end
```

### 4. Run the Tests

Ensure that everything is working by running the test suite.

```bash
bundle exec rspec
```

## Code Standards

We follow Ruby best practices and conventions. Ensure your code adheres to the following:

### 1. Linting

Before submitting any code, run `rubocop` to ensure it adheres to our style guidelines.

### 2. Code Format

```bash
bundle exec rubocop
```

If there are any issues, please resolve them before submitting your pull request.

### 2. Code Format

- **Ruby Version**: Ensure that your code is compatible with Ruby version `>= 3.1.0`.
- **Rails Version**: This project uses Rails `7.x`. Make sure your changes are compatible.
- **Style**: Follow the [Ruby community style guide](https://rubystyle.guide).

### 3. Code Organization

- Place any new services in the `lib/ruby_api_pack_active_campaign/` folder.
- Follow the same structure for methods in service classes and modules, ensuring maintainability across features.
- Keep code DRY (Don’t Repeat Yourself). If something is reusable, refactor it into a shared method or module.

## Commit Messages

A good commit message provides clarity and context for the changes made. Follow these guidelines for commit messages:

- Use present tense: "Add feature" instead of "Added feature".
- Limit the subject line to 50 characters.
- Provide a detailed description if necessary.
- Reference any related issues by number.

### Example Commit Message

```md
Add contact list fetch functionality for Active Campaign API

- Implement `ac_contacts` method in AcContacts class
- Add corresponding tests in `ac_contacts_spec.rb`
- Update API connection class to handle new endpoint

Fixes #15
```

## Pull Requests

When you're ready to submit your changes, please follow these steps:

### 1. Create a Branch

Work on a separate branch that describes the feature or fix.

```bash
git checkout -b feature/add-provider-list
```

### 2. Test Your Changes

Ensure all tests pass before submitting your pull request (PR).

```bash
bundle exec rspec
```

### 3. Submit the PR

When your changes are ready, push your branch to GitHub and open a pull request. Make sure to:

- Provide a descriptive title.
- Reference any related issues.
- Include details of the changes you’ve made and any necessary context.

### 4. Respond to Feedback

The maintainers may request changes. Be ready to address them.

## Testing

Before submitting a PR, ensure the test suite passes. We use RSpec for unit and integration testing. Follow these steps:

### 1. Run Tests

Ensure that the test suite runs and passes.

```bash
bundle exec rspec
```

### 2. Write Tests

Any new functionality should include corresponding tests. Tests are located in the `spec/` folder, and you should follow the structure already in place for:

- **Modules**: Place new tests in `spec/api/`.

### 3. Test Coverage

Ensure that your code is well-covered by tests.

## Reporting Issues

If you encounter any bugs or have feature requests, please [open an issue](https://github.com/phcdevworks/ruby_api_pack_active_campaign/issues). When reporting, please include:

- A clear title and description.
- Steps to reproduce the issue.
- Any relevant logs or error messages.

## Code of Conduct

Please read and follow our [Code of Conduct](https://github.com/phcdevworks/ruby_api_pack_active_campaign/blob/main/CODE_OF_CONDUCT.md) to ensure a welcoming and inclusive environment for everyone.