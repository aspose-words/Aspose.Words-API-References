---
title: "XmlReadMode"
linktitle: "XmlReadMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment lire des données XML et un schéma relationnel dans un DataSet en Java."
type: docs
weight: 37
url: /fr/java/com.aspose.words.net.system.data/xmlreadmode/
---

**Inheritance:**
java.lang.Object, java.lang.Enum
```
public enum XmlReadMode extends Enum<System.Data.XmlReadMode>
```

Spécifie comment lire des données XML et un schéma relationnel dans un [DataSet](../../com.aspose.words.net.system.data/dataset/).
## Champs

| Champ | Description |
| --- | --- |
| [AUTO](#AUTO) | Par défaut. |
| [DIFF_GRAM](#DIFF-GRAM) | Lit un DiffGram, appliquant les modifications du DiffGram au [DataSet](../../com.aspose.words.net.system.data/dataset/) et préservant les valeurs [DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow/\#getRowState). |
| [FRAGMENT](#FRAGMENT) | Lit des fragments XML, tels que ceux générés par l’exécution de requêtes FOR XML, sur une instance de SQL Server. |
| [IGNORE_SCHEMA](#IGNORE-SCHEMA) | Ignore tout schéma en ligne et lit les données dans le schéma existant du [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [INFER_SCHEMA](#INFER-SCHEMA) | Ignore tout schéma en ligne, déduit le schéma à partir des données et charge les données. |
| [INFER_TYPED_SCHEMA](#INFER-TYPED-SCHEMA) | Ignore tout schéma en ligne, déduit un schéma fortement typé à partir des données, et charge les données. |
| [READ_SCHEMA](#READ-SCHEMA) | Lit tout schéma en ligne et charge les données. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [<T>valueOf(Class<T> arg0, String arg1)](#-T-valueOf-java.lang.Class-T--java.lang.String) |  |
| [compareTo(E arg0)](#compareTo-E) |  |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getDeclaringClass()](#getDeclaringClass) |  |
| [hashCode()](#hashCode) |  |
| [name()](#name) |  |
| [ordinal()](#ordinal) |  |
| [toString()](#toString) |  |
| [valueOf(String name)](#valueOf-java.lang.String) |  |
| [values()](#values) |  |
### AUTO {#AUTO}
```
public static final System.Data.XmlReadMode AUTO
```


Par défaut.

### DIFF_GRAM {#DIFF-GRAM}
```
public static final System.Data.XmlReadMode DIFF_GRAM
```


Lit un DiffGram, appliquant les modifications du DiffGram au [DataSet](../../com.aspose.words.net.system.data/dataset/) et préservant les valeurs [DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow/\#getRowState).

### FRAGMENT {#FRAGMENT}
```
public static final System.Data.XmlReadMode FRAGMENT
```


Lit des fragments XML, tels que ceux générés par l'exécution de requêtes FOR XML, contre une instance de SQL Server. Lorsque [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) est défini sur Fragment, l'espace de noms par défaut est lu comme le schéma en ligne.

### IGNORE_SCHEMA {#IGNORE-SCHEMA}
```
public static final System.Data.XmlReadMode IGNORE_SCHEMA
```


Ignore tout schéma en ligne et lit les données dans le schéma [DataSet](../../com.aspose.words.net.system.data/dataset/) existant. Si des données ne correspondent pas au schéma existant, elles sont rejetées (y compris les données provenant d'espaces de noms différents définis pour le [DataSet](../../com.aspose.words.net.system.data/dataset/)). Si les données sont un DiffGram, IgnoreSchema a la même fonctionnalité que DiffGram.

### INFER_SCHEMA {#INFER-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_SCHEMA
```


Ignore tout schéma en ligne, déduit le schéma à partir des données et charge les données. Si le [DataSet](../../com.aspose.words.net.system.data/dataset/) contient déjà un schéma, le schéma actuel est étendu en ajoutant de nouvelles tables ou des colonnes aux tables existantes. Une exception est levée si la table déduite existe déjà mais avec un espace de noms différent, ou si l'une des colonnes déduites entre en conflit avec des colonnes existantes.

### INFER_TYPED_SCHEMA {#INFER-TYPED-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_TYPED_SCHEMA
```


Ignore tout schéma en ligne, déduit un schéma fortement typé à partir des données et charge les données. Si le type ne peut pas être déduit des données, il est interprété comme des données de type chaîne. Si le [DataSet](../../com.aspose.words.net.system.data/dataset/) contient déjà un schéma, le schéma actuel est étendu, soit en ajoutant de nouvelles tables, soit en ajoutant des colonnes aux tables existantes. Une exception est levée si la table déduite existe déjà mais avec un espace de noms différent, ou si l'une des colonnes déduites entre en conflit avec des colonnes existantes.

### READ_SCHEMA {#READ-SCHEMA}
```
public static final System.Data.XmlReadMode READ_SCHEMA
```


Lit tout schéma en ligne et charge les données. Si le [DataSet](../../com.aspose.words.net.system.data/dataset/) contient déjà un schéma, de nouvelles tables peuvent être ajoutées au schéma, mais une exception est levée si des tables du schéma en ligne existent déjà dans le [DataSet](../../com.aspose.words.net.system.data/dataset/).

### <T>valueOf(Class<T> arg0, String arg1) {#-T-valueOf-java.lang.Class-T--java.lang.String}
```
public static T <T>valueOf(Class<T> arg0, String arg1)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Class<T> |  |
| arg1 | java.lang.String |  |

**Returns:**
T
### compareTo(E arg0) {#compareTo-E}
```
public final int compareTo(E arg0)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| arg0 | E |  |

**Returns:**
int
### equals(Object arg0) {#equals-java.lang.Object}
```
public final boolean equals(Object arg0)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getDeclaringClass() {#getDeclaringClass}
```
public final Class<E> getDeclaringClass()
```




**Returns:**
java.lang.Class<E>
### hashCode() {#hashCode}
```
public final int hashCode()
```




**Returns:**
int
### name() {#name}
```
public final String name()
```




**Returns:**
java.lang.String
### ordinal() {#ordinal}
```
public final int ordinal()
```




**Returns:**
int
### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### valueOf(String name) {#valueOf-java.lang.String}
```
public static System.Data.XmlReadMode valueOf(String name)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| nom | java.lang.String |  |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/)
### values() {#values}
```
public static System.Data.XmlReadMode[] values()
```




**Returns:**
com.aspose.words.net.System.Data.XmlReadMode[]
