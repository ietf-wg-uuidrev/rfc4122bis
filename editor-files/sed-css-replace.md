### Replace inline CSS with css from /docs/better-rfc.css
``` 
cat draft-ietf-uuidrev-rfc4122bis.html | sed '/<style/{:b;$!N;/style>/!bb;s/.*/<link rel="stylesheet" href="..\/better-rfc.css">/}' > draft-ietf-uuidrev-rfc4122bis-00.html
mv -f draft-ietf-uuidrev-rfc4122bis-00.html docs/draft-00/draft-ietf-uuidrev-rfc4122bis.html
```