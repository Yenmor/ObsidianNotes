题目为文件上传漏洞，那先二话不说写个 php 看看能不能传上去
><img src="https://tuchuangh-1386261756.cos.ap-guangzhou.myqcloud.com/blog/20251214212007794.png"/>

失败，尝试使用 bp 抓包修改文件类型
><img src="https://tuchuangh-1386261756.cos.ap-guangzhou.myqcloud.com/blog/20251214212237416.png"/>

先改后缀名png过一下前端，在抓包把文件类型改回去
><img src="https://tuchuangh-1386261756.cos.ap-guangzhou.myqcloud.com/blog/20251214212740581.png"/>

页面返回：upload success : upload/1765718855.111.php
感情好，上传到哪都不用我找了，直接访问：
><img src="https://tuchuangh-1386261756.cos.ap-guangzhou.myqcloud.com/blog/20251214213022909.png" width=50%>

ls 看起来成功执行了，那再试试访问父目录
显然，父目录就有 flag.php 了

><img src="https://tuchuangh-1386261756.cos.ap-guangzhou.myqcloud.com/blog/20251214213238101.png" width=50%>

phps没法访问，那只能再 cat 一下了，成功
><img src="https://tuchuangh-1386261756.cos.ap-guangzhou.myqcloud.com/blog/20251214213632587.png" width=50%>
