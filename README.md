# Expand tilde notation and $HOME/${HOME} variables in paths

This crate provides a function to expand both, tilde notation, for referring
to home directories, as well as the ${HOME}/$HOME variables, in paths. For example

```
~/foo
```

or

```
$HOME/foo
```

would be expanded to

```
/home/tomjon/foo
```

if the current user's home directory is `/home/tomjon`.

Example:

```
use home_dir::HomeDirExt;

let public_html = "~/public_html".expand_home().unwrap();
```
