---
title: "IDataRecord"
linktitle: "IDataRecord"
second_title: "Aspose.Words pour Java"
description: "Fournit un accès aux valeurs des colonnes de chaque ligne pour un DataReader et est implémenté par les fournisseurs de données du .NET Framework qui accèdent aux bases de données relationnelles en Java."
type: docs
weight: 35
url: /fr/java/com.aspose.words.net.system.data/idatarecord/
---
```
public interface IDataRecord
```

Fournit un accès aux valeurs des colonnes de chaque ligne pour un DataReader, et est implémenté par les fournisseurs de données du .NET Framework qui accèdent aux bases de données relationnelles.
## Méthodes

| Méthode | Description |
| --- | --- |
| [get(int i)](#get-int) | Obtient la colonne située à l'index spécifié. |
| [getFieldCount()](#getFieldCount) | Obtient le nombre de colonnes dans la ligne actuelle. |
| [getFieldType(int i)](#getFieldType-int) | Obtient les informations java.lang.Class correspondant au type de java.lang.Object qui serait retourné par [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int). |
| [getName(int i)](#getName-int) | Obtient le nom du champ à rechercher. |
| [getValue(int i)](#getValue-int) | Renvoie la valeur du champ spécifié. |
### get(int i) {#get-int}
```
public abstract Object get(int i)
```


Obtient la colonne située à l'index spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| i | int | L'index basé sur zéro de la colonne à obtenir. |

**Returns:**
java.lang.Object - La colonne située à l'index spécifié en tant que java.lang.Object.
### getFieldCount() {#getFieldCount}
```
public abstract int getFieldCount()
```


Obtient le nombre de colonnes dans la ligne actuelle.

**Returns:**
int - Lorsqu'il n'est pas positionné sur un jeu d'enregistrements valide, 0 ; sinon, le nombre de colonnes dans l'enregistrement actuel. La valeur par défaut est -1.
### getFieldType(int i) {#getFieldType-int}
```
public abstract Class getFieldType(int i)
```


Obtient les informations java.lang.Class correspondant au type de java.lang.Object qui serait retourné par [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| i | int | L'index du champ à rechercher. |

**Returns:**
java.lang.Class - Les informations java.lang.Class correspondant au type de java.lang.Object qui serait retourné par [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int).
### getName(int i) {#getName-int}
```
public abstract String getName(int i)
```


Obtient le nom du champ à rechercher.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| i | int | L'index du champ à rechercher. |

**Returns:**
java.lang.String - Le nom du champ ou la chaîne vide (""), s'il n'y a aucune valeur à retourner.
### getValue(int i) {#getValue-int}
```
public abstract Object getValue(int i)
```


Renvoie la valeur du champ spécifié.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| i | int | L'index du champ à rechercher. |

**Returns:**
java.lang.Object - Le java.lang.Object qui contiendra la valeur du champ au retour.
