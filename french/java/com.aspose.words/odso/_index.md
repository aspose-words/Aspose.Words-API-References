---
title: "Odso"
linktitle: "Odso"
second_title: "Aspose.Words pour Java"
description: "Spécifie les paramètres de l'objet source de données Office ODSO pour une source de données de publipostage en Java."
type: docs
weight: 487
url: /fr/java/com.aspose.words/odso/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Odso implements Cloneable
```

Spécifie les paramètres de l'Office Data Source Object (ODSO) pour une source de données de publipostage.

Pour en savoir plus, consultez l’article de documentation [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

ODSO semble être la « nouvelle » façon dont les versions plus récentes de Microsoft Word préfèrent utiliser lors de la spécification de certains types de sources de données pour un document de publipostage. ODSO est probablement apparu pour la première fois dans Microsoft Word 2000.

L'utilisation de ODSO est mal documentée et la meilleure façon d'apprendre à utiliser les propriétés de cet objet est de créer un document avec une source de données souhaitée manuellement dans Microsoft Word, puis d'ouvrir ce document avec Aspose.Words et d'examiner les propriétés des objets [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) et [MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso). C'est une bonne approche à adopter si vous souhaitez apprendre à configurer programmétiquement une source de données, par exemple.

Vous n'avez généralement pas besoin de créer des objets de cette classe directement car les paramètres ODSO sont toujours disponibles via la propriété [MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso).


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Méthodes

| Méthode | Description |
| --- | --- |
| [deepClone()](#deepClone) | Renvoie un clone profond de cet objet. |
| [getColumnDelimiter()](#getColumnDelimiter) | Spécifie le caractère qui doit être interprété comme le délimiteur de colonne utilisé pour séparer les colonnes dans les sources de données externes. |
| [getDataSource()](#getDataSource) | Spécifie l'emplacement de la source de données externe à connecter à un document pour effectuer la fusion de courrier. |
| [getDataSourceType()](#getDataSourceType) | Spécifie le type de la source de données externe à connecter dans le cadre des informations de connexion ODSO pour cette fusion de courrier. |
| [getFieldMapDatas()](#getFieldMapDatas) | Obtient une collection d'objets qui spécifient comment les colonnes de la source de données externe sont mappées aux noms de champs de fusion prédéfinis dans le document. |
| [getFirstRowContainsColumnNames()](#getFirstRowContainsColumnNames) | Spécifie qu'une application hôte doit traiter la première ligne de données de la source de données externe spécifiée comme une ligne d'en-tête contenant les noms de chaque colonne de la source de données. |
| [getRecipientDatas()](#getRecipientDatas) | Obtient une collection d'objets qui spécifient l'inclusion/exclusion d'enregistrements individuels dans la fusion de courrier. |
| [getTableName()](#getTableName) | Spécifie l'ensemble particulier de données auquel une source doit être connectée au sein d'une source de données externe. |
| [getUdlConnectString()](#getUdlConnectString) | Spécifie la chaîne de connexion Universal Data Link (UDL) utilisée pour se connecter à une source de données externe. |
| [setColumnDelimiter(char value)](#setColumnDelimiter-char) | Spécifie le caractère qui doit être interprété comme le délimiteur de colonne utilisé pour séparer les colonnes dans les sources de données externes. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | Spécifie l'emplacement de la source de données externe à connecter à un document pour effectuer la fusion de courrier. |
| [setDataSourceType(int value)](#setDataSourceType-int) | Spécifie le type de la source de données externe à connecter dans le cadre des informations de connexion ODSO pour cette fusion de courrier. |
| [setFieldMapDatas(OdsoFieldMapDataCollection value)](#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection) | Définit une collection d'objets qui spécifient comment les colonnes de la source de données externe sont mappées aux noms de champs de fusion prédéfinis dans le document. |
| [setFirstRowContainsColumnNames(boolean value)](#setFirstRowContainsColumnNames-boolean) | Spécifie qu'une application hôte doit traiter la première ligne de données de la source de données externe spécifiée comme une ligne d'en-tête contenant les noms de chaque colonne de la source de données. |
| [setRecipientDatas(OdsoRecipientDataCollection value)](#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection) | Définit une collection d'objets qui spécifient l'inclusion/exclusion d'enregistrements individuels dans la fusion de courrier. |
| [setTableName(String value)](#setTableName-java.lang.String) | Spécifie l'ensemble particulier de données auquel une source doit être connectée au sein d'une source de données externe. |
| [setUdlConnectString(String value)](#setUdlConnectString-java.lang.String) | Spécifie la chaîne de connexion Universal Data Link (UDL) utilisée pour se connecter à une source de données externe. |
### deepClone() {#deepClone}
```
public Odso deepClone()
```


Renvoie un clone profond de cet objet.

**Returns:**
[Odso](../../com.aspose.words/odso/)
### getColumnDelimiter() {#getColumnDelimiter}
```
public char getColumnDelimiter()
```


Spécifie le caractère qui doit être interprété comme le délimiteur de colonne utilisé pour séparer les colonnes dans les sources de données externes. La valeur par défaut est 0, ce qui signifie qu'aucun délimiteur de colonne n'est défini.

 **Remarks:** 

RK je n'ai jamais vu cela utilisé.

**Returns:**
char - La valeur  char  correspondante.
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


Spécifie l'emplacement de la source de données externe à connecter à un document pour effectuer la fusion de courrier. La valeur par défaut est une chaîne vide.

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getDataSourceType() {#getDataSourceType}
```
public int getDataSourceType()
```


Spécifie le type de la source de données externe à connecter dans le cadre des informations de connexion ODSO pour cette fusion de courrier. La valeur par défaut est [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT).

 **Remarks:** 

Ce paramètre n'est qu'une suggestion du type de source de données utilisé pour cette fusion de courrier.

**Returns:**
int - La valeur  int  correspondante. La valeur retournée est l'une des constantes [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/).
### getFieldMapDatas() {#getFieldMapDatas}
```
public OdsoFieldMapDataCollection getFieldMapDatas()
```


Obtient une collection d'objets qui spécifient comment les colonnes de la source de données externe sont mappées aux noms de champs de fusion prédéfinis dans le document. Cet objet n'est jamais  null .

**Returns:**
[OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) - A collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document.
### getFirstRowContainsColumnNames() {#getFirstRowContainsColumnNames}
```
public boolean getFirstRowContainsColumnNames()
```


Spécifie qu'une application hôte doit traiter la première ligne de données de la source de données externe spécifiée comme une ligne d'en-tête contenant les noms de chaque colonne de la source de données. La valeur par défaut est  false .

 **Remarks:** 

RK je n'ai jamais vu cela utilisé.

**Returns:**
boolean - La valeur  boolean  correspondante.
### getRecipientDatas() {#getRecipientDatas}
```
public OdsoRecipientDataCollection getRecipientDatas()
```


Obtient une collection d'objets qui spécifient l'inclusion/exclusion d'enregistrements individuels dans la fusion de courrier. Cet objet n'est jamais  null .

**Returns:**
[OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) - A collection of objects that specify inclusion/exclusion of individual records in the mail merge.
### getTableName() {#getTableName}
```
public String getTableName()
```


Spécifie l'ensemble particulier de données auquel une source doit être connectée au sein d'une source de données externe. La valeur par défaut est une chaîne vide.

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getUdlConnectString() {#getUdlConnectString}
```
public String getUdlConnectString()
```


Spécifie la chaîne de connexion Universal Data Link (UDL) utilisée pour se connecter à une source de données externe. La valeur par défaut est une chaîne vide.

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### setColumnDelimiter(char value) {#setColumnDelimiter-char}
```
public void setColumnDelimiter(char value)
```


Spécifie le caractère qui doit être interprété comme le délimiteur de colonne utilisé pour séparer les colonnes dans les sources de données externes. La valeur par défaut est 0, ce qui signifie qu'aucun délimiteur de colonne n'est défini.

 **Remarks:** 

RK je n'ai jamais vu cela utilisé.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | char | La valeur  char  correspondante. |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


Spécifie l'emplacement de la source de données externe à connecter à un document pour effectuer la fusion de courrier. La valeur par défaut est une chaîne vide.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setDataSourceType(int value) {#setDataSourceType-int}
```
public void setDataSourceType(int value)
```


Spécifie le type de la source de données externe à connecter dans le cadre des informations de connexion ODSO pour cette fusion de courrier. La valeur par défaut est [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT).

 **Remarks:** 

Ce paramètre n'est qu'une suggestion du type de source de données utilisé pour cette fusion de courrier.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur  int  correspondante. La valeur doit être l'une des constantes [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/). |

### setFieldMapDatas(OdsoFieldMapDataCollection value) {#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection}
```
public void setFieldMapDatas(OdsoFieldMapDataCollection value)
```


Définit une collection d'objets qui spécifient comment les colonnes de la source de données externe sont mappées aux noms de champs de fusion prédéfinis dans le document. Cet objet n'est jamais  null .

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) | Une collection d'objets qui spécifient comment les colonnes de la source de données externe sont mappées aux noms de champs de fusion prédéfinis dans le document. |

### setFirstRowContainsColumnNames(boolean value) {#setFirstRowContainsColumnNames-boolean}
```
public void setFirstRowContainsColumnNames(boolean value)
```


Spécifie qu'une application hôte doit traiter la première ligne de données de la source de données externe spécifiée comme une ligne d'en-tête contenant les noms de chaque colonne de la source de données. La valeur par défaut est  false .

 **Remarks:** 

RK je n'ai jamais vu cela utilisé.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setRecipientDatas(OdsoRecipientDataCollection value) {#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection}
```
public void setRecipientDatas(OdsoRecipientDataCollection value)
```


Définit une collection d'objets qui spécifient l'inclusion/exclusion d'enregistrements individuels dans la fusion de courrier. Cet objet n'est jamais  null .

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) | Une collection d'objets qui spécifient l'inclusion/exclusion d'enregistrements individuels dans la fusion de courrier. |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


Spécifie l'ensemble particulier de données auquel une source doit être connectée au sein d'une source de données externe. La valeur par défaut est une chaîne vide.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setUdlConnectString(String value) {#setUdlConnectString-java.lang.String}
```
public void setUdlConnectString(String value)
```


Spécifie la chaîne de connexion Universal Data Link (UDL) utilisée pour se connecter à une source de données externe. La valeur par défaut est une chaîne vide.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

