# gitautodeploy
All the files needed to set up git auto deploy.

### 1. API Key
Go to [platform.cloudways.com/api](platform.cloudways.com/api) and generate an API key. Write down the key and email for use later.  
**NOTE:** This step may be unnecessary.

### 2. Add gitautodeploy.php
Upload `gitautodeploy.php` to the server's main directory.

### 3. Add webhook
Go [here](https://platform.cloudways.com/apps/771777/access_detail) and get your application URL. Append `gitautodeploy.php?server_id=SERVERID&app_id=APPID&git_url=git@github.com:elderhs-cs2/gitautodeploy.git&branch_name=master` where `SERVERID` is equal to your server ID, and `APPID` is equal to your app ID, to the end of the application URL and write it down for use later. Go [here](https://github.com/elderhs-cs2/gitautodeploy/settings/hooks/new) and paste the new application URL in the box titled `Payload URL`. Change the `Content type` to `application/json`. Then scroll down and click `Add webhook`.

## 4. Done
Now whenever you deploy a commit to the `master` branch it should automatically be pushed to the Cloudways server. If this did not work you may have to set up [manual git deployment](https://support.cloudways.com/using-git-for-deployment/) first.
