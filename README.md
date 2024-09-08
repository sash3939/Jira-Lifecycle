# Домашнее задание к занятию 7 «Жизненный цикл ПО»

## Подготовка к выполнению

1. Получить бесплатную версию Jira - https://www.atlassian.com/ru/software/jira/work-management/free (скопируйте ссылку в адресную строку). Вы можете воспользоваться любым(в том числе бесплатным vpn сервисом) если сайт у вас недоступен. Кроме того вы можете скачать [docker образ](https://hub.docker.com/r/atlassian/jira-software/#) и запустить на своем хосте self-managed версию jira.
2. Настроить её для своей команды разработки.

   <img width="803" alt="Screen1" src="https://github.com/user-attachments/assets/478b4bec-1fe7-4979-999e-16871bb25b5d">

   <img width="640" alt="Screen2" src="https://github.com/user-attachments/assets/55afbbad-52e4-45fa-8461-ea77ec3b8814">

   <img width="796" alt="Screen3" src="https://github.com/user-attachments/assets/adeb947c-7235-4525-a007-d7b261acafd4">

   
3. Создать доски Kanban и Scrum.

   <img width="1091" alt="Screen4" src="https://github.com/user-attachments/assets/4f6ba504-38cb-4bc1-8ed3-0566fa28742e">

   <img width="1028" alt="Screen5" src="https://github.com/user-attachments/assets/a172b965-b568-49da-bccd-394bbb5b4b21">


4. [Дополнительные инструкции от разработчика Jira](https://support.atlassian.com/jira-cloud-administration/docs/import-and-export-issue-workflows/).

## Основная часть

Необходимо создать собственные workflow для двух типов задач: bug и остальные типы задач. Задачи типа bug должны проходить жизненный цикл:

1. Open -> On reproduce.
2. On reproduce -> Open, Done reproduce.
3. Done reproduce -> On fix.
4. On fix -> On reproduce, Done fix.
5. Done fix -> On test.
6. On test -> On fix, Done.
7. Done -> Closed, Open.

   <img width="374" alt="Workflow_bug" src="https://github.com/user-attachments/assets/93fb5bf9-cc89-4665-b252-8e843ea4c242">


Остальные задачи должны проходить по упрощённому workflow:

1. Open -> On develop.
2. On develop -> Open, Done develop.
3. Done develop -> On test.
4. On test -> On develop, Done.
5. Done -> Closed, Open.

   <img width="154" alt="Workflow_other" src="https://github.com/user-attachments/assets/8d7d2790-7ad2-4a44-b835-b2828f47fd67">

**Что нужно сделать**

1. Создайте задачу с типом bug, попытайтесь провести его по всему workflow до Done.

   <img width="1229" alt="Done_Bug" src="https://github.com/user-attachments/assets/26898fb7-f9d4-4c94-aa71-a86edebf581e">

   <img width="1222" alt="Done_Bug короткий Workflow" src="https://github.com/user-attachments/assets/c5e94294-a8d8-4b9e-90da-7188675535d3">

2. Создайте задачу с типом epic, к ней привяжите несколько задач с типом task, проведите их по всему workflow до Done. 

   <img width="1217" alt="TasksforEpic" src="https://github.com/user-attachments/assets/085692a3-20b1-4096-b780-a28193c52fd1">


3. При проведении обеих задач по статусам используйте kanban. 
4. Верните задачи в статус Open.

   <img width="1011" alt="Status Open" src="https://github.com/user-attachments/assets/96f684e1-6e3e-4c8c-b570-68741b52b030">

5. Перейдите в Scrum, запланируйте новый спринт, состоящий из задач эпика и одного бага, стартуйте спринт, проведите задачи до состояния Closed. Закройте спринт.

   <img width="1213" alt="Sprint" src="https://github.com/user-attachments/assets/aa0e2c79-82de-4670-91aa-313c577acc9a">

   <img width="1223" alt="Begun Sprint" src="https://github.com/user-attachments/assets/37dc637d-c34d-49ca-9484-df91fb466040">

   <img width="959" alt="Report Sprint" src="https://github.com/user-attachments/assets/e3887115-f2f2-44ad-96ba-e79f115f5da9">

6. Если всё отработалось в рамках ожидания — выгрузите схемы workflow для импорта в XML. Файлы с workflow и скриншоты workflow приложите к решению задания.

[bug.xml](https://github.com/sash3939/Jira-Lifecycle/blob/main/JIRA/bug.xml)

[other.xml](https://github.com/sash3939/Jira-Lifecycle/blob/main/JIRA/other.xml)

---

