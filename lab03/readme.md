# Отчёт по работе с Git и GitHub  
**Студент:** Евгений Митков  
**Проект:** lab03  
**Дата выполнения:** 30.09.2025  

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

2.2 Переход в папку проекта lab03
powershell
Копировать код
cd C:\Users\mihai\DPA\lab03
2.3 Инициализация локального Git-репозитория
powershell
Копировать код
git init
2.4 Создание файла .gitignore
Файл .gitignore был создан для игнорирования временных и сгенерированных файлов:

powershell
Копировать код
echo node_modules/ > .gitignore
echo .vscode/ >> .gitignore
echo *.log >> .gitignore
echo __pycache__/ >> .gitignore
2.5 Настройка данных пользователя в Git
powershell
Копировать код
git config user.name "Евгений Митков"
git config user.email "mihai@example.com"
Проверить настройки можно командой:

powershell
Копировать код
git config --list
2.6 Добавление файлов и первый коммит
powershell
Копировать код
git add .
git commit -m "Первый коммит: добавлены файлы проекта lab03 и .gitignore"
Пример вывода:

sql
Копировать код
[master (root-commit) f85ceec] Первый коммит: добавлены файлы проекта lab03 и .gitignore
 2 files changed, 1 insertion(+)
 create mode 100644 .gitignore
 create mode 100644 readme.md
2.7 Создание удалённого репозитория на GitHub
Был создан новый репозиторий DPA_lab03 на GitHub:

Тип: Public

Пустой (без README и .gitignore)

2.8 Связь локального репозитория с GitHub
Удалённый репозиторий был привязан к локальному:

powershell
Копировать код
git remote remove origin
git remote add origin https://github.com/Mitcov9847/DPA_lab03.git
Проверка связи:

powershell
Копировать код
git remote -v
Вывод:

perl
Копировать код
origin  https://github.com/Mitcov9847/DPA_lab03.git (fetch)
origin  https://github.com/Mitcov9847/DPA_lab03.git (push)
2.9 Переименование ветки в main
powershell
Копировать код
git branch -M main
2.10 Загрузка проекта на GitHub
Так как удалённый репозиторий содержал файлы, был выполнен принудительный пуш:

powershell
Копировать код
git push origin main --force
Пример вывода:

bash
Копировать код
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 397 bytes | 397.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
+ 592c13b...f85ceec main -> main (forced update)
3. Выводы
Работа с Git позволяет удобно отслеживать изменения в проекте и управлять версиями.

Файл .gitignore помогает исключать ненужные временные файлы из репозитория.

Связывание локального репозитория с GitHub обеспечивает хранение проекта в облаке и доступ с других устройств.

При возникновении конфликта с удалённым репозиторием можно использовать git pull или --force push в зависимости от ситуации.

Все цели лабораторной работы достигнуты: локальный репозиторий был создан, файлы проекта закоммичены и успешно загружены на GitHub в отдельный репозиторий DPA_lab03.


