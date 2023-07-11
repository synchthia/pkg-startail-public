# STARTAIL Public Maven Repository

## How to Deploy

```bash
MVN_REPO_SERVER_ID="startail-public"
MVN_REPO_USERNAME="<Username for Personal Access Token>"
MVN_REPO_PASSWORD="<Personal Access Token>"


cat <<EOT > ~/.m2/settings.xml
<settings>
  <servers>
    <server>
      <id>${{ env.MVN_REPO_SERVER_ID }}</id>
      <username>${{ secrets.MVN_REPO_USERNAME }}</username>
      <password>${{ secrets.MVN_REPO_PASSWORD }}</password>
    </server>
  </servers>
</settings>
EOT
```
