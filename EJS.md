EJS is a simple template language which allows javascript processing to be placed into an HTML document.

Template files end with '.ejs'. 

All templates are stored in a view directory.

<%= %>          tag which indicates output declared in the index.js
<% %>           logic used in the ejs document
<%% %%>         comments 
<%-  %>         used to include other template files or HTML that should be rendered

EJS doesn't follow the same scoping rules as Javascript. In order to check whether a variable used in EJS exists, you need to use the 'locals' object to prefix a passed variable. 

