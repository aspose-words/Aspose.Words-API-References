---
title: "ContentDisposition"
linktitle: "ContentDisposition"
second_title: "Aspose.Words für Java"
description: "Enumeriert verschiedene Möglichkeiten, das Dokument im Client‑Browser in Java darzustellen."
type: docs
weight: 126
url: /de/java/com.aspose.words/contentdisposition/
---

**Inheritance:**
java.lang.Object
```
public class ContentDisposition
```

Enumeriert verschiedene Möglichkeiten, das Dokument im Browser des Clients darzustellen.

 **Remarks:** 

Beachten Sie, dass das tatsächliche Verhalten im Client‑Browser durch die Sicherheitseinstellungen des Browsers beeinflusst werden kann.

 **Examples:** 

Zeigt, wie man einen Seriendruck ausführt und anschließend das Dokument im Client‑Browser speichert.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" MERGEFIELD FullName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Company ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD City ");

 doc.getMailMerge().execute(new String[]{"FullName", "Company", "Address", "City"},
         new Object[]{"James Bond", "MI5 Headquarters", "Milbank", "London"});
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ATTACHMENT](#ATTACHMENT) | Sendet das Dokument an den Browser und bietet die Möglichkeit, das Dokument auf die Festplatte zu speichern oder in der mit der Dateierweiterung verknüpften Anwendung zu öffnen. |
| [INLINE](#INLINE) | Sendet das Dokument an den Browser und bietet die Möglichkeit, das Dokument auf die Festplatte zu speichern oder im Browser zu öffnen. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String contentDispositionName)](#fromName-java.lang.String) |  |
| [getName(int contentDisposition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int contentDisposition)](#toString-int) |  |
### ATTACHMENT {#ATTACHMENT}
```
public static int ATTACHMENT
```


Sendet das Dokument an den Browser und bietet die Möglichkeit, das Dokument auf die Festplatte zu speichern oder in der mit der Dateierweiterung verknüpften Anwendung zu öffnen.

### INLINE {#INLINE}
```
public static int INLINE
```


Sendet das Dokument an den Browser und bietet die Möglichkeit, das Dokument auf die Festplatte zu speichern oder im Browser zu öffnen.

### length {#length}
```
public static int length
```


### fromName(String contentDispositionName) {#fromName-java.lang.String}
```
public static int fromName(String contentDispositionName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| contentDispositionName | java.lang.String |  |

**Returns:**
int
### getName(int contentDisposition) {#getName-int}
```
public static String getName(int contentDisposition)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int contentDisposition) {#toString-int}
```
public static String toString(int contentDisposition)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| contentDisposition | int |  |

**Returns:**
java.lang.String
