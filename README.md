# Python Google Drive share

Simple Python script to list share details on a Google Drive folders children.

Outputs csv with the id,name,permissions of all the folders/files in the folder, e.g.:
```
id,name,permissions
"AAA1yEGX00COTblhfWjZBNVhjYVk","tes11","owner=me@gmail.com","writer=you@gmail.com","reader=anyone"
```

Requires:
* Python (2.7, pip for dependencies)
* Google API project with oauth client credentials setup and Google Drive API enabled (see [here](https://developers.google.com/drive/v3/web/quickstart/python))

Download your client credentials to `client_secret.json`.

Install dependencies:
```
pip install --upgrade google-api-python-client
```

## Run

First time it runs it will open a browser window for oauth confirmation of Drive access permissions, later calls will use saved credentials in `~/.credentials/google-drive-share.json` delete to reset.

```
# get folderId from URL in Google Drive
python google-drive-share.py --folderId MYFOLDERID > permissions.csv
```

