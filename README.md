# Swing Left / Vote Forward Take Home Test

For the SL/VF Technical Take Home please submit **ONE** of the following that might best showcase your range and expertise:

- [Frontend Test](https://codesandbox.io/s/swing-left-vote-forward-frontend-take-home-test-zkhz7?file=/README.md)
- [Backend Test](#backend-test)
- An **equivalent** open-source code sample

If you choose to submit an equivalent sample we will ask you specific technical questions about it in the subsequent interview stages. We will be interested in the technical tradeoffs you made, the challenges you faced and what you would choose to do differently with additional time.

### Evaluation

Generally, we will be considering the following when evaluating all submissions:

- Does it work?
- Is the code clean and accessible to others?
- Does the code elegantly handle edge case conditions?

## Frontend Test

The frontend test can be taken in CodeSandbox. The link to the frontend test [can be found here](https://codesandbox.io/s/swing-left-vote-forward-frontend-take-home-test-zkhz7?file=/README.md). Please fork the sandbox and send the link to [patrick@swingleft.org](mailto:patrick@swingleft.org) upon completion. If you find CodeSandbox to be inhibiting, please zip your project and send it to [patrick@swingleft.org](mailto:patrick@swingleft.org) and include any neccessary instructions for running the project locally in the README.

## Backend Test

Please include a README that gives instructions for setup required to run your code (if any), and for how to run your submission. We would absolutely love it if you chose to test and run your code in an ephemeral environment like the ones provided by [Gitpod](https://github.com/gitpod-io/template-python-django). This would allow us to guarentee dependency and environment parity with your intended work. If you choose to take this route, feel free to submit a public repo that contains a link to the gitpod.

If you're uncomfortable using an ephemeral environment (no worries!), submit your project as a zip file with a detailed 'Getting Started' section to your README.

Use as many or as few code files as you like, whatever makes the project easiest for you to organize. Send your final submission to [patrick@swingleft.org](mailto:patrick@swingleft.org).

### Instructions

Fetch the semi-structured per-state voter registration deadline info from https://web.archive.org/web/20190209174006/https://www.nonprofitvote.org/voting-in-your-state/voter-registration-deadlines/. A few notes on this resource:

- We’re using an archived version in the interest of consistency, so this data is for 2018.
- You shouldn’t need to use the last column (“Description”)--it’s just an explanation of the general rule that produces the dates in the earlier columns.
- The table is a little unclear about this, but assume that every state that has any registration (i.e. not North Dakota) has registration available both in-person and by-mail. These days may or may not be the same, though! Not every state has online as a valid method.
- Use the language and ORM framework of your choice to parse and store the info for each state into a sqlite database. Internally, we use Python and SQL Alchemy or NodeJS and Knex, depending on our project.
  For each state, store the in-person, by-mail, and online voter registration deadlines, if any.
  Define a schema that makes the most sense to you for representing the data.
  Write tests to validate the core parsing logic and a few states that represent edge cases.
