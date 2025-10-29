curl -s -H "Accept: application/vnd.github.v3+json" https://api.github.com/meta \
  | jq -r '.actions[] | select(test("^[0-9.]+/"))' > github_actions_ips.txt
