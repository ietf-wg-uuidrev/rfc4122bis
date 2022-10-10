### Replace CSS value from make with better CSS.
```
cat draft-ietf-uuidrev-rfc4122bis.html | sed '/<style/{:b;$!N;/style>/!bb;s/.*/<link rel="stylesheet" href="https:\/\/raw.githubusercontent.com\/ietf-wg-uuidrev\/rfc4122bis\/draft-00-merge-1\/editor-files\/better-rfc.css">/}' > draft-ietf-uuidrev-rfc4122bis-00.html
```

### Same but within this folder
``` 
cat draft-ietf-uuidrev-rfc4122bis.html | sed '/<style/{:b;$!N;/style>/!bb;s/.*/<link rel="stylesheet" href="./better-rfc.css">/}' > draft-ietf-uuidrev-rfc4122bis-00.html
```