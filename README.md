# 📊 Analyse des déterminants de l'espérance de vie mondiale

Projet d'économétrie — M1 2025/2026  
**Romain Cariou** (Rennes 2) & **Noah Buard** (Rennes 1)

---

## 📋 Présentation du projet

Ce projet vise à identifier et quantifier les facteurs socio-économiques et sanitaires qui expliquent les disparités internationales d'espérance de vie.

**Problématique :** Dans quelle mesure les facteurs socio-économiques et sanitaires expliquent-ils les disparités internationales d'espérance de vie ?

L'analyse porte sur **173 pays** pour l'année **2015**, à partir de données issues de l'OMS, de l'ONU, de l'UNICEF et du PNUD.

---

## 🔬 Hypothèses testées

**H1 — Rôle des facteurs socio-économiques**
L'IDH et le niveau d'éducation moyen (SCOL) sont les principaux déterminants de l'espérance de vie.

**H2 — Impact des risques sanitaires**
La mortalité adulte, la mortalité infantile et la prévalence du VIH/SIDA ont un effet négatif significatif sur l'espérance de vie.

**H3 — Efficacité des politiques de santé publique**
La couverture vaccinale contre la polio reflète la capacité organisationnelle des systèmes de santé et a un effet positif significatif.

---

## 📊 Données

| Variable | Définition | Source |
|----------|-----------|--------|
| `ESP_VIE` | Espérance de vie à la naissance (années) | ONU / OMS |
| `MORT_ADU` | Probabilité de décès entre 15 et 60 ans (pour 1000 hab.) | OMS |
| `MORT_ENF` | Décès d'enfants < 1 an (pour 1000 naissances) | UNICEF |
| `PREV_VIH` | Prévalence VIH/SIDA — 15-49 ans (% population) | ONUSIDA |
| `IDH` | Indice de développement humain (0 à 1) | PNUD |
| `SCOL` | Nombre moyen d'années d'éducation | UNESCO |
| `VACC_POLIO` | Couverture vaccinale polio (% enfants vaccinés) | OMS |
| `STAT_DEV` | Statut de développement (Développé / En développement) | ONU |

---

## 🛠️ Méthode

- **Régression linéaire multiple** par la méthode des **Moindres Carrés Ordinaires (MCO)**
- Analyse descriptive univariée et bivariée
- Tests de robustesse : normalité des résidus, homoscédasticité, multicolinéarité (VIF)
- Analyses complémentaires : transformation des variables, effets non linéaires, effets croisés

---

## 🗂️ Fichiers

- `Projet_Econometrie.Rmd` — code source R Markdown
- `Projet_Econometrie.html` — rapport final rendu
- `datas.csv` — jeu de données

---

## 🚀 Lancement

Ouvrir `Projet_Econometrie.Rmd` dans **RStudio** et knitter le document.

Packages R requis :
```r
install.packages(c("rmdformats", "ggplot2", "dplyr", "corrplot", 
                   "lmtest", "car", "stargazer"))
```

---

## 👤 Auteurs

- **Romain Cariou** — Université Rennes 2
- **Noah Buard** — Université Rennes 1
