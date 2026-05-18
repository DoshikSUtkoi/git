git clone https://github.com/user/style-repo.git
cd style-repo

# Создаём ветку style и переключаемся на неё
git checkout -b style

# Создаём файл .gitignore с содержимым *.log
echo "*.log" > .gitignore

# Добавляем файл в индекс
git add .gitignore

# Коммитим с понятным сообщением
git commit -m "Add .gitignore to ignore *.log files"

# Синхронизация: получаем изменения из удалённого репозитория
git pull origin style --rebase  # или просто git pull, но для новой ветки лучше явно

# Если pull не требуется (ветка новая), просто пушим
git push -u origin style

# В Visual Studio: Team Explorer → Branches → выбрать ветку style → Push
# Затем Team Explorer → Pull Requests → Create Pull Request → style → main → Create
