---
title: "OdsoRecipientData"
linktitle: "OdsoRecipientData"
second_title: "Aspose.Words pour Java"
description: "Représente des informations sur un enregistrement unique d’une source de données externe qui doit être exclu de la fusion de courrier en Java."
type: docs
weight: 492
url: /fr/java/com.aspose.words/odsorecipientdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoRecipientData implements Cloneable
```

Représente les informations concernant un enregistrement unique d'une source de données externe qui doit être exclu du publipostage.

Pour en savoir plus, consultez l’article de documentation [ Mail Merge and Reporting ][Mail Merge and Reporting].

 **Remarks:** 

Si un enregistrement doit être fusionné dans un document fusionné, aucune information n'est nécessaire à propos de cet enregistrement. Cependant, si un enregistrement donné ne doit pas être fusionné dans un document fusionné, la valeur de la clé unique pour cet enregistrement doit être stockée dans la propriété [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte) de cet objet pour indiquer cette exclusion.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Méthodes

| Méthode | Description |
| --- | --- |
| [deepClone()](#deepClone) | Renvoie un clone profond de cet objet. |
| [getActive()](#getActive) | Spécifie si l'enregistrement de la source de données doit être importé dans un document lors de l'exécution de la fusion de courrier. |
| [getColumn()](#getColumn) | Spécifie la colonne de la source de données qui contient des données uniques pour l'enregistrement actuel. |
| [getHash()](#getHash) | Représente le code de hachage de cet enregistrement. |
| [getUniqueTag()](#getUniqueTag) | Spécifie le contenu d'un enregistrement donné dans la colonne contenant des données uniques. |
| [setActive(boolean value)](#setActive-boolean) | Spécifie si l'enregistrement de la source de données doit être importé dans un document lors de l'exécution de la fusion de courrier. |
| [setColumn(int value)](#setColumn-int) | Spécifie la colonne de la source de données qui contient des données uniques pour l'enregistrement actuel. |
| [setHash(int value)](#setHash-int) | Représente le code de hachage de cet enregistrement. |
| [setUniqueTag(byte[] value)](#setUniqueTag-byte) | Spécifie le contenu d'un enregistrement donné dans la colonne contenant des données uniques. |
### deepClone() {#deepClone}
```
public OdsoRecipientData deepClone()
```


Renvoie un clone profond de cet objet.

**Returns:**
[OdsoRecipientData](../../com.aspose.words/odsorecipientdata/)
### getActive() {#getActive}
```
public boolean getActive()
```


Spécifie si l'enregistrement de la source de données doit être importé dans un document lors de la fusion de courrier. La valeur par défaut est true.

**Returns:**
boolean - La valeur  boolean  correspondante.
### getColumn() {#getColumn}
```
public int getColumn()
```


Spécifie la colonne de la source de données qui contient des données uniques pour l'enregistrement actuel. La valeur par défaut est 0.

**Returns:**
int - La valeur int correspondante.
### getHash() {#getHash}
```
public int getHash()
```


Représente le code de hachage de cet enregistrement. Parfois, Microsoft Word utilise [getHash()](../../com.aspose.words/odsorecipientdata/\#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/\#setHash-int) d'un enregistrement complet au lieu d'une valeur [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte). La valeur par défaut est 0.

**Returns:**
int - La valeur int correspondante.
### getUniqueTag() {#getUniqueTag}
```
public byte[] getUniqueTag()
```


Spécifie le contenu d'un enregistrement donné dans la colonne contenant des données uniques. La valeur par défaut est null.

**Returns:**
byte[] - La valeur byte[] correspondante.
### setActive(boolean value) {#setActive-boolean}
```
public void setActive(boolean value)
```


Spécifie si l'enregistrement de la source de données doit être importé dans un document lors de la fusion de courrier. La valeur par défaut est true.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


Spécifie la colonne de la source de données qui contient des données uniques pour l'enregistrement actuel. La valeur par défaut est 0.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La valeur  int  correspondante. |

### setHash(int value) {#setHash-int}
```
public void setHash(int value)
```


Représente le code de hachage de cet enregistrement. Parfois, Microsoft Word utilise [getHash()](../../com.aspose.words/odsorecipientdata/\#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/\#setHash-int) d'un enregistrement complet au lieu d'une valeur [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte). La valeur par défaut est 0.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | int | La valeur  int  correspondante. |

### setUniqueTag(byte[] value) {#setUniqueTag-byte}
```
public void setUniqueTag(byte[] value)
```


Spécifie le contenu d'un enregistrement donné dans la colonne contenant des données uniques. La valeur par défaut est null.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | byte[] | La valeur byte[] correspondante. |

