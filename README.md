# Navi-Cheats Repository

Cheatsheets for [navi](https://github.com/denisidoro/navi).

When the user runs navi for the first time, navi prompts to download `.cheat`s from this repository.

In order to add your own repository as a featured cheatsheet repo, please [edit this file](https://github.com/denisidoro/cheats/edit/master/featured_repos.txt). This list will be displayed when `navi repo browse` is run.

## FAQ

### FAQ-1 如何使用本仓库

安装 [navi](https://github.com/denisidoro/navi) 和 [fzf](https://github.com/junegunn/fzf) 后，执行以下命令：

```
navi repo add https://github.com/lyy289065406/navi-cheats
```

然后按需选择 `.cheat` 文件即可。


### FAQ-2 fzf 导致的排序体验问题

由于 [navi](https://github.com/denisidoro/navi) 使用 [fzf](https://github.com/junegunn/fzf) 搜索并回显结果，而 [fzf](https://github.com/junegunn/fzf) 的回显存在一个体验问题，其候选列表排序与 `.cheat` 文件的编辑顺序是没有任何关系的，纯粹就是按命令长度排序（等长则按注释长度），导致若某个关键字对应的候选命令较多时，会陷入查找困难的麻烦，针对此问题的解决方法可见 [issue](https://github.com/denisidoro/navi/issues/369) 。

简而言之，只需要在 `.zshrc` （或 `.bashrc`） 追加以下内容：

```
export FZF_DEFAULT_OPTS="${FZF_DEFAULT_OPTS:-} --no-sort --reverse"
```

通过 `--no-sort` 声明不排序， `--reverse` 声明倒序， 则可使得回显结果与 `.cheat` 文件编辑顺序保持一致。

但这种做法有个副作用就是 navi 的 console 输入会被移动到 terminal 顶部，不过就个人而言还是可以接受这种效果的。

若不期望变成这样，可以只声明 `--no-sort` ， 然后倒序编辑 `.cheat` 文件即可。

> 即使解决了排序问题，也不建议在 navi 放太多命令，只需要放那些不熟悉、很长很难记的命令即可，命令太多的话又会陷入类似 `man` 的怪圈
