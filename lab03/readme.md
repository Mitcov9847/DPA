# Git и GitHub  
---

## 1. Цель работы

Целью лабораторной работы было освоение базовой работы с системой контроля версий Git и взаимодействие с удалённым репозиторием на GitHub.  

Задачи:  
- Инициализация локального Git-репозитория для проекта.  
- Создание файла `.gitignore` для игнорирования временных и сгенерированных файлов.  
- Настройка данных пользователя для Git.  
- Выполнение коммитов изменений в локальном репозитории.  
- Создание удалённого репозитория на GitHub.  
- Связывание локального репозитория с удалённым и загрузка проекта на GitHub.  

---

## 2. Ход работы

### 2.1 Клонирование репозитория DPA  

Сначала был склонирован основной репозиторий `DPA` с GitHub:  

```powershell
git clone https://github.com/Mitcov9847/DPA.git
После выполнения команды локальная копия репозитория появилась в папке C:\Users\mihai\DPA.

<img width="917" height="186" alt="image" src="https://github.com/user-attachments/assets/88189491-6971-44a7-9d3d-9c3cacbe5106" />

2.2 Переход в папку проекта lab03

cd C:\Users\mihai\DPA\lab03

2.3 Инициализация локального Git-репозитория

git init

<img width="663" height="49" alt="image" src="https://github.com/user-attachments/assets/bee4b871-838f-4339-989e-616ecbfd4e70" />

2.4 Создание файла .gitignore

Файл .gitignore был создан для игнорирования временных и сгенерированных файлов:
echo node_modules/ > .gitignore
echo .vscode/ >> .gitignore
echo *.log >> .gitignore
echo __pycache__/ >> .gitignore

<img width="870" height="98" alt="image" src="https://github.com/user-attachments/assets/31b0f53b-5ac6-4709-8164-b05fe107712b" />

2.5 Настройка данных пользователя в Git

git config user.name "Mitcov9847"
git config user.email "malcolmmarvellous@.com"

<img width="1050" height="44" alt="image" src="https://github.com/user-attachments/assets/17d4444f-9969-404c-a140-4a979022e5f2" />

2.6 Добавление файлов и первый коммит

git add .
git commit -m "Первый коммит: добавлены файлы проекта lab03 и .gitignore"

<img width="1067" height="113" alt="image" src="https://github.com/user-attachments/assets/c802396e-2d32-4435-b007-9b5bb0046ed2" />

2.7 Создание удалённого репозитория на GitHub
Был создан новый репозиторий DPA_lab03 на GitHub:

2.8 Связь локального репозитория с GitHub
Удалённый репозиторий был привязан к локальному:

git remote remove origin
git remote add origin https://github.com/Mitcov9847/DPA_lab03.git

<img width="1069" height="128" alt="image" src="https://github.com/user-attachments/assets/842f46d8-247c-4ac7-8677-bb71ba723b5a" />

2.9 Переименование ветки в main

git branch -M main

<img width="808" height="46" alt="image" src="https://github.com/user-attachments/assets/d39d7108-e1e2-4faa-b010-9a5d2d1159ad" />

2.10 Загрузка проекта на GitHub

Так как удалённый репозиторий содержал файлы, был выполнен принудительный пуш:
git push origin main --force

<img width="804" height="205" alt="image" src="https://github.com/user-attachments/assets/89089919-8bf2-46c8-b2b8-6a719b1a9008" />

3. Выводы
Работа с Git позволяет удобно отслеживать изменения в проекте и управлять версиями.
Файл .gitignore помогает исключать ненужные временные файлы из репозитория.
Связывание локального репозитория с GitHub обеспечивает хранение проекта в облаке и доступ с других устройств.
При возникновении конфликта с удалённым репозиторием можно использовать git pull или --force push в зависимости от ситуации.

