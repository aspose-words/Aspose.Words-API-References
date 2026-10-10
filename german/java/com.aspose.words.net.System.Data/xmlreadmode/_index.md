---
title: "XmlReadMode"
linktitle: "XmlReadMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie XML-Daten und ein relationales Schema in ein DataSet in Java eingelesen werden."
type: docs
weight: 37
url: /de/java/com.aspose.words.net.system.data/xmlreadmode/
---

**Inheritance:**
java.lang.Object, java.lang.Enum
```
public enum XmlReadMode extends Enum<System.Data.XmlReadMode>
```

Gibt an, wie XML-Daten und ein relationales Schema in ein [DataSet](../../com.aspose.words.net.system.data/dataset/) eingelesen werden.
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AUTO](#AUTO) | Standard. |
| [DIFF_GRAM](#DIFF-GRAM) | Liest ein DiffGram, wendet Änderungen aus dem DiffGram auf das [DataSet](../../com.aspose.words.net.system.data/dataset/) an und bewahrt die Werte von [DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow/\#getRowState). |
| [FRAGMENT](#FRAGMENT) | Liest XML‑Fragmente, wie sie durch die Ausführung von FOR XML‑Abfragen erzeugt werden, gegen eine Instanz von SQL Server. |
| [IGNORE_SCHEMA](#IGNORE-SCHEMA) | Ignoriert jedes Inline‑Schema und liest Daten in das vorhandene Schema des [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [INFER_SCHEMA](#INFER-SCHEMA) | Ignoriert jedes Inline‑Schema, leitet das Schema aus den Daten ab und lädt die Daten. |
| [INFER_TYPED_SCHEMA](#INFER-TYPED-SCHEMA) | Ignoriert jedes Inline‑Schema, leitet ein stark typisiertes Schema aus den Daten ab und lädt die Daten. |
| [READ_SCHEMA](#READ-SCHEMA) | Liest jedes Inline‑Schema und lädt die Daten. |
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
### AUTO {#AUTO}
```
public static final System.Data.XmlReadMode AUTO
```


Standard.

### DIFF_GRAM {#DIFF-GRAM}
```
public static final System.Data.XmlReadMode DIFF_GRAM
```


Liest ein DiffGram, wendet Änderungen aus dem DiffGram auf das [DataSet](../../com.aspose.words.net.system.data/dataset/) an und bewahrt die Werte von [DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow/\#getRowState).

### FRAGMENT {#FRAGMENT}
```
public static final System.Data.XmlReadMode FRAGMENT
```


Liest XML‑Fragmente, wie sie durch die Ausführung von FOR XML‑Abfragen erzeugt werden, gegen eine Instanz von SQL Server. Wenn [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) auf Fragment gesetzt ist, wird der Standardsnamespace als Inline‑Schema gelesen.

### IGNORE_SCHEMA {#IGNORE-SCHEMA}
```
public static final System.Data.XmlReadMode IGNORE_SCHEMA
```


Ignoriert jedes Inline‑Schema und liest Daten in das vorhandene Schema des [DataSet](../../com.aspose.words.net.system.data/dataset/). Wenn Daten nicht mit dem vorhandenen Schema übereinstimmen, werden sie verworfen (einschließlich Daten aus unterschiedlichen Namespaces, die für das [DataSet](../../com.aspose.words.net.system.data/dataset/) definiert sind). Handelt es sich bei den Daten um ein DiffGram, hat IgnoreSchema dieselbe Funktionalität wie DiffGram.

### INFER_SCHEMA {#INFER-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_SCHEMA
```


Ignoriert jedes Inline‑Schema, leitet das Schema aus den Daten ab und lädt die Daten. Wenn das [DataSet](../../com.aspose.words.net.system.data/dataset/) bereits ein Schema enthält, wird das aktuelle Schema erweitert, indem neue Tabellen hinzugefügt oder Spalten zu bestehenden Tabellen ergänzt werden. Eine Ausnahme wird ausgelöst, wenn die abgeleitete Tabelle bereits existiert, jedoch mit einem anderen Namespace, oder wenn abgeleitete Spalten mit bestehenden Spalten kollidieren.

### INFER_TYPED_SCHEMA {#INFER-TYPED-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_TYPED_SCHEMA
```


Ignoriert jedes Inline‑Schema, leitet ein stark typisiertes Schema aus den Daten ab und lädt die Daten. Wenn der Typ aus den Daten nicht abgeleitet werden kann, wird er als Zeichenkettendaten interpretiert. Wenn das [DataSet](../../com.aspose.words.net.system.data/dataset/) bereits ein Schema enthält, wird das aktuelle Schema erweitert, entweder durch Hinzufügen neuer Tabellen oder durch Hinzufügen von Spalten zu bestehenden Tabellen. Eine Ausnahme wird ausgelöst, wenn die abgeleitete Tabelle bereits existiert, jedoch mit einem anderen Namespace, oder wenn abgeleitete Spalten mit bestehenden Spalten kollidieren.

### READ_SCHEMA {#READ-SCHEMA}
```
public static final System.Data.XmlReadMode READ_SCHEMA
```


Liest jedes Inline‑Schema und lädt die Daten. Wenn das [DataSet](../../com.aspose.words.net.system.data/dataset/) bereits ein Schema enthält, können neue Tabellen zum Schema hinzugefügt werden, aber es wird eine Ausnahme ausgelöst, wenn Tabellen im Inline‑Schema bereits im [DataSet](../../com.aspose.words.net.system.data/dataset/) existieren.

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
public static System.Data.XmlReadMode valueOf(String name)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/)
### values() {#values}
```
public static System.Data.XmlReadMode[] values()
```




**Returns:**
com.aspose.words.net.System.Data.XmlReadMode[]
