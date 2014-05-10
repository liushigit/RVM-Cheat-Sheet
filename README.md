# Basics
[https://rvm.io/rvm/basics]
```bash
$ rvm use 2.1.1 --default
```

## Installing Rubies
```bash
$ rvm list known
$ rvm install 1.9.3
```
### Patch levels
```bash
$ rvm install ruby-1.8.7-p160
```

### Copying single gemsets to new ruby
```bash
$ rvm gemset copy 1.8.6-p420@myapplication rbx-1.2.3@myapplication
```

### Manual migration of all gemsets
```bash
$ rvm migrate 1.8.6-p420 rbx-1.2.3
```

### Updating all gemsets
```bash
$ rvm gemset update
```

## Removing Rubies
```bash
$ rvm remove # Removes the ruby, source files and optional gemsets / archives
$ rvm uninstall # Just removes the ruby - leaves everything else
```

+ You can uninstall one or many rubies. If you're using many, please ensure you seperate the ruby string with a comma, e.g.: 
```bash
$ rvm uninstall ree,1.8.7
```


## Upgrading rubies
```bash
$ rvm upgrade 1.9.2-p136 1.9.2-p180
```


## List
[https://rvm.io/rubies/list]
```bash
$ rvm list
$ rvm list rubies
$ rvm list default
```

## Gemset
```bash
$ rvm gemset create rails222 rails126
=> Gemset 'rails222' created.
=> Gemset 'rails126' created.
```
```bash
$ rvm 1.9.2-head@rails222
$ gem install rails -v 2.2.2
```
+ If you are deploying to a server, or you do not want to wait around for rdoc and ri to install for each gem, you can disable them for gem installs and updates. Just add these two lines to your ~/.gemrc or /etc/gemrc: 
    gem: --no-rdoc --no-ri

### Deleting Gemsets
```bash
$ rvm gemset use albinochipmunk
$ rvm gemset delete albinochipmunk

$ rvm 1.9.2 do gemset delete albinochipmunk
```

### Listing
```bash
$ rvm gemset list
$ rvm gemdir
```

### To list all named gemsets for all interpreters
```bash
$ rvm gemset list_all
```

### To empty a gemset
```bash
$ rvm gemset empty albinochipmunk
```


