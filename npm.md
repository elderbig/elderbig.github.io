# markdown 语法块
```markdown
# 一级标题
## 二级标题
* 小标题
```

# sql 语法块
```sql
select * from tab
where  a = b and c = d
```

# python 语法块
``` python
a = "string"
b = 1
c = [1, 2, 3]
```

# shell 语法
```bash
mkdir ~/script

cnt=`ps -ef|grep docker|wc -l`
[[ $cnt<0 ]] && echo "123"


echo export NLS_LANG='SIMPLIFIED CHINESE_CHINA.ZHS16GBK'>>~/.bashrc
```