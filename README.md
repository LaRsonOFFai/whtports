# whtports

🔍 A CLI tool to quickly look up network port assignments from the official IANA database (https://www.iana.org/assignments/service-names-port-numbers/).  
Just type a port number — and get its name and description right in your terminal!

## 💡 Examples

whtports 22      # → Port 22: ssh  
whtports 80      # → Port 80: http  
whtports 2049    # → Port 2049: nfs  
whtports 9999    # → Port not found → shows Google search link  

## 🚀 Installation

Make sure you have Python 3.6+ and the `requests` library installed:  
pip install requests

Download the script and make it executable:  
curl -s https://raw.githubusercontent.com/LaRsonOFFai/whtports/main/whtports -o ~/bin/whtports  
chmod +x ~/bin/whtports

If the ~/bin directory doesn’t exist, create it and add it to your $PATH:  
mkdir -p ~/bin  
echo 'export PATH="$HOME/bin:$PATH"' >> ~/.zshrc  
source ~/.zshrc

## ⚠️ After Updating

If you update whtports to a new version (especially after data format changes), please clear the old cache:  
rm -rf ~/.cache/whtports/  
This prevents errors caused by cache format incompatibility.

## 🛠 How It Works

On first run, data is downloaded from the official IANA CSV (https://www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.csv).  
Data is cached in ~/.cache/whtports/iana_ports.json.  
The cache auto-updates every 7 days.  
If a port is not found, a Google search link is provided.

## 📦 Requirements

Python 3.6+  
Library: requests

Install dependencies:  
pip install requests

## 📜 License

This project is licensed under the MIT License — feel free to use and modify it!

Made with ❤️ for hackers, admins, and the curious.

# whtports

🔍 CLI-утилита для быстрого поиска назначения сетевых портов по официальной базе IANA (https://www.iana.org/assignments/service-names-port-numbers/).  
Просто введите номер порта — и получите его имя и назначение прямо в терминале!

## 💡 Примеры

whtports 22      # → Порт 22: ssh  
whtports 80      # → Порт 80: http  
whtports 2049    # → Порт 2049: nfs  
whtports 9999    # → Порт не найден → предложит поиск в Google  

## 🚀 Установка

Убедитесь, что у вас установлен Python 3.6+ и библиотека requests:  
pip install requests

Скачайте скрипт и сделайте его исполняемым:  
curl -s https://raw.githubusercontent.com/LaRsonOFFai/whtports/main/whtports -o ~/bin/whtports  
chmod +x ~/bin/whtports

Если папки ~/bin нет — создайте её и добавьте в $PATH:  
mkdir -p ~/bin  
echo 'export PATH="$HOME/bin:$PATH"' >> ~/.zshrc  
source ~/.zshrc

## ⚠️ После обновления

Если вы обновляете whtports до новой версии (особенно после изменений в формате данных), обязательно удалите старый кэш:  
rm -rf ~/.cache/whtports/  
Это предотвратит ошибки, связанные с несовместимостью формата кэша.

## 🛠 Как это работает?

При первом запуске — данные загружаются с официального CSV IANA (https://www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.csv).  
Данные кэшируются в ~/.cache/whtports/iana_ports.json.  
Кэш автоматически обновляется раз в 7 дней.  
Если порт не найден — выводится ссылка на поиск в Google.

## 📦 Требования

Python 3.6+  
Библиотека: requests

Установка зависимостей:  
pip install requests

## 📜 Лицензия

Этот проект распространяется под лицензией MIT — используйте и модифицируйте свободно!

Сделано с ❤️ для хакеров, админов и любопытных.

