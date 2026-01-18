# Making the Script Executable

Before running the setup script, you must mark it as executable.

From the directory where the script lives, run:

```bash
chmod +x mkback_repo_setup
```

reload the shell if necessary (e.g., `source ~/.bashrc` or `source ~/.zshrc`).
You can then execute it with:

```bash
./mkback_repo_setup my_project_name
```

---

## (Optional) Make the Script Globally Available

If you want to run the script from anywhere (recommended for frequent use), move it to a directory on your `PATH`.

For example:

```bash
mv mkback_repo_setup ~/.local/bin/mkback_repo_setup
```

Ensure that `~/.local/bin` is included in your `PATH` (most modern Linux distributions already include it):

```bash
echo $PATH
```

Once available on your `PATH`, you can run the script from any directory:

```bash
mkback_repo_setup my_project_name
```
