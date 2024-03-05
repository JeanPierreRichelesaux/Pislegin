Создание ключа:
ssh-keygen -t ed25519 -C "имя.фамилия@phystech.edu"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

Добавление ключа в аккаунт:
Github.com -> settings -> SSH and GPG keys -> New SSH key ->
-> вставить результат выполнения cat ~/.ssh/id_ed25519.pub
ssh -T git@github.com

Клонирование репозитория:
git clone <url репозитория ssh на Github>
