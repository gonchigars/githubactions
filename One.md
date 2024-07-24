# GitHub Actions Tutorial for Beginners

## What are GitHub Actions?

Imagine you have a helper robot for your GitHub project. This robot can do tasks for you automatically whenever something happens in your project. That's essentially what GitHub Actions does!

## Key Concepts

1. **Workflow**: Think of this as a recipe for your robot. It tells the robot what to do and when to do it.
2. **Event**: This is the trigger that makes your robot start working. It's like saying, "Hey robot, wake up and do your job!"
3. **Job**: These are the individual tasks in your recipe. Like "mix the ingredients" or "put the cake in the oven".
4. **Action**: These are pre-made helper tools that your robot can use. It's like giving your robot a whisk or a spatula to help with baking.

## Your First Workflow

Let's create a simple workflow that says "Hello, World!" whenever you push code to your repository.

1. In your GitHub repository, create a new folder called `.github/workflows`.
2. Inside this folder, create a new file called `hello-world.yml`.
3. Copy this code into your new file:

```yaml
name: Hello World Workflow

on:
  push:
    branches: [main]

jobs:
  say-hello:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Say Hello
        run: echo "Hello, World!"
```

Let's break this down:

- `name:` This is the name of your workflow (recipe).
- `on:` This tells your robot when to wake up (the event).
- `jobs:` These are the tasks your robot needs to do.
- `runs-on:` This is like telling your robot which kitchen to use.
- `steps:` These are the detailed instructions for your robot.

Now, whenever you push code to your main branch, your robot will wake up and say "Hello, World!"

## Practice Exercise

Try modifying the workflow to say "Hello, [Your Name]!" instead. Can you figure out how to do it?

## Next Steps

In the next tutorial, we'll explore how to use GitHub Actions to automatically run tests on your code every time you make changes.
