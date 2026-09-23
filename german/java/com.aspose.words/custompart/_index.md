---
title: "CustomPart"
linktitle: "CustomPart"
second_title: "Aspose.Words für Java"
description: "Stellt einen benutzerdefinierten beliebigen Inhaltsabschnitt dar, der nicht durch den ISO/IEC‑29500‑Standard in Java definiert ist."
type: docs
weight: 141
url: /de/java/com.aspose.words/custompart/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class CustomPart implements Cloneable
```

Stellt einen benutzerdefinierten (beliebigen Inhalt) Teil dar, der nicht durch den ISO/IEC‑29500‑Standard definiert ist.

Weitere Informationen finden Sie im Dokumentationsartikel [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

Diese Klasse repräsentiert einen OOXML‑Teil, der Ziel einer "unknown relationship" ist. Alle Beziehungen, die nicht innerhalb von ISO/IEC 29500 definiert sind, gelten als "unknown relationships". Unbekannte Beziehungen sind in einem Office Open XML‑Dokument zulässig, sofern sie den Richtlinien für Beziehungs‑Markup entsprechen.

Microsoft Word bewahrt benutzerdefinierte Teile während der Öffnen-/Speichern‑Zyklen. Weitere Informationen finden Sie hier http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words führt benutzerdefinierte Teile ebenfalls durch den Round‑Trip und ermöglicht zusätzlich den programmgesteuerten Zugriff auf solche Teile über die [CustomPart](../../com.aspose.words/custompart/)‑ und [CustomPartCollection](../../com.aspose.words/custompartcollection/)‑Objekte.

Verwechseln Sie benutzerdefinierte Teile nicht mit benutzerdefinierten XML‑Daten. Verwenden Sie [CustomXmlPart](../../com.aspose.words/customxmlpart/), wenn Sie auf benutzerdefinierte XML‑Daten zugreifen müssen.

 **Examples:** 

Zeigt, wie man auf die Sammlung beliebiger benutzerdefinierter Teile eines Dokuments zugreift.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [deepClone()](#deepClone) | Erstellt eine "deep enough" Kopie des Objekts. |
| [getContentType()](#getContentType) | Gibt den Inhaltstyp dieses benutzerdefinierten Teils an. |
| [getData()](#getData) | Enthält die Daten dieses benutzerdefinierten Teils. |
| [getName()](#getName) | Ermittelt den absoluten Namen dieses Teils innerhalb des OOXML‑Pakets oder die Ziel‑URL. |
| [getRelationshipType()](#getRelationshipType) | Ermittelt den Beziehungstyp vom übergeordneten Teil zu diesem benutzerdefinierten Teil. |
| [isExternal()](#isExternal) | Falsch, wenn dieser benutzerdefinierte Teil im OOXML-Paket gespeichert ist. |
| [isExternal(boolean value)](#isExternal-boolean) | Falsch, wenn dieser benutzerdefinierte Teil im OOXML-Paket gespeichert ist. |
| [setContentType(String value)](#setContentType-java.lang.String) | Gibt den Inhaltstyp dieses benutzerdefinierten Teils an. |
| [setData(byte[] value)](#setData-byte) | Enthält die Daten dieses benutzerdefinierten Teils. |
| [setName(String value)](#setName-java.lang.String) | Legt den absoluten Namen dieses Teils im OOXML-Paket oder die Ziel-URL fest. |
| [setRelationshipType(String value)](#setRelationshipType-java.lang.String) | Legt den Beziehungstyp vom übergeordneten Teil zu diesem benutzerdefinierten Teil fest. |
### deepClone() {#deepClone}
```
public CustomPart deepClone()
```


Erstellt eine „tief genug“ Kopie des Objekts. Dupliziert nicht die Bytes des [getData()](../../com.aspose.words/custompart/#getData) / [setData(byte[])](../../com.aspose.words/custompart/#setData-byte) Werts.

 **Examples:** 

Zeigt, wie man auf die Sammlung beliebiger benutzerdefinierter Teile eines Dokuments zugreift.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
[CustomPart](../../com.aspose.words/custompart/)
### getContentType() {#getContentType}
```
public String getContentType()
```


Gibt den Inhaltstyp dieses benutzerdefinierten Teils an.

 **Remarks:** 

Diese Eigenschaft ist nur anwendbar, wenn [isExternal()](../../com.aspose.words/custompart/#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/#isExternal-boolean) false ist.

Der Standardwert ist eine leere Zeichenkette. Ein gültiger Wert muss eine nicht-leere Zeichenkette sein.

 **Examples:** 

Zeigt, wie man auf die Sammlung beliebiger benutzerdefinierter Teile eines Dokuments zugreift.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getData() {#getData}
```
public byte[] getData()
```


Enthält die Daten dieses benutzerdefinierten Teils.

 **Remarks:** 

Diese Eigenschaft ist nur anwendbar, wenn [isExternal()](../../com.aspose.words/custompart/#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/#isExternal-boolean) false ist.

Der Standardwert ist ein leeres Byte‑Array. Der Wert darf nicht null sein.

 **Examples:** 

Zeigt, wie man auf die Sammlung beliebiger benutzerdefinierter Teile eines Dokuments zugreift.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
byte[] - Der entsprechende byte[]-Wert.
### getName() {#getName}
```
public String getName()
```


Ermittelt den absoluten Namen dieses Teils innerhalb des OOXML‑Pakets oder die Ziel‑URL.

 **Remarks:** 

Wenn das Beziehungsziel intern ist, ist diese Eigenschaft der absolute Teilname innerhalb des Pakets. Wenn das Beziehungsziel extern ist, ist diese Eigenschaft die Ziel-URL.

Der Standardwert ist eine leere Zeichenkette. Ein gültiger Wert muss eine nicht-leere Zeichenkette sein.

 **Examples:** 

Zeigt, wie man auf die Sammlung beliebiger benutzerdefinierter Teile eines Dokuments zugreift.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
java.lang.String - Der absolute Name dieses Teils im OOXML-Paket oder die Ziel-URL.
### getRelationshipType() {#getRelationshipType}
```
public String getRelationshipType()
```


Ermittelt den Beziehungstyp vom übergeordneten Teil zu diesem benutzerdefinierten Teil.

 **Remarks:** 

Der Beziehungstyp für einen benutzerdefinierten Teil muss "unknown" sein, z. B. ein benutzerdefinierter Beziehungstyp, nicht einer der Beziehungstypen, die in ISO/IEC 29500 definiert sind.

Der Standardwert ist eine leere Zeichenkette. Ein gültiger Wert muss eine nicht-leere Zeichenkette sein.

 **Examples:** 

Zeigt, wie man auf die Sammlung beliebiger benutzerdefinierter Teile eines Dokuments zugreift.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
java.lang.String - Der Beziehungstyp vom übergeordneten Teil zu diesem benutzerdefinierten Teil.
### isExternal() {#isExternal}
```
public boolean isExternal()
```


Falsch, wenn dieser benutzerdefinierte Teil im OOXML-Paket gespeichert ist. Wahr, wenn dieser benutzerdefinierte Teil ein externes Ziel ist.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man auf die Sammlung beliebiger benutzerdefinierter Teile eines Dokuments zugreift.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### isExternal(boolean value) {#isExternal-boolean}
```
public void isExternal(boolean value)
```


Falsch, wenn dieser benutzerdefinierte Teil im OOXML-Paket gespeichert ist. Wahr, wenn dieser benutzerdefinierte Teil ein externes Ziel ist.

 **Remarks:** 

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man auf die Sammlung beliebiger benutzerdefinierter Teile eines Dokuments zugreift.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setContentType(String value) {#setContentType-java.lang.String}
```
public void setContentType(String value)
```


Gibt den Inhaltstyp dieses benutzerdefinierten Teils an.

 **Remarks:** 

Diese Eigenschaft ist nur anwendbar, wenn [isExternal()](../../com.aspose.words/custompart/#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/#isExternal-boolean) false ist.

Der Standardwert ist eine leere Zeichenkette. Ein gültiger Wert muss eine nicht-leere Zeichenkette sein.

 **Examples:** 

Zeigt, wie man auf die Sammlung beliebiger benutzerdefinierter Teile eines Dokuments zugreift.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setData(byte[] value) {#setData-byte}
```
public void setData(byte[] value)
```


Enthält die Daten dieses benutzerdefinierten Teils.

 **Remarks:** 

Diese Eigenschaft ist nur anwendbar, wenn [isExternal()](../../com.aspose.words/custompart/#isExternal) / [isExternal(boolean)](../../com.aspose.words/custompart/#isExternal-boolean) false ist.

Der Standardwert ist ein leeres Byte‑Array. Der Wert darf nicht null sein.

 **Examples:** 

Zeigt, wie man auf die Sammlung beliebiger benutzerdefinierter Teile eines Dokuments zugreift.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | byte[] | Der entsprechende byte[]-Wert. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Legt den absoluten Namen dieses Teils im OOXML-Paket oder die Ziel-URL fest.

 **Remarks:** 

Wenn das Beziehungsziel intern ist, ist diese Eigenschaft der absolute Teilname innerhalb des Pakets. Wenn das Beziehungsziel extern ist, ist diese Eigenschaft die Ziel-URL.

Der Standardwert ist eine leere Zeichenkette. Ein gültiger Wert muss eine nicht-leere Zeichenkette sein.

 **Examples:** 

Zeigt, wie man auf die Sammlung beliebiger benutzerdefinierter Teile eines Dokuments zugreift.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der absolute Name dieses Teils im OOXML-Paket oder die Ziel-URL. |

### setRelationshipType(String value) {#setRelationshipType-java.lang.String}
```
public void setRelationshipType(String value)
```


Legt den Beziehungstyp vom übergeordneten Teil zu diesem benutzerdefinierten Teil fest.

 **Remarks:** 

Der Beziehungstyp für einen benutzerdefinierten Teil muss "unknown" sein, z. B. ein benutzerdefinierter Beziehungstyp, nicht einer der Beziehungstypen, die in ISO/IEC 29500 definiert sind.

Der Standardwert ist eine leere Zeichenkette. Ein gültiger Wert muss eine nicht-leere Zeichenkette sein.

 **Examples:** 

Zeigt, wie man auf die Sammlung beliebiger benutzerdefinierter Teile eines Dokuments zugreift.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Beziehungstyp vom übergeordneten Teil zu diesem benutzerdefinierten Teil. |

