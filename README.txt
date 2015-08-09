
## Setup:
- 1. add folder "vim", folder "tags", file "vimrc", file "ycm_extra_conf.py" in your home directory(cd ~)
- 2. modify the name "vim", "tags", "vimrc", "ycm_extra_conf.py" to ".vim", "tags",.vimrc", ".ycm_extra_conf.py"

Then everything is done.

## Notes:
folder "tags" is used to set C/C++ autocompleting(for standard C++ library and Linux API), it contains "stdcpp.tags" and "sys.tags", if it doesn't work well in your system,
then you can do as follows to create your own "tags".

- 1) cd /usr/include/c++/4.9 (different systems may have different c++ version,so you should use your own version,such as 4.8)
- 2) ctags -R --c++-kinds=+l+x+p --fields=+iaSl --extra=+q --language-force=c++ -f stdcpp.tags
- 3) use stdcpp.tags to replace the one in folder "tags"
- 4) if the C++ version in your system in not 4.9, then you need to update the ".ycm_extra_conf.py",replace the line 59 with your own version.

- 5) cd /usr/include/
- 6) ctags -R --c-kinds=+l+x+p --fields=+lS -I __THROW,__nonnull -f sys.tags
- 7) use sys.tags to replace the one in folder "tags"

