# Julia environment preparation

## Prepare working folder

1. Create folder
2. Open shell
3. Move to folder

## To activate a Julia project environment, there are several methods available:

1. From the Julia REPL (Package Mode):
- Open the Julia REPL.
- Enter package mode by typing ].
- To activate the project in the current directory (where Project.toml and Manifest.toml are located), type:

```bash
activate .
```

- To activate a project in a specific folder (e.g., MyProject), type:

```bash
activate MyProject
```

To activate a temporary, clean environment, type:

```bash
activate --temp
```

2. When Starting Julia from the Terminal:
Navigate to your project directory in the terminal.
Start Julia and activate the project in the current directory using:

```bash
julia --project=.
```

To activate a project in a specific path, use:

```bash
julia --project=/path/to/my/project
```

3. Programmatically within a Julia Script:
Use the `Pkg.activate()` function.

```bash
using Pkg
Pkg.activate("path/to/project")
```

4. Using the JULIA_PROJECT Environment Variable:
Set the JULIA_PROJECT environment variable to the path of your project before launching Julia. This will automatically activate the specified project when Julia starts.
Choosing the Right Method:

- REPL Package Mode (activate . or activate MyProject): Ideal for interactive development and when you are already within the Julia REPL.
- julia --project=. (from terminal): Convenient for starting a Julia session directly within a project environment from your shell.
- Pkg.activate() (programmatically): Useful for scripts that need to ensure a specific environment is active before running.
- JULIA_PROJECT environment variable: Suitable for consistent project activation in specific workflows or automated setups.
