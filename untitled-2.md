# 用户中心脚本
select * from work_order.work_order where id = 10123860;
select * from work_order.process_info where work_order_template_id = 3137;

select a.* from heimdallr.t_system_role a,work_order.process_info b where  b.role_ids = a.id and b.work_order_template_id = 3137;

select group_concat(b.id) from work_order.process_info a ,work_order.work_order_template b where a.work_order_template_id = b.id and a.role_ids like '%32860%' and b.del_flag = 0


update work_order.process_info set role_ids = 33041 where work_order_template_id in (3051,3128,3137,3142) and role_ids = 32860;

select * from heimdallr.t_system_role where (id = 32860 or name = '星叶艾佳财务经理') and del_flag = 0;
select * from heimdallr.heimdallr_user where user_id = '180429';

select * from heimdallr.sys_role_operate_log where params like '%32860%';

select * from heimdallr.t_system_role_user where role_id = 32860;
