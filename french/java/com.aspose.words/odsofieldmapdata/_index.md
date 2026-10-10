---
title: "OdsoFieldMapData"
linktitle: "OdsoFieldMapData"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment une colonne de la source de données externe doit être mappée aux champs de fusion prédéfinis du document en Java."
type: docs
weight: 489
url: /fr/java/com.aspose.words/odsofieldmapdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoFieldMapData implements Cloneable
```

Spécifie comment une colonne de la source de données externe doit être mappée aux champs de fusion prédéfinis du document.

Pour en savoir plus, consultez l’article de documentation [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Microsoft Word fournit certains noms de champs de fusion prédéfinis qu’il permet d’insérer dans un document en tant que MERGEFIELD ou d’utiliser dans les champs ADDRESSBLOCK ou GREETINGLINE. Les informations spécifiées dans [OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/) permettent de mapper une colonne de la source de données externe à un seul champ de fusion prédéfini.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Méthodes

| Méthode | Description |
| --- | --- |
| [deepClone()](#deepClone) | Renvoie un clone profond de cet objet. |
| [getColumn()](#getColumn) | Spécifie l’indice zéro‑bas de la colonne dans une source de données externe qui doit être mappé au nom local d’un champ MERGEFIELD spécifique. |
| [getMappedName()](#getMappedName) | Spécifie le nom du champ de fusion prédéfini qui doit être mappé au numéro de colonne indiqué par la propriété [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) dans ce mappage de champ. |
| [getName()](#getName) | Spécifie le nom de la colonne dans une source de données externe pour la colonne dont l’indice est indiqué par la propriété [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). |
| [getType()](#getType) | Indique si un champ de fusion donné a été mappé à une colonne de la source de données externe spécifiée ou non. |
| [setColumn(int value)](#setColumn-int) | Spécifie l’indice zéro‑bas de la colonne dans une source de données externe qui doit être mappé au nom local d’un champ MERGEFIELD spécifique. |
| [setMappedName(String value)](#setMappedName-java.lang.String) | Spécifie le nom du champ de fusion prédéfini qui doit être mappé au numéro de colonne indiqué par la propriété [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) dans ce mappage de champ. |
| [setName(String value)](#setName-java.lang.String) | Spécifie le nom de la colonne dans une source de données externe pour la colonne dont l’indice est indiqué par la propriété [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). |
| [setType(int value)](#setType-int) | Indique si un champ de fusion donné a été mappé à une colonne de la source de données externe spécifiée ou non. |
### deepClone() {#deepClone}
```
public OdsoFieldMapData deepClone()
```


Renvoie un clone profond de cet objet.

**Returns:**
[OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/)
### getColumn() {#getColumn}
```
public int getColumn()
```


Spécifie l’indice zéro‑bas de la colonne dans une source de données externe qui doit être mappé au nom local d’un champ MERGEFIELD spécifique. La valeur par défaut est 0.

**Returns:**
int - La valeur int correspondante.
### getMappedName() {#getMappedName}
```
public String getMappedName()
```


Spécifie le nom du champ de fusion prédéfini qui doit être mappé au numéro de colonne indiqué par la propriété [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) dans ce mappage de champ. La valeur par défaut est une chaîne vide.

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getName() {#getName}
```
public String getName()
```


Spécifie le nom de la colonne dans une source de données externe pour la colonne dont l’indice est indiqué par la propriété [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). La valeur par défaut est une chaîne vide.

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### getType() {#getType}
```
public int getType()
```


Indique si un champ de fusion donné a été mappé à une colonne de la source de données externe spécifiée ou non. La valeur par défaut est [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/\#DEFAULT).

**Returns:**
int - La valeur  int  correspondante. La valeur retournée est l’une des constantes [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/).
### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


Spécifie l’indice zéro‑bas de la colonne dans une source de données externe qui doit être mappé au nom local d’un champ MERGEFIELD spécifique. La valeur par défaut est 0.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La valeur  int  correspondante. |

### setMappedName(String value) {#setMappedName-java.lang.String}
```
public void setMappedName(String value)
```


Spécifie le nom du champ de fusion prédéfini qui doit être mappé au numéro de colonne indiqué par la propriété [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) dans ce mappage de champ. La valeur par défaut est une chaîne vide.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Spécifie le nom de la colonne dans une source de données externe pour la colonne dont l’indice est indiqué par la propriété [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). La valeur par défaut est une chaîne vide.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


Indique si un champ de fusion donné a été mappé à une colonne de la source de données externe spécifiée ou non. La valeur par défaut est [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/\#DEFAULT).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur  int  correspondante. La valeur doit être l’une des constantes [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/). |

