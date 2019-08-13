-- 新建user1表，取经组
create table user1 (
  id int primary key auto_increment,
  user_name varchar(40),
  comment varchar(40),
  mobile varchar(100)
);

-- 新建user2表，悟空的朋友圈
create table user2 (
  id int primary key auto_increment,
  user_name varchar(40),
  comment varchar(40)
);

-- 新建user1_kills表，取经路上杀的妖怪数量
create table user1_kills (
  id int primary key auto_increment,
  user_name varchar(40),
  timestr timestamp default current_timestamp,
  kills int
);

-- 新建user1_equipment表，取经组装备
create table user1_equipment (
  id int auto_increment primary key,
  user_name varchar(40),
  arms varchar(10),
  clothing varchar(10),
  shoe varchar(10)
);

-- 创建tb_sequence表，序列化
create table tb_sequence(id int auto_increment primary key);

-- 插入user1表数据
insert into user1(user_name, comment, mobile) values ('唐僧', '旃檀功德佛', '138245623,021-382349');
insert into user1(user_name, comment, mobile) values ('孙悟空', '斗战胜佛', '159384292,022-483432,+86-392432');
insert into user1(user_name, comment, mobile) values ('猪八戒', '净坛使者', '183208243,055-8234234');
insert into user1(user_name, comment, mobile) values ('沙僧', '金身罗汉', '293842295,098-2383429');
insert into user1(user_name, comment, mobile) values (null, '白龙马', '993267899');

-- 插入user2表数据
insert into user2(user_name, comment) values ('孙悟空', '美猴王');
insert into user2(user_name, comment) values ('牛魔王', '牛哥');
insert into user2(user_name, comment) values ('铁扇公主', '牛夫人');
insert into user2(user_name, comment) values ('菩提老祖', '葡萄');
insert into user2(user_name, comment) values (null, '晶晶');

-- 插入user1_kills表数据
insert into user1_kills(user_name, timestr, kills) values ('孙悟空', timestamp('2013-01-10'), 10);
insert into user1_kills(user_name, timestr, kills) values ('孙悟空', timestamp('2013-02-01'), 2);
insert into user1_kills(user_name, timestr, kills) values ('孙悟空', timestamp('2013-02-05'), 12);
insert into user1_kills(user_name, timestr, kills) values ('孙悟空', timestamp('2013-02-12'), 22);
insert into user1_kills(user_name, timestr, kills) values ('猪八戒', timestamp('2013-01-11'), 20);
insert into user1_kills(user_name, timestr, kills) values ('猪八戒', timestamp('2013-02-07'), 17);
insert into user1_kills(user_name, timestr, kills) values ('猪八戒', timestamp('2013-02-08'), 35);
insert into user1_kills(user_name, timestr, kills) values ('沙僧', timestamp('2013-01-10'), 3);
insert into user1_kills(user_name, timestr, kills) values ('沙僧', timestamp('2013-01-22'), 9);
insert into user1_kills(user_name, timestr, kills) values ('沙僧', timestamp('2013-02-11'), 5);

-- 插入user1_equipment表数据
insert into user1_equipment values (null, '唐僧', '九环锡杖', '锦斓袈裟', '僧鞋');
insert into user1_equipment values (null, '孙悟空', '金箍棒', '梭子黄金甲', '藕丝步云履');
insert into user1_equipment values (null, '猪八戒', '九齿钉耙', '僧衣', '僧鞋');
insert into user1_equipment values (null, '沙僧', '降妖宝杖', '僧衣', '僧鞋');

-- 插入tb_sequence表数据
insert into tb_sequence values(),(),(),(),(),(),(),(),(),();