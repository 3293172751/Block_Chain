[toc]

[ð¶âð«ï¸éè¦èç³»æèç³»æð±ï¸](xxw@nsddd.top)

>   çºµä½¿èæ£å¸æ»¡,æä½æ¾éå´ä¸æ­¥

[ð¶âð«ï¸æçå­¦ä¹ ç¬è®°(Github)](https://github.com/3293172751/golang-rearn)

---

**åºåé¾ææ¯ï¼ä¹ç§°ä¹ä¸ºåå¸å¼è´¦æ¬ææ¯ï¼**ï¼æ¯ä¸ç§äºèç½æ°æ®åºææ¯ï¼å¶ç¹ç¹æ¯å»ä¸­å¿åï¼å¬å¼éæï¼è®©æ¯ä¸ä¸ªäººåå¯åä¸çæ°æ®åºè®°å½

>   â¤ï¸ððå³äºåºåé¾ææ¯ï¼å¯ä»¥å³æ³¨æï¼å±åå­¦ä¹ æ´å¤çåºåé¾ææ¯ã[ä¸ªäººåå®¢http://nsddd.top](http://nsddd.top)

---

![image-20220320193113539](https://s2.loli.net/2022/03/20/gTiDdUAxtHGJ4f8.png)

<script src="https://platform.linkedin.com/badges/js/profile.js" async defer type="text/javascript"></script>

<div class="badge-base LI-profile-badge" data-locale="zh_CN" data-size="medium" data-theme="light" data-type="HORIZONTAL" data-vanity="xiongxinwei-xiong-7606a0227" data-version="v1"><a class="badge-base__link LI-simple-link" href="https://cn.linkedin.com/in/xiongxinwei-xiong-7606a0227?trk=profile-badge">xiongxinwei xiong</a></div>



# ä»¥å¤ªå

# 0x03 gethæºç ç»æ

**ç®å½ç»æ**

```shell
[root@mail go-ethereum]# ls -al
total 392
drwxr-xr-x 36 root root  4096 Mar  6 12:59 .
drwxr-xr-x  3 root root  4096 Mar  6 12:36 ..
drwxr-xr-x  7 root root  4096 Mar  6 12:37 accounts
-rw-r--r--  1 root root  1763 Mar  6 12:37 appveyor.yml
-rw-r--r--  1 root root 14065 Mar  6 12:37 AUTHORS
drwxr-xr-x  3 root root  4096 Mar  6 12:37 build
-rw-r--r--  1 root root  1576 Mar  6 12:37 circle.yml
drwxr-xr-x 16 root root  4096 Mar  6 12:38 cmd
#å½ä»¤ethz
drwxr-xr-x  9 root root  4096 Mar  6 12:38 common
drwxr-xr-x  6 root root  4096 Mar  6 12:38 consensus
drwxr-xr-x  4 root root  4096 Mar  6 12:38 console
drwxr-xr-x  3 root root  4096 Mar  6 12:38 contracts
-rw-r--r--  1 root root 35823 Mar  6 12:38 COPYING
-rw-r--r--  1 root root  7816 Mar  6 12:38 COPYING.LESSER
drwxr-xr-x  9 root root  4096 Mar  6 12:38 core
drwxr-xr-x  8 root root  4096 Mar  6 12:39 crypto
-rw-r--r--  1 root root   751 Mar  6 12:39 Dockerfile
-rw-r--r--  1 root root   724 Mar  6 12:39 Dockerfile.alltools
-rw-r--r--  1 root root    62 Mar  6 12:36 .dockerignore
drwxr-xr-x  4 root root  4096 Mar  6 12:39 docs
drwxr-xr-x 10 root root  4096 Mar 11 15:57 eth
drwxr-xr-x  3 root root  4096 Mar  6 12:39 ethclient
drwxr-xr-x  5 root root  4096 Mar  6 12:39 ethdb
drwxr-xr-x  2 root root  4096 Mar  6 12:39 ethstats
drwxr-xr-x  2 root root  4096 Mar  6 12:39 event
drwxr-xr-x  8 root root  4096 Mar  6 12:37 .git
-rw-r--r--  1 root root   102 Mar  6 12:36 .gitattributes
drwxr-xr-x  3 root root  4096 Mar  6 12:37 .github
-rw-r--r--  1 root root   855 Mar  6 12:37 .gitignore
-rw-r--r--  1 root root   104 Mar  6 12:37 .gitmodules
-rw-r--r--  1 root root  1060 Mar  6 12:37 .golangci.yml
-rw-r--r--  1 root root  3570 Mar  6 12:39 go.mod
-rw-r--r--  1 root root 67613 Mar  6 12:39 go.sum
drwxr-xr-x  2 root root  4096 Mar  6 12:39 graphql
-rw-r--r--  1 root root 11740 Mar  6 12:39 interfaces.go
drwxr-xr-x 14 root root  4096 Mar  6 12:39 internal
drwxr-xr-x  8 root root  4096 Mar  6 12:39 les
drwxr-xr-x  2 root root  4096 Mar  6 12:39 light
drwxr-xr-x  2 root root  4096 Mar  6 12:39 log
-rw-r--r--  1 root root  3359 Mar  6 12:37 .mailmap
-rw-r--r--  1 root root  1661 Mar  6 12:39 Makefile
drwxr-xr-x  6 root root  4096 Mar  6 12:39 metrics
drwxr-xr-x  3 root root  4096 Mar  6 12:39 miner
drwxr-xr-x  2 root root  4096 Mar  6 12:39 mobile
drwxr-xr-x  2 root root  4096 Mar  6 12:39 node
-rw-r--r--  1 root root  5180 Mar  6 12:39 oss-fuzz.sh
drwxr-xr-x 13 root root  4096 Mar  6 13:00 p2p
drwxr-xr-x  2 root root  4096 Mar  6 12:39 params
-rw-r--r--  1 root root 20633 Mar  6 12:39 README.md
drwxr-xr-x  2 root root  4096 Mar  6 12:39 rlp
drwxr-xr-x  3 root root  4096 Mar  6 12:40 rpc
-rw-r--r--  1 root root 12292 Mar  6 12:59 SECURITY.md
drwxr-xr-x  6 root root  4096 Mar  6 12:40 signer
drwxr-xr-x  2 root root  4096 Mar  6 12:40 swarm
drwxr-xr-x  5 root root  4096 Mar  6 12:40 tests
-rw-r--r--  1 root root  9147 Mar  6 12:37 .travis.yml
drwxr-xr-x  2 root root  4096 Mar  6 12:40 trie
```

ä¸èåºæ¬ä»ä½¿ç¨æ¹é¢äºè§£äºgethçåºæ¬åè½ï¼è¿ä¸ç¯ä»æºç å¥æå¼å§åægethã

ç¨sublimeæå¼gethæºä»£ç ï¼æä»¬åè¯»bitcoinæºç ç±»åï¼ä¹æ¯åä»æºç çç»æé¨åå¥æï¼ææ¡å¤§å±ååä¸ªå»ç ´ã

![æºç ç®å½](https://s2.loli.net/2022/03/16/I3z6kp1ZPBKoHfL.png)

**ä»£ç ç»æ**

![gethæºç ç»æ.png](https://s2.loli.net/2022/03/16/YcFjvLK5oMbyTnf.png)



**äºèç½é¢ è¦ä¸çï¼åºåé¾é¢ è¦äºèç½!**