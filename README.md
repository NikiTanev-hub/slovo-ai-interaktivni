# Инструкции за настройване и конфигурация на средите и инструментите


## 1. Предварителни изисквания
* **VSCode**
* **Git** - проверявате, като напишете `git --version` в Command Prompt
* **Node.js (v24.21.0 LTS)** - инсталирате [оттук](https://nodejs.org/en/download#:~:text=Windows%20Installer%20(.msi)), след това проверявате с `node --version`. За Linux избирате "v24.21.0 LTS за Linux" и инсталирате с дадения bash код в терминала

## 2. Инсталиране и настройка на Firebase CLI
За бекенд функциите ще използваме Firebase CLI

1. Инсталиране на Firebase през VSCode терминала
Във VSCode отваряте терминала с Ctrl+~ и там изпълнявате:
* За Windows: npm install -g firebase-tools
* За Linux: sudo npm install -g firebase-tools
Накрая задължително проверявате с firebase --version

2. Свързване към Google акаунт
В терминала на VSCode изпълнвате firebase login и се регистрирате с **ЛИЧНИТЕ СИ АКАУНТИ** (звършващи на @gmail.com)

## 3. Инсталиране на Flutter SDK
С Flutter ще разработваме потребителския интерфейс на приложението

* За Windows: [следвайте стъпките тук](https://docs.flutter.dev/install/quick#:~:text=of%20your%20choice.-,Install%20and%20set%20up%20Flutter,-%23)
* За Linux: [инсталирай предварителните пакети с тези команди](https://docs.flutter.dev/install/quick#:~:text=ChromeOS-,Download%20prerequisite%20software,-%23)

Възможно е след инсталацията на Flutter и проверка с flutter doctor в терминала да получите две грешки. Тъй като няма да правим нито мобилно приложение, нито executable файл, можете да напишете следните две команди:
`flutter config --no-enable-windows-desktop`
`flutter config --no-enable-android`

## 4. Създаване на Fork и клониране на repository-то
* Fork в Гитхъб е копие на оригиналното repository във вашите профили. Когато правите промени по своя fork, те не се актуализират автоматично в оригиналното repository. За целта трябва да създадете Pull Request, който впоследствие да бъде одобрен.
**Как се създава Fork?**
1. Отворете страницата на основното репозитори [https://github.com/gRuntolev/slovo-ai-interaktivni/]
2. Натиснете Fork -> Create Fork

* Клонирането означава, че правите копие на репозиторито на вашия локален компютър. Нужно е, защото такаа всички ще боравим с една и съща файлова структура на проекта. **За целта:**
1. От бутона Code горе вдясно на началната страница на repository-то копирате HTTPS линка
2. В Git Bash влизате в директорията, в която искате да се намира проектът (`cd "path"`)
3. Изпълнявате командата `git clone копирания линк`

* За по-лесно изпълнение на работния процес, ви предлагам в Git Bash да изпълните следната команда:
`git remote add upstream Копирания линк`

По този начин ще можем лесно да обновяваме кода си на локалните устройства, използвайки следните команди:

`git checkout main`

`git pull upstream main`
