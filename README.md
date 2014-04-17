This bookmarklet will take you to a JIRA issue after responding to two prompts.

Steps:
1. Click Bookmarklet in bookmarks bar.
2. Enter the JIRA issue you would like to jump to. Click OK.
3. The browser will prompt you to see if you want to open the issue in the panel next to the scrum board (OK), or as the issue-only view (Cancel).

You will then be redirected to the appropriate URL based on your entries.

To manually add the bookmarklet:
1. Add a new bookmark.
2. Assign it a name.
3. Paste the text* in the oneLinejavascript.txt file into the URL field.
4. I'd suggest putting the bookmark on your bookmarks bar for easy access. (That is after all the point) But feel free to put it wherever you'd like.

Here is the text to enter in the URL field:

<pre>
javascript:var issueNumber=prompt('What issue number are you looking for (AN-###)');console.log(issueNumber);var scrumResponse=confirm('Do you want to see this issue in the Scrum board?');console.log(scrumResponse);{if(scrumResponse==true){window.location=('https://jira.mheducation.com/secure/RapidBoard.jspa?rapidView=329&view=detail&selectedIssue=AN-' + issueNumber);}else{window.location=('https://jira.mheducation.com/browse/AN-' + issueNumber);}}
</pre>