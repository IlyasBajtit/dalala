# AuBonDeal

# Règles de Gestion pour la Base de Données du site  e commerce AuBonDeal

## Table `users`:
- **Clé primaire (PRIMARY KEY):** `user_uuid` est une clé primaire unique pour identifier chaque utilisateur de manière unique.
- **Contrainte d'unicité (UNIQUE):** La contrainte d'unicité sur `username` garantit que chaque nom d'utilisateur est unique.
- **Contrainte NOT NULL:** Aucune des colonnes ne peut contenir de valeurs NULL.

## Table `products`:
- **Clé primaire (PRIMARY KEY):** `product_uuid` est une clé primaire unique pour identifier chaque produit de manière unique.
- **Contrainte de vérification (CHECK):** Les contraintes de vérification sur `product_price` et `product_quantity` garantissent que ces valeurs sont supérieures ou égales à zéro.
- **Contrainte NOT NULL:** Aucune des colonnes ne peut contenir de valeurs NULL.
- **Contrainte de dates (CHECK):** La contrainte `chk_dates` garantit que la date de création (`created_at`) est antérieure à la date de mise à jour (`updated_at`), si cette dernière est spécifiée.


## Table `orders`:
- **Clé primaire (PRIMARY KEY):** `order_number` est une clé primaire unique pour identifier chaque commande de manière unique.
- **Contrainte de vérification (CHECK):** Les contraintes de vérification sur `order_total_cost_ht` et `order_total_quantity` garantissent que ces valeurs sont supérieures ou égales à zéro.
- **Contrainte NOT NULL:** Aucune des colonnes ne peut contenir de valeurs NULL.