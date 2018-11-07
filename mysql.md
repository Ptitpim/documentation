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

### Afficher toutes les tables d’une base

```bash
mysql> SHOW TABLES FROM db_name;
```

### Créer une base

```bash
mysql> CREATE DATABASE db_name DEFAULT CHARACTER SET utf8 COLLATE utf8_unicode_ci;
```

```bash
mysql> CREATE DATABASE [IF NOT EXISTS] db_name;
```

### Supprimer une base

```bash
mysql> DROP DATABASE db_name;
```

### Sélectionner une base

```bash
mysql> USE db_name;
```

### Afficher les colonnes d’une table

```bash
mysql> SHOW COLUMNS FROM matable;
```
