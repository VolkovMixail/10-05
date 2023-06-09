# Домашнее задание к занятию 10.5 «Балансировка нагрузки. HAProxy/Nginx»
---

### Задание 1

Что такое балансировка нагрузки и зачем она нужна? 

*Приведите ответ в свободной форме.*

#### Термин балансировка нагрузки относится к распределению рабочих нагрузок между несколькими вычислительными ресурсами. Балансировка нагрузки нацелена на оптимизацию использования ресурсов, увеличение пропускной способности, уменьшение времени отклика и предотвращение перегрузки одного ресурса. Кроме того, она может повысить доступность за счет совместного использования рабочей нагрузки в пределах избыточных вычислительных ресурсов.
---

### Задание 2

Чем отличаются алгоритмы балансировки Round Robin и Weighted Round Robin? В каких случаях каждый из них лучше применять? 

*Приведите ответ в свободной форме.*

#### Round Robin - отправляет все запросы последовательно, получил запрос отправил на сервер1, получил еще один отправил на сервер2. Подходит в том случае, если в пуле все сервера одинаковые по мощности.

#### Weighted Round Robin - имеет точно такой же алгоритм как и Round Robin, только он имеет дополнительное свойство мощность (вес) сервера, что озночает что сервер мощнее выдержит и справится с нагрузкой больше чем стандартный, появляется возможность указывать балансировщику, куда направлять трафик.

---

### Задание 3

Установите и запустите Haproxy.

*Приведите скриншот systemctl status haproxy, где будет видно, что Haproxy запущен.*
![](https://github.com/VolkovMixail/10-05/blob/main/imj/Снимок%20экрана%202023-04-12%20в%2013.14.26.png)
---

### Задание 4

Установите и запустите Nginx.

*Приведите скриншот systemctl status nginx, где будет видно, что Nginx запущен.*
![](https://github.com/VolkovMixail/10-05/blob/main/imj/Снимок%20экрана%202023-04-12%20в%2013.07.29.png)
---

### Задание 5

Настройте Nginx на виртуальной машине таким образом, чтобы при запросе:

`curl http://localhost:8088/ping`

он возвращал в ответе строчку: 

"nginx is configured correctly".

*Приведите конфигурации настроенного Nginx сервиса и скриншот результата выполнения команды curl http://localhost:8088/ping.*
![](https://github.com/VolkovMixail/10-05/blob/main/imj/Снимок%20экрана%202023-04-12%20в%2013.18.14.png)
![](https://github.com/VolkovMixail/10-05/blob/main/imj/Снимок%20экрана%202023-04-12%20в%2013.25.07.png)
---
