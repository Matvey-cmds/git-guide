# Инструкция по работе с GIT
## Структура документа 
Документ разбит на главы
1. Создание учетной записи в GitHub
2. Установка Git 
3. Работа с локальным Git
4. Работа с удалённым Git и форками
### 1. Создание учётной записи в GitHub
1. Перейдите на [https://github.com](https://github.com)
2. Нажмите кномку **Sign up** (или "Регистрация")
3. Введите email, придумайте пароль, укажите имя пользователя
4. Подтвердите email (придёт письмо)
5. Готово. Теперь у вас аккаунт на GitHub.
### 2. Установка Git
1. Перейдите на официальный сайт: [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. Скачайте установщик
3. Запустите файл и жмите **Next** на всех шагах
4. В конце установки поставьте галочку **Git Bash Here**
5. `git config --global user.name "Твоё Имя"`
6. `git config --global user.email "твой@email.com"`
7. Готово
### 3 Работа с локальным Git
#### Работа с локальным Git
1. `git init` - создать новый репозиторий, пример:<img width="615" height="57" alt="3" src="https://github.com/user-attachments/assets/ae86984d-d242-47d3-ba55-ee3c9c458838" />
2. `git status` - Показасть состояние файлов, пример:<img width="594" height="126" alt="4" src="https://github.com/user-attachments/assets/475a4bec-c3cb-471c-88c3-67bca8cab708" />
3. `git add .` - Добавить все изменения в staging, пример<img width="728" height="77" alt="6" src="https://github.com/user-attachments/assets/b157f7bd-45a1-46bb-afd8-5a2946fc6fa8" />
4. `git commit -m "сообщение"` - Сохранить изменения, пример:<img width="559" height="92" alt="7" src="https://github.com/user-attachments/assets/33222225-4266-47b0-8086-c1a218f17ebf" />
5. `git log` - История коммитов, пример:<img width="513" height="63" alt="8" src="https://github.com/user-attachments/assets/661db7f7-265b-4b1a-807e-7c13eace1f0c" />
6. `git log --oneline` — короткая история
7.  `git log --oneline -5` — только 5 последних коммитов
8.  `git log --graph --oneline --all` — дерево всех веток
#### Работа с ветками
9. `git branch` - Список веток, пример:<img width="455" height="97" alt="11" src="https://github.com/user-attachments/assets/ed52dda4-ac49-404a-a478-1a4f8c65dda8" />
10. `git checkout -b new-branch` - создать и переключится на ветку, пример:<img width="462" height="131" alt="9" src="https://github.com/user-attachments/assets/4daf894c-6964-4700-91a7-22a458c8e0a0" />
11. `git checkout имя-ветки` - переключится на ветку, пример:<img width="446" height="71" alt="10" src="https://github.com/user-attachments/assets/6229da87-a203-497d-811f-c68c0aad32b5" />
12.  `git merge имя-ветки` - Слить ветку в текущую, пример:<img width="459" height="124" alt="12" src="https://github.com/user-attachments/assets/fc0dc481-1885-4329-84bf-71a2034aeeb3" />
13. `git branch -d имя-ветки`-безопасное удаление (только если ветка слита) <img width="452" height="64" alt="20" src="https://github.com/user-attachments/assets/641f39e9-2330-4786-b6de-35d5416d2cae" />

14. `git branch -D имя-ветки` - принудительное удаление<img width="458" height="65" alt="21" src="https://github.com/user-attachments/assets/b7d2f4d0-a784-4e2b-bd5a-e31696f9ddd9" />

### 4. Работа с удалённым Git и форками
#### Основные команды для работы с удалённым репозиторием 
1. `git remote add origin <url>` - подключить удалённый репозиторий, пример:<img width="604" height="42" alt="13" src="https://github.com/user-attachments/assets/6a7af874-088a-4067-9af7-9a243b3cd3ea" />
2. `git clone <url>` - клонировать репозиторий к себе, пример:<img width="644" height="131" alt="19" src="https://github.com/user-attachments/assets/c9810b39-9a93-4065-a077-42bbbf14071b" />
3. `git push -u origin main` - отправить ветку, пример:<img width="573" height="162" alt="14" src="https://github.com/user-attachments/assets/a98ec95a-ed31-447a-ade8-58d9ace07bf9" />
4. `git push` - отправить изменения на сервер, пример:<img width="452" height="55" alt="18" src="https://github.com/user-attachments/assets/8d8450fd-a0cb-47f7-a0d5-2a7d19fcb9ea" />
5. `git pull` - получить изменения с сервера и слить, пример:<img width="445" height="63" alt="16" src="https://github.com/user-attachments/assets/30a64a1b-a618-409d-b118-93a802da5e43" />
6. `git fetch` - скачать изменения без слияния, пример:<img width="449" height="39" alt="17" src="https://github.com/user-attachments/assets/1b46a8bc-db71-4895-81d0-e4fa41acfeed" />
7. `git remote -v` - показать подключённые удалённые репозитории, пример:<img width="549" height="84" alt="15" src="https://github.com/user-attachments/assets/fc6f1f75-82f1-4cfd-9ee4-fec6924421c7" />
#### Принцип работы с форками
1. На GitHub зайдите на нужный репозиторий и нажмите кнопку **Fork** - у вас появиться копия репозитория в вашем аккаунте
2. склонируйте свой форк:
git clone https: //github.com/Ваш_ник/имя-форка.git
3. Добавьте оригинальный репозиторий как upstream:
git remote add upstream <url>
4. добавьте новую ветку и закомитьте их
5. отправить изменения в свой форк
6. На GitHub в свойм форке нажмите Compare&pulll request создайте Pull Request в оригинальный репозиторий 

