---
title: "Regel"
linktitle: "Regel"
second_title: "Aspose.Words für Java"
description: "Gibt die Aktion an, die auftritt, wenn ein ForeignKeyConstraint in Java durchgesetzt wird."
type: docs
weight: 36
url: /de/java/com.aspose.words.net.system.data/rule/
---

**Inheritance:**
java.lang.Object, java.lang.Enum
```
public enum Rule extends Enum<System.Data.Rule>
```

Gibt die Aktion an, die auftritt, wenn ein [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) durchgesetzt wird.
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CASCADE](#CASCADE) | Löschen oder Aktualisieren verwandter Zeilen. |
| [NONE](#NONE) | Keine Aktion für verwandte Zeilen. |
| [SET_DEFAULT](#SET-DEFAULT) | Setzt Werte in verwandten Zeilen auf den in der Eigenschaft [DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn/\#getDefaultValue) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn/\#setDefaultValue-java.lang.Object) enthaltenen Wert. |
| [SET_NULL](#SET-NULL) | Setzt Werte in verwandten Zeilen auf DBNull. |
## Methoden

| Methode | Beschreibung |
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
### CASCADE {#CASCADE}
```
public static final System.Data.Rule CASCADE
```


Löschen oder Aktualisieren verwandter Zeilen. Dies ist die Vorgabe.

### NONE {#NONE}
```
public static final System.Data.Rule NONE
```


Keine Aktion für verwandte Zeilen.

### SET_DEFAULT {#SET-DEFAULT}
```
public static final System.Data.Rule SET_DEFAULT
```


Setzt Werte in verwandten Zeilen auf den in der Eigenschaft [DataColumn.getDefaultValue()](../../com.aspose.words.net.system.data/datacolumn/\#getDefaultValue) / [DataColumn.setDefaultValue(java.lang.Object)](../../com.aspose.words.net.system.data/datacolumn/\#setDefaultValue-java.lang.Object) enthaltenen Wert.

### SET_NULL {#SET-NULL}
```
public static final System.Data.Rule SET_NULL
```


Setzt Werte in verwandten Zeilen auf DBNull.

### <T>valueOf(Class<T> arg0, String arg1) {#-T-valueOf-java.lang.Class-T--java.lang.String}
```
public static T <T>valueOf(Class<T> arg0, String arg1)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| arg0 | E |  |

**Returns:**
int
### equals(Object arg0) {#equals-java.lang.Object}
```
public final boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
public static System.Data.Rule valueOf(String name)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/)
### values() {#values}
```
public static System.Data.Rule[] values()
```




**Returns:**
com.aspose.words.net.System.Data.Rule[]
