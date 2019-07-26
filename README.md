# Language: English（Wrote by original author）
## homebrew-php56
In a perfect world such things would not be necessary.

```bash
# *sigh*
brew tap bryonbean/homebrew-php56 git@github.com:bryonbean/homebrew-php56.git 
brew reinstall php@5.6
```
### Update...
My multiple versions of php were originally set up by way of this [great post](https://getgrav.org/blog/macos-mojave-apache-multiple-php-versions). I should have checked it before creating this because the author keeps it up-to-date in spectacular fashion. Sure enough it seems that there is already `homebrew-deprecated` being maintained which services both php@5.6 and php@7.0.

```bash
brew tap exolnet/homebrew-deprecated
```

# Language: 中文
## homebrew-php56 找不到

如若你在安装 php5.6 ```brew install php@56```时遇到下面的报错，那么可以选择往下读。
```
Error: No available formula with the name "php@56" 
==> Searching for a previously deleted formula (in the last month)...
Warning: homebrew/core is shallow clone. To get complete history run:
  git -C "$(brew --repo homebrew/core)" fetch --unshallow

Error: No previously deleted formula found.
==> Searching for similarly named formulae...
This similarly named formula was found:
bryonbean/php56/php@5.6
To install it, run:
  brew install bryonbean/php56/php@5.6
==> Searching taps...
==> Searching taps on GitHub...
Error: No formulae found in taps.
```
### 原因
[官方声明链接](https://brew.sh/2018/01/19/homebrew-1.5.0/)

Homebrew 2018.1.18 更新的 1.5.0 版本宣布将于 2018.3.31 废除 Homebrew/php，也即意味着我们不能够通过```brew install php56```或```brew install php@5.6```来安装指定版本的 PHP。
### 解决方案
执行下面代码
```
brew tap bryonbean/homebrew-php56 git@github.com:bryonbean/homebrew-php56.git
brew reinstall php@5.6
```
