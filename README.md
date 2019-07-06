# redisbackup
redis备份

1.redis-port redis数据备份
     ./redis-port  restore  --input=x/dump.rdb  --target=dst\_host:dst\_port   --auth=dst\_password  [--filterkey="str1|str2|str3"] [--targetdb=DB] [--rewrite] [--bigkeysize=SIZE] [--logfile=REDISPORT.LOG]

    src_host：自建 redis 域名（或者 IP）
    src_port：自建 redis 端口
    src_password：自建 redis 密码
    dst_host：云数据库 redis 域名
    dst_port：云数据库 redis 端口
    dst_password：云数据库 redis 密码
    str1|str2|str3：过滤具有 str1 或 str2 或 str3 的 key
    DB：将同步入云 redis 的 DB
    rewrite：覆盖已经写入的 key
    bigkeysize=SIZE：当写入的 value 大于 SIZE 时，走大 key 写入模式
