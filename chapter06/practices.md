# 习题

## 第六章

6.1 使用getspnam函数返回的spwd结构体中的sp_pwdp字段访问加密字段，此字段是在/etc/shadow文件中存储的，此函数即是访问此文件的系统接口，操作系统在/etc/passwd中的加密口令字选择使用占位符，不真正的将加密字段显示给普通用户查看。

6.2 直接使用超级用户权限查看/etc/shadow文件中的字段，可以查看加密口令相对应的字段。验证代码见源文件shadow_look.c

6.3 见源程序uname_use.c

6.4 C++11标准规定long类型最少占32位，在我的计算机上，系统使用long int来实现time_t，实际使用64位来表示long类型，因此其取值值范围为 -9223372036854775808～9223372036854775807，由于该值特别大，2900亿年后才会溢出，此时宇宙可能都不存在了。对于某些32位系统或者旧的程序，它们的time_t类型是使用32位int来实现的，而int取值范围为-2147483648～2147483647，我们可以利用localtime( )函数来分解该值，并用strftime( )函数来打印。源程序见time_t_use.c

6.5 见源程序get_time.c
