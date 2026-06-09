# 🚀 GUIDE DE LANCEMENT - COOPERATIVE MARKET

## 📋 Table des Matières
1. [Prérequis](#prérequis)
2. [Installation Automatique](#installation-automatique)
3. [Installation Manuelle](#installation-manuelle)
4. [Comptes par Défaut](#comptes-par-défaut)
5. [Résolution des Problèmes](#résolution-des-problèmes)

---

## 🔧 Prérequis

Avant de commencer, assurez-vous d'avoir installé:

### Obligatoire:
- **PHP 8.1 ou supérieur** - [Télécharger PHP](https://www.php.net/downloads)
- **Composer** - [Télécharger Composer](https://getcomposer.org/download/)
- **Node.js 16 ou supérieur** - [Télécharger Node.js](https://nodejs.org/)
- **MySQL ou MariaDB** - [Télécharger MySQL](https://dev.mysql.com/downloads/)

### Vérifier les installations:
```bash
php -v        # Doit afficher PHP 8.1+
composer -V   # Doit afficher Composer 2.x
node -v       # Doit afficher v16+
npm -v        # Doit afficher 8+
mysql -V      # Doit afficher MySQL/MariaDB
```

---
## 🔧 Étape 1: XAMPP

Démarrer Apache + MySQL

## 🔧 Étape 2: Base de données

**PHPMyAdmin → Nouvelle DB: cooperative_market**

## 🔧 Étape 3: Backend
```bash
cd C:\xampp\htdocs\cooperative-market\fixed-project\laravel-main
composer install
copy .env.example .env
Modifier .env:
```
env
DB_DATABASE=cooperative_market
DB_USERNAME=root
DB_PASSWORD=
```bash
php artisan key:generate
php artisan migrate --seed
php artisan storage:link
php artisan serve
```
Étape 4: Frontend
```bash
cd C:\xampp\htdocs\cooperative-market\fixed-project\react-main
npm install
npm run dev
```
Étape 5: Connexion
http://localhost:5173



📱 SI VOUS UTILISEZ APACHE XAMPP AU LIEU DE PHP ARTISAN SERVE
Option A: Accès direct via Apache
text
Backend API: http://localhost/cooperative-market/fixed-project/laravel-main/public/api/cooperatives
Frontend:    http://localhost:5173
Option B: Modifier les URLs dans React
Dans tous les fichiers qui appellent l'API, remplacer:

```javascript
// Avant
axios.get('http://localhost:8000/api/...')

// Après (Apache XAMPP)
axios.get('http://localhost/cooperative-market/fixed-project/laravel-main/public/api/...')
```
✅ VÉRIFICATION FINALE
```bash
# 1. XAMPP
Apache: ✅ Running (Port 80)
MySQL:  ✅ Running (Port 3306)
```
# 2. Base de données

PHPMyAdmin: ✅ http://localhost/phpmyadmin
DB Name:    ✅ cooperative_market
Tables:     ✅ users, cooperatives, products

# 3. Backend

Laravel: ✅ http://localhost:8000
API:     ✅ http://localhost:8000/api/cooperatives

# 4. Frontend

React:   ✅ http://localhost:5173


🎉 FÉLICITATIONS!


✅XAMPP: **Apache + MySQL démarrés**

✅Base de données: **cooperative_market**

✅Backend: **Laravel sur port 8000**

✅Frontend: **React sur port 5173**


Bonne chance! 🚀
