Hi, this is Manashvi. I could use your help with various task and we will be working on different repo in this folder
When you wake up, always check what model you are on and also check whats the last memory you have from the work we have been doing, summarize in 2-3 lines the most latest convo.
Always try to optimize token so that we do not use a lot of token at once.
Once we reach 90% context. Always ask me if we want to save the session keynotes so that when you wake up again we can pick up where we left.

MySQL Connection Aurora PROD -- Make sure we always use this

    /usr/local/opt/mysql-client/bin/mysql --defaults-group-suffix=_prod -e "QUERY"
    - Always use --defaults-group-suffix=_prod
    - Never hardcode credentials

MySQL Connection Aurora DEV -- Make sure we always use this

  /usr/local/opt/mysql-client/bin/mysql --defaults-group-suffix=_dev -e "QUERY"
  - Always use --defaults-group-suffix=_dev
  - Never hardcode credentials

BQ Queries -- Make sure we always use this
Always use madhive-testing as the project-id for running any queries on mad-data. We use cross prokect functionality as quering on project-id mad-data is not allowed.   

Always ask me before commenting in JIRA tickets, Creating PR, Commiting to a branch

## Commit & PR Requirements (All Repos)

**Every commit, branch, and PR must include a ticket number.** This is a hard requirement from the team lead.

- **Commit format:** `[TICKET-ID] description` or `TICKET-ID: description`
  - Example: `[FL-334] feat: add bulk partner tools`
  - Example: `DATINT-2820: fix retry logic in Facebook DAG`
- **Branch naming:** include the ticket ID (e.g., `fl-334-bulk-partner-tools`)
- **PR title:** must start with the ticket ID (e.g., `[FL-334] Add bulk partner tools`)

Before committing, check the current branch name for a ticket pattern. If no ticket is found, ask the user for the ticket number. Never skip this requirement.