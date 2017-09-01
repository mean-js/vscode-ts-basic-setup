#### Run following command, it will generate package.json
    `npm init`
  
#### Create file .gitignore, and add node_modules in the file, to avoid versioning of node_modules folder.

#### Run following command, it will generate tsconfig.json
    `tsc --init`

#### Important Attributes ares :
    `target`
    `modules`
    `sourceMap`
    `outDir`
    `rootDir`

#### Create source folder (src) for typescript, and bin folder for compiled typescript files with source maps.


#### Next create task configuration, inbuilt feature of VSCode. (This is one of the way to compile typescript program.)
    `Tasks -> Configure Default Build Task`

#### To Run the build task, with watch mode on. 
Option 1, Run at the terminal following command,
--
    `tsc -w  -p "${project_folder}/tsconfig.json"`

Option 2, Add follwing in package.json under scripts tag,
-- 
    `"dev": "tsc -w -p tsconfig.json"`
After adding above script, run following at terminal, 
--
    `npm run dev`

#### To debug typescript program, use create configuration. this will create launch.json. Following is for reference,
    {
        "type": "node",
        "request": "launch",
        "sourceMaps": true,
        "name": "Applicatin Launch",
        "program": "${workspaceRoot}/src/app.ts",
        "outFiles": [
            "${workspaceRoot}/bin/**/*.js"
        ]
    }


#### Refernce, 
    https://stackoverflow.com/questions/31169259/how-to-debug-typescript-files-in-visual-studio-code