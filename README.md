# BasicTex-Installation-Guide-on-macOS

## Testing Environment
* macOS 10.14.6
* HomeBrew the package manager


## Installation Guide
1. Install `basictex` from `brew` and make sure you restart the terminal.
```
brew cask install basictex
```
2. Change the repository that is geographically near you. For example, I live in Taipei, so I will use <http://ftp.yzu.edu.tw/CTAN/systems/texlive/tlnet/> as my upstream repository. (P.S. Search <https://ctan.org/mirrors/> to find the best repository for you)
```
sudo tlmgr option repository http://ftp.yzu.edu.tw/CTAN/systems/texlive/tlnet/
```
3. Update `tlmgr` itself.
```
sudo tlmgr update --self
```
4. Then you can start to install whatever packages you miss by this command
```
sudo tlmgr install <your_package_name>
```

## FAQ

1. How can I know what is my desired package name?

Most of the time, if the reported error is like this:
```
! LaTeX Error: File `multirow.sty' not found.

Type X to quit or to roceed, or enter new name. (Default extension: sty)

Enter file name:
```
You probably can directly install it by: `sudo tlmgr install multirow`.

But if it is not the case, then you might need to use other methods to find your desired package name.

Check <https://tex.stackexchange.com/questions/974/why-is-the-mactex-distribution-so-large-is-there-anything-smaller-for-os-x> for more information.
