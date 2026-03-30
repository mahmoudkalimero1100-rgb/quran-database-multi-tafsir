# 📖 Quran Mega Tafsir Database (SQLite)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
Une base de données complète et optimisée contenant le texte sacré du Coran, l'analyse grammaticale et 7 exégèses (Tafsirs) majeures.

## 📥 Téléchargement
Le fichier étant volumineux (~270 Mo), il n'est pas stocké dans le code source. 
👉 **[Téléchargez la dernière version (.db) ici](https://github.com/mahmoudkalimero1100-rgb/quran-database-multi-tafsir/releases/latest)**

---

## 📊 Structure des données (Table `quran`)

| Colonne | Description |
| :--- | :--- |
| `sora` | Numéro de la sourate (1-114) |
| `aya_no` | Numéro du verset |
| `aya_text_tashkil` | Texte arabe avec voyelles |
| `aya_text_emlaey` | Texte arabe simplifié (Idéal pour les moteurs de recherche) |
| `earab_quran` | Analyse grammaticale détaillée (I'rab) |
| `reasons_of_verses` | Causes de la révélation (Asbab al-Nuzul) |
| `tafseer_ibn_kathir` | Exégèse d'Ibn Kathir |
| `tafseer_tabari` | Exégèse d'At-Tabari |
| `tafseer_saadi` | Exégèse d'As-Saadi |
| `...` | Et 4 autres Tafsirs (Moysar, Bughiu, Alwasit, Ibn Uthaymeen) |

---

## 💻 Exemple d'utilisation (SQL)

Pour récupérer un verset spécifique avec son I'rab et le Tafsir d'Ibn Kathir :

```sql
SELECT aya_text_tashkil, earab_quran, tafseer_ibn_kathir 
FROM quran 
WHERE sora = 1 AND aya_no = 1;
## 📜 Licence & Crédits

### Licence
Ce projet est distribué sous la licence **MIT**. Vous êtes libre d'utiliser cette base de données pour vos projets personnels ou commerciaux, à condition de conserver cette mention de licence.

### Crédits & Sources
Les données contenues dans `quran.db` ont été compilées à partir de sources fiables :
* **Texte du Coran :** [Tanzil.net](https://tanzil.net)
* **Tafsirs & I'rab :** Projet Ayah et sources Open Data.
* **Développement :** Mahmoud (@mahmoudkalimero1100-rgb)
![Downloads](https://img.shields.io/github/downloads/mahmoudkalimero1100-rgb/quran-database-multi-tafsir/total)
