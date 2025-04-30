### How To Use

1. Download the Project

Click the **'Download archive'** icon to download the project to your local repository as shown in the image.

<img width="794" alt="Image" src="https://github.com/user-attachments/assets/042bfe89-0305-4330-9709-aeaf12b12002" />

2. Rename the Rules Directory
In your IDE (Cursor, VSCode...), access the project and rename the clinerules folder to match Cline implementation requirements:

```
vibe-coding-rules > .clinerules
```

3. Configure Token Settings
Open Cline settings as shown in the image, then update your setting.json file with the following configuration:

<img width="987" alt="Image" src="https://github.com/user-attachments/assets/d5786828-cdd0-4379-bdd7-b5af53f696fd" />

```
setting.json

{
    "diffEditor.ignoreTrimWhitespace": false,
    "[json]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "javascript.updateImportsOnFileMove.enabled": "always",
    "explorer.confirmDragAndDrop": false,
    "git.confirmSync": false,
    "[markdown]": {
        "diffEditor.ignoreTrimWhitespace": false
    },
    "cline.vsCodeLmModelSelector": {
        
    },
    "cline.allowAutoTruncate": true // 이 부분 추가
}
```

4. Generate Code
Copy and paste the content from **PRD.txt** into the Cline Prompt Input window to generate your code