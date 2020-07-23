## Navi-Cheats Repository

Cheatsheets for [navi](https://github.com/denisidoro/navi).

When the user runs navi for the first time, navi prompts to download `.cheat`s from this repository.

In order to add your own repository as a featured cheatsheet repo, please [edit this file](https://github.com/denisidoro/cheats/edit/master/featured_repos.txt). This list will be displayed when `navi repo browse` is run.

## 注

navi 存在一个体验问题，其候选列表排序与 `.cheat` 文件的编辑顺序是没有任何关系的，纯粹就是按命令长度排序，导致若某个关键字对应的候选命令较多时，会陷入查找困难的麻烦，针对此体验问题已向官方提 [issue](https://github.com/denisidoro/navi/issues/369)。

目前的解决方法是在命令末尾后补空格（一般情况下末尾空格是不会对命令本身有影响的），通过空格控制命令长度，继而达到控制候选列表顺序的目的。

另外不建议在 navi 放太多命令，只需要放那些不熟悉、很长很难记的命令即可，命令太多的话又会陷入类似 man 的怪圈。
