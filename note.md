
  * 批量添加用户
\

    #!/bin/bash
    
    i=1
    
    while [ $i -le 20 ]
    do
        useradd user$i
        echo "123456" | passwd --stdin user$i $> /dev/null
        i = `expr $i + 1`
    done

`--stdin` 表示从标准输入中读取密码，上述代码中，也即把"123456"作为每个新添加的用户的密码
`&> /dev/null` 丢弃掉无关的信息



