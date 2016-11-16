# Add color to the terminal in macOS

Edit `.bash_profile`.
```shell
sudo vim ~/.bash_profile
```

Add following lines:
```shell
export TERM=xterm-color
export PS1="\[\033[38;5;166m\]\u\[\033[38;5;15m\]@\[\033[38;5;179m\]\h\[\033[38;5;15m\]:\[\033[38;5;36m\]\w\[\033[38;5;15m\]\\$" # colorize and rearrange bash prompt
export CLICOLOR=1 # enable command line color
export LSCOLORS=ExFxCxDxBxegedabagaced # define colors for ls command
alias ls='ls -GFh' # set default flags for ls
export GREP_OPTIONS='--color=auto' # highlight grep output
```

## Reference
- [>_.bashrc PS1 generator](http://bashrcgenerator.com)
- [LS_COLORS](http://geoff.greer.fm/lscolors/)
- [Simple Tricks to Improve the Terminal Appearance in Mac OS X](http://osxdaily.com/2013/02/05/improve-terminal-appearance-mac-os-x/)
- [[Mac] 터미널 컬러링을 위한 초기 설정](http://theeye.pe.kr/archives/1669)
- [리눅스 터미널 프롬프트 정보와 색상 변경하기](http://blog.saltfactory.net/linux/change-prompt-in-terminal.html)