---
title: "IDataReader"
linktitle: "IDataReader"
second_title: "Aspose.Words pour Java"
description: "Fournit un moyen de lire un ou plusieurs flux en lecture seule des ensembles de résultats obtenus en exécutant une commande sur une source de données et est implémenté par les fournisseurs de données du .NET Framework qui accèdent aux bases de données relationnelles en Java."
type: docs
weight: 34
url: /fr/java/com.aspose.words.net.system.data/idatareader/
---

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
```
public interface IDataReader extends System.Data.IDataRecord
```

Fournit un moyen de lire un ou plusieurs flux en lecture seule des ensembles de résultats obtenus en exécutant une commande sur une source de données, et est implémenté par les fournisseurs de données du .NET Framework qui accèdent aux bases de données relationnelles.
## Méthodes

| Méthode | Description |
| --- | --- |
| [close()](#close) | Ferme l'objet [IDataReader](../../com.aspose.words.net.system.data/idatareader/). |
| [getDepth()](#getDepth) | Obtient une valeur indiquant la profondeur d'imbrication de la ligne actuelle. |
| [getRecordsAffected()](#getRecordsAffected) | Obtient le nombre de lignes modifiées, insérées ou supprimées par l'exécution de l'instruction SQL. |
| [getSchemaTable()](#getSchemaTable) | Renvoie un [DataTable](../../com.aspose.words.net.system.data/datatable/) qui décrit les métadonnées des colonnes du [IDataReader](../../com.aspose.words.net.system.data/idatareader/). |
| [isClosed()](#isClosed) | Obtient une valeur indiquant si le lecteur de données est fermé. |
| [nextResult()](#nextResult) | Fait avancer le lecteur de données vers le résultat suivant, lors de la lecture des résultats d'instructions SQL groupées. |
| [read()](#read) | Fait avancer le [IDataReader](../../com.aspose.words.net.system.data/idatareader/) vers l'enregistrement suivant. |
### close() {#close}
```
public abstract void close()
```


Ferme l'objet [IDataReader](../../com.aspose.words.net.system.data/idatareader/).

### getDepth() {#getDepth}
```
public abstract int getDepth()
```


Obtient une valeur indiquant la profondeur d'imbrication de la ligne actuelle.

**Returns:**
int - Le niveau d'imbrication.
### getRecordsAffected() {#getRecordsAffected}
```
public abstract int getRecordsAffected()
```


Obtient le nombre de lignes modifiées, insérées ou supprimées par l'exécution de l'instruction SQL.

**Returns:**
int - Le nombre de lignes modifiées, insérées ou supprimées ; 0 si aucune ligne n'a été affectée ou si l'instruction a échoué ; et -1 pour les instructions SELECT.
### getSchemaTable() {#getSchemaTable}
```
public abstract System.Data.DataTable getSchemaTable()
```


Renvoie un [DataTable](../../com.aspose.words.net.system.data/datatable/) qui décrit les métadonnées des colonnes du [IDataReader](../../com.aspose.words.net.system.data/idatareader/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata.
### isClosed() {#isClosed}
```
public abstract boolean isClosed()
```


Obtient une valeur indiquant si le lecteur de données est fermé.

**Returns:**
boolean - vrai si le lecteur de données est fermé ; sinon, faux.
### nextResult() {#nextResult}
```
public abstract boolean nextResult()
```


Fait avancer le lecteur de données vers le résultat suivant, lors de la lecture des résultats d'instructions SQL groupées.

**Returns:**
boolean - vrai s'il y a plus de lignes ; sinon, faux.
### read() {#read}
```
public abstract boolean read()
```


Fait avancer le [IDataReader](../../com.aspose.words.net.system.data/idatareader/) vers l'enregistrement suivant.

**Returns:**
boolean - vrai s'il y a plus de lignes ; sinon, faux.
