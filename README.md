# _template
Start here

[General Instructions](https://wiki.archlinux.org/index.php/PKGBUILD) /
[Общие Инструкции](https://wiki.archlinux.org/index.php/PKGBUILD_(%D0%A0%D1%83%D1%81%D1%81%D0%BA%D0%B8%D0%B9))

## Нow to publish

```
makepkg --printsrcinfo > .SRCINFO
git init
git remote add origin ssh://aur@aur.archlinux.org/python-orange-canvas-core.git
git fetch origin
git add PKGBUILD .SRCINFO
git commit -m "welcome"
git push --set-upstream origin master
```

[arch4edu](https://github.com/arch4edu/arch4edu)
