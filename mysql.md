# MYSQL

## Se connecter

```bash
mysql -u root -p
```

## Importer un dump

```bash
mysql -u username -p new_database < data-dump.sql
```

## Quelques requêtes utiles

### Afficher toutes les bases

```bash
mysql> SHOW DATABASES;
```

### Créer un base de données

```bash
mysql> CREATE DATABASE [IF NOT EXISTS] db_name;
```

### Afficher toutes les tables d’une base

```bash
mysql> SHOW TABLES FROM mabase;
```

### Créer une base

```bash
mysql> CREATE DATABASE mabase DEFAULT CHARACTER SET utf8 COLLATE utf8_unicode_ci;
```

### Sélectionner une base

```bash
mysql> USE mabase;
```

### Afficher les colonnes d’une table

```bash
mysql> SHOW COLUMNS FROM matable;
```
