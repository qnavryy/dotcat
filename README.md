# dotcat
A small bash script to manage your **dot**files into **cat**egories. Categories are just subfolders in the dotfile directory.

## Installation
Dotcat always looks for `../dotfiles`, starting from the location of the script. So your dotfile dir might look like:
```
dotcat    # This repository
∟ dotcat
∟ etc.

dotfiles
∟ category0
  ∟ .somedotfile
∟ category1
∟ etc.
∟ category0.sh
∟ etc.
```

## Usage
```
dotcat add <file> <category>               # Add <file> to <category>
```
```
dotcat link [category0 category1 ...]     # Symlink all files in [categories], if no categories are specified
                                            prompt the user for every category
```

## Behavior
If it exists `<category>.sh` is sourced. All files (including symlinks) in the category are symlinked to `$HOME`, non existent directories are created. Conflicting files are overwritten.

## Contributing
Bug reports and pull requests are always welcome.
