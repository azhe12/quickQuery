# quickQuery

@(python)
## Overview
简单的问题搜索小工具.
利用Google对`stackoverflow`进行搜索需要的答案，并选中其中`投票数(votes)`最高的答案，返回到标准输出.

site形如: `https://www.google.com.hk/search?q=site:stackoverflow.com%20query`


url中`query`即为要搜索的答案.


## Usage

```
usage: quickQuery.py [-h] [-p POS] [-a] [-l] [-c] [-n NUM_ANSWERS] [-C]
                     [QUERY [QUERY ...]]

instant coding answers via the command line

positional arguments:
  QUERY                 the question to answer

optional arguments:
  -h, --help            show this help message and exit
  -p POS, --pos POS     select answer in specified position (default: 1)
  -a, --all             display the full text of the answer
  -l, --link            display only the answer link
  -c, --color           enable colorized output
  -n NUM_ANSWERS, --num-answers NUM_ANSWERS
                        number of answers to return
  -C, --clear-cache     clear the cache
```

例如: 搜索netstate的用法， query必须为英文。

`$./quickQuery.py usage of netstate`
```
netstat -np <protocol> | find "port #"
```
