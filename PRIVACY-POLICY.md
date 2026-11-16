# Spillguard privacy policy

Last updated: 16 November 2026
Contact: satyarthshukla86@gmail.com / Satyarth Shukla

Spillguard is an app for Atlassian Cloud (Jira and Confluence). It checks text that is posted to customers on Jira Service Management requests and tells you when it copies a restricted Confluence page.

## What it reads
When it runs, Spillguard reads, through Atlassian's own APIs and with the permissions you approve at install:
- Confluence pages and their read restrictions (to find restricted pages),
- Jira comments, summaries and descriptions of requests and the text of Confluence pages that are created or edited (to compare them),
- team and team-member information from the Atlassian Teamwork Graph, and who has Browse permission on a Jira project (to show the owning team and how many people outside it can see a place).

## What it stores
Spillguard stores data in Atlassian's Forge hosted storage for your site, and nowhere else:
- for each restricted page: its title and fingerprints of its text (salted hashes, not the text; anyone who can read the app's stored data could still test guesses against them). The page text itself is not stored;
- the owning teams of the page's space: the team's id, name and number of members;
- a list of alerts: time, work item key or page, titles of the matched restricted pages, what Spillguard did, and the owning team;
- a random value used for hashing and markers of what was already reported.
Spillguard does not store comment text, page text, Atlassian account IDs, names or e-mail addresses. Team members are read from Atlassian while the administrator page loads, to count people, and are not saved. When Spillguard restricts an open Confluence page, it uses the page author's account for that one request and does not keep it.

## What it sends
Spillguard sends no data to any server outside Atlassian. It does not use analytics or advertising. Technical logs written by the app contain request status codes and error messages, not comment or page text.

## Who can see it
The data is only available to the app on your site and to the app developer through Atlassian's tools (for example Forge logs and support requests). Atlassian hosts the storage.

## How long it is kept and how to delete it
- Page fingerprints and team entries are replaced each time an administrator re-indexes.
- Alerts older than 90 days are deleted at each re-index. The other markers are kept until the app is uninstalled.
- When you uninstall Spillguard, Atlassian keeps the app's stored data for 28 days and then deletes it. When a site is permanently deleted, the app data is deleted with it.
- To ask a question about the data, contact satyarthshukla86@gmail.com.

## Personal data
Spillguard does not store personal data (no account IDs, names or e-mail addresses). Page titles and work item keys that appear in alerts belong to your content and can be as sensitive as your content is. Reading a page, comment or team through Atlassian's APIs while the app runs is covered by the permissions you approved at install.

## What it does to Confluence pages
When a newly created or edited open page copies a restricted page, Spillguard adds a read restriction: the page author, the app and the site-admins group keep access (if your site has no group of that name, only the author and the app). Remove the restriction on the page to undo it.

## Changes
We will update this page and its date when the app changes what it stores.
