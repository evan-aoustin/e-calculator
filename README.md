# ⚡ e-Calculator

Calculateur de charge pour véhicule électrique — application web mobile-first, 100 % statique.

## Utilisation

1. Entrez la **distance** de votre trajet (km)
2. Le calculateur affiche instantanément le **pourcentage de charge nécessaire** au départ
3. Ajustez vos paramètres (roue dentée en haut à droite) selon votre véhicule

### Paramètres

| Paramètre | Description | Défaut |
|---|---|---|
| Consommation | kWh / 100 km | 15 |
| Capacité batterie | kWh | 60 |
| Arriver avec | % restant à destination | 10 |

### Formule

```
kWh nécessaires = distance × consommation / 100
% batterie utilisée = kWh nécessaires / capacité × 100
Charge de départ = % batterie utilisée + % d'arrivée souhaité
```

## Déploiement GitHub Pages

Le site est déployé automatiquement via GitHub Actions à chaque push sur `main`.

**Activation initiale (une seule fois) :**

1. Aller dans **Settings → Pages** du dépôt
2. Source : choisir **GitHub Actions**
3. Sauvegarder — le prochain push déploiera le site automatiquement

URL publique : `https://<username>.github.io/e-calculator/`
