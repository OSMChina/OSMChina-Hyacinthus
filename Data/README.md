表结构设计

需要考虑的实体

1. 项目，如yamanokatachi就是一个项目
2. 任务，如yamanokatachi beijing就是一个任务

项目和任务分别需要建表，并且给予一个唯一的uuid

而任务的表中需要指明一个任务属于什么项目，进行带where的查询



3. 参与

用户的参与算是一个联系，这个可以单独建一个表，A用户参与了B项目的C任务，主键是参与的uuid，同时包含任务的uuid，用户信息。

用户信息在考虑要不要创一个用户表，直接填uid，还是直接塞json进去作为用户信息，记录头像和主页link

但是在未来接入OSM用户的OAuth以后肯定是要走这个用户分表的形式，并且把现有贡献者和OSM用户关联的。



暂时不需要其他表作为必须表了