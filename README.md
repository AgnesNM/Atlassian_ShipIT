# Forge App

This project is supposed to notify a Jira user if they forget to attach something. 

### User Stories
- A user types in a comment and says they have attached a screenshot
- On clicking the 'save' button on a Jira issue, they should see a modal that tells them that they forgot to attach the screenshot. 


### Requirements

- We need to detect that a new comment has been created (use the Jira comment event - Comment on issue, which means subscribing to the `avi:jira:commented:issue` event on our manifest.yaml)
- We also need to extract our `issueId` from the event payload so that we can identify the issue on which a comment is created or edited.
- We need to be able to read the contents of the comment and check for keywords like `attach` or `screenshot`
- If the keyword exists, a modal pops up - show modal on comment/save


## Edge cases

- Incorporate mentions 
- Eventually send a notification to the user
- Check for file extensions (.jpg, .jpeg, .pdf, .png, .xlxs, .webp...etc) and attachments

## Project set up

 - You need to complete all the steps on [Getting Started](https://developer.atlassian.com/platform/forge/getting-started/) so that you’re familiar with the Forge development process.



