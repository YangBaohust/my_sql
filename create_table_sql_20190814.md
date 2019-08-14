-- 新建salary，取经四人工资表
create table salary(
id int primary key auto_increment,
user_name varchar(64),
comment varchar(64),
money int);

-- 插入相关数据
insert into salary(user_name, comment, money) 
values('唐僧', '旃檀功德佛', 35000)
,('孙悟空', '斗战胜佛', 28000)
,('猪八戒', '净坛使者', 15000)
,('沙僧', '金身罗汉', 8000);

-- 新建tax，税率表
create table tax(
id int primary key auto_increment,
low int,
high int,
rate decimal(10,2));

-- 插入相关数据
insert into tax(low, high, rate)
values(0, 1500, 0.03),
(1500, 4500, 0.1),
(4500, 9000, 0.2),
(9000, 35000, 0.25),
(35000, 55000, 0.3),
(55000, 1000000, 0.35);


