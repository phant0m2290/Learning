# Deno
Deno is a Javascript and Typescript executor and compiler used in the terminal.\

## Installation

Open a powershell and run `irm https://deno.land/install.ps1 | iex`\
You now should see something like this:
```ps
Deno was installed successfully to C:\Users\phant0m2290\.deno\bin\deno.exe
Run 'deno --help' to get started
Stuck? Join our Discord https://discord.gg/deno
```

You should also install the deno extension for vscode.\
https://marketplace.visualstudio.com/items?itemName=denoland.vscode-deno

## The REPL (Read Eval Process Loop)
A REPL is a command line code executor. Start it by running `deno` in your terminal.\
You can enter code after the `>` and press enter to evaluate it. Everything needs to be on one line tough so you wont be able to make complex functions\
Any variable that is created in the REPL will stay defined so if you define a variable you can use it until you delete the variable or close the REPL.\

To close the REPL you can press `ctrl` + `d` or press `ctrl` + `c` twice.

## Commands

If things are in square brackets **[ ]** its a required argument.
If things are in normal brackets **( )** its an optional argument

### run [file]
Run a Javascript or Typescript file
  
### compile [file]
Turn a Javascript or Typescript file into an executable

### upgrade
Update deno

### task [task]
Execute commands defined in [the deno.json file](#the-denojson-file)

## the deno.json file
The deno.json file is a file where you can define a bunch of settings and tasks. In this case i will go over tasks. For everything else refer to the [deno docs](https://docs.deno.com/runtime/manual/getting_started/configuration_file#configuration-file)

The deno.json file usually looks something like this:
```json
{
    "tasks": {
        "start": "deno run -A .\main.ts",
        "compile": "deno compile -A .\main.ts"
    },
    "imports": {
        "std/": "https://deno.land/std@0.211.0/"
    }
    
}
```

### Tasks
Tasks can be used to quickly run commands.\
Tasks are defined inside the `tasks` object in the `deno.json` file.\
In the following example i define a task called `dev` which will run the `main.ts` file with all permissions using the `-A` argument and watch for changes using the `--watch` argument to any file and restart the execution when changes are detected.
```json
{
    "tasks": {
        "dev": "deno run -A --watch .\main.ts" 
    }
}
```