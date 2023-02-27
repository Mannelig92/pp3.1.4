# pp3.1.4
По поводу n + 1 мне подсказали сделать выборку через квэри в UserRepository, стало на 5 селектов меньше,
Подходит ли это или читал ещё про @BatchSize, можно ли использовать его для решения проблемы?
Там многие селекты повторяются, но я не полностью понимаю должно ли это быть так или в этом и есть ошибка. Например тут:
2023-02-22 19:06:56.059 DEBUG 928 --- [nio-8080-exec-8] org.hibernate.SQL: select roles0_.user_id as user_id1_2_0_, roles0_.roles_id as roles_id2_2_0_, role1_.id as id1_0_1_, role1_.role as role2_0_1_ from users_roles roles0_ inner join roles role1_ on roles0_.roles_id=role1_.id where roles0_.user_id=?
Hibernate: select roles0_.user_id as user_id1_2_0_, roles0_.roles_id as roles_id2_2_0_, role1_.id as id1_0_1_, role1_.role as role2_0_1_ from users_roles roles0_ inner join roles role1_ on roles0_.roles_id=role1_.id where roles0_.user_id=?

    
