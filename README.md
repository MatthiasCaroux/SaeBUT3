SaeBUT3
--- DOCKER ---
🚀 Guide de démarrage de notre App React Native + Django
Pré-requis
Docker Desktop installé et lancé
Git pour cloner le projet
L'app Expo Go sur ton téléphone
🔧 Installation rapide (première fois)
Clone le projet :
git clone [url-du-repo]
cd mon-projet
Lance tout d'un coup :
docker-compose up --build
Attends que tout se lance (peut prendre 2-3 minutes la première fois)

Vérifie que ça marche :

API Django : http://localhost:8000
Expo Dev Tools : http://localhost:19000
📱 Test sur téléphone
Ouvre l'app Expo Go
Scanne le QR code qui apparaît dans ton terminal
L'app se lance sur ton téléphone !
🔄 Utilisation quotidienne
# Lancer le projet
docker-compose up

# Arrêter le projet
docker-compose down

# Voir les logs
docker-compose logs -f

# Reconstruire si tu changes les Dockerfile
docker-compose up --build
🐛 Dépannage
Problème : "Port already in use"

docker-compose down
docker-compose up
Problème : Les changements n'apparaissent pas

docker-compose restart frontend
Problème : Base de données corrompue

docker-compose down -v
docker-compose up --build
📂 Structure du projet
mon-projet/
├── backend/         # API Django
├── frontend/        # App React Native
├── docker-compose.yml
└── README.md
💡 Tips
Laisse Docker Desktop ouvert pendant le développement
Les changements de code sont automatiquement pris en compte (hot reload)
Si tu changes les packages, relance avec --build
