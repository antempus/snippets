# Parse JSON to .env structure
```bash
# from stdin
cat $JSON_FILE | jq -r 'keys[] as $k | "\($k)=\(.[$k])"' > .env
```
