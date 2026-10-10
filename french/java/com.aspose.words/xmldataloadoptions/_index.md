---
title: "XmlDataLoadOptions"
linktitle: "XmlDataLoadOptions"
second_title: "Aspose.Words pour Java"
description: "Représente les options de chargement de données XML en Java."
type: docs
weight: 745
url: /fr/java/com.aspose.words/xmldataloadoptions/
---

**Inheritance:**
java.lang.Object
```
public class XmlDataLoadOptions
```

Représente les options de chargement des données XML.

Pour en savoir plus, consultez l'article de documentation [ LINQ Reporting Engine ][LINQ Reporting Engine].

 **Remarks:** 

Une instance de cette classe peut être passée aux constructeurs de [XmlDataSource](../../com.aspose.words/xmldatasource/).


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Constructors

| Constructor | Description |
| --- | --- |
| [XmlDataLoadOptions()](#XmlDataLoadOptions) | Initialise une nouvelle instance de cette classe avec les options par défaut. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [getAlwaysGenerateRootObject()](#getAlwaysGenerateRootObject) | Obtient un indicateur indiquant si une source de données générée contiendra toujours un objet pour un élément racine XML. |
| [setAlwaysGenerateRootObject(boolean value)](#setAlwaysGenerateRootObject-boolean) | Définit un indicateur indiquant si une source de données générée contiendra toujours un objet pour un élément racine XML. |
### XmlDataLoadOptions() {#XmlDataLoadOptions}
```
public XmlDataLoadOptions()
```


Initialise une nouvelle instance de cette classe avec les options par défaut.

### getAlwaysGenerateRootObject() {#getAlwaysGenerateRootObject}
```
public boolean getAlwaysGenerateRootObject()
```


Obtient un indicateur indiquant si une source de données générée contiendra toujours un objet pour un élément racine XML. Si un élément racine XML n’a aucun attribut et que tous ses éléments enfants portent le même nom, un tel objet n’est pas créé par défaut.

 **Remarks:** 

La valeur par défaut est false.

**Returns:**
booléen - Un indicateur indiquant si une source de données générée contiendra toujours un objet pour un élément racine XML.
### setAlwaysGenerateRootObject(boolean value) {#setAlwaysGenerateRootObject-boolean}
```
public void setAlwaysGenerateRootObject(boolean value)
```


Définit un indicateur indiquant si une source de données générée contiendra toujours un objet pour un élément racine XML. Si un élément racine XML n’a aucun attribut et que tous ses éléments enfants portent le même nom, un tel objet n’est pas créé par défaut.

 **Remarks:** 

La valeur par défaut est false.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | Un indicateur indiquant si une source de données générée contiendra toujours un objet pour un élément racine XML. |

