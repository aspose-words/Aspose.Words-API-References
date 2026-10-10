---
title: "DocumentProperty"
linktitle: "DocumentProperty"
second_title: "Aspose.Words für Java"
description: "Stellt eine benutzerdefinierte oder integrierte Dokumenteigenschaft in Java dar."
type: docs
weight: 168
url: /de/java/com.aspose.words/documentproperty/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class DocumentProperty implements Cloneable
```

Stellt eine benutzerdefinierte oder integrierte Dokumenteigenschaft dar.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Work with Document Properties ][Work with Document Properties].


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getLinkSource()](#getLinkSource) | Ermittelt die Quelle einer verknüpften benutzerdefinierten Dokumenteigenschaft. |
| [getName()](#getName) | Gibt den Namen der Eigenschaft zurück. |
| [getType()](#getType) | Ermittelt den Datentyp der Eigenschaft. |
| [getValue()](#getValue) | Ermittelt den Wert der Eigenschaft. |
| [isLinkToContent()](#isLinkToContent) | Zeigt an, ob diese Eigenschaft mit Inhalt verknüpft ist oder nicht. |
| [setValue(Object value)](#setValue-java.lang.Object) | Setzt den Wert der Eigenschaft. |
| [toBool()](#toBool) | Gibt den Eigenschaftswert als bool zurück. |
| [toByteArray()](#toByteArray) | Gibt den Eigenschaftswert als Byte-Array zurück. |
| [toDateTime()](#toDateTime) | Gibt den Eigenschaftswert als **DateTime** in UTC zurück. |
| [toDouble()](#toDouble) | Gibt den Eigenschaftswert als double zurück. |
| [toInt()](#toInt) | Gibt den Eigenschaftswert als integer zurück. |
| [toString()](#toString) | Gibt den Eigenschaftswert als Zeichenkette zurück, formatiert nach dem aktuellen Gebietsschema. |
### getLinkSource() {#getLinkSource}
```
public String getLinkSource()
```


Ermittelt die Quelle einer verknüpften benutzerdefinierten Dokumenteigenschaft.

 **Examples:** 

Zeigt, wie man eine benutzerdefinierte Dokumenteigenschaft mit einem Lesezeichen verknüpft.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startBookmark("MyBookmark");
 builder.write("Hello world!");
 builder.endBookmark("MyBookmark");

 // Link a new custom property to a bookmark. The value of this property
 // will be the contents of the bookmark that it references in the "LinkSource" member.
 CustomDocumentProperties customProperties = doc.getCustomDocumentProperties();
 DocumentProperty customProperty = customProperties.addLinkToContent("Bookmark", "MyBookmark");

 Assert.assertEquals(true, customProperty.isLinkToContent());
 Assert.assertEquals("MyBookmark", customProperty.getLinkSource());
 Assert.assertEquals("Hello world!", customProperty.getValue());

 doc.save(getArtifactsDir() + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
 
```

**Returns:**
java.lang.String - Die Quelle einer verknüpften benutzerdefinierten Dokumenteigenschaft.
### getName() {#getName}
```
public String getName()
```


Gibt den Namen der Eigenschaft zurück.

 **Remarks:** 

Darf nicht null sein und darf nicht leer sein.

**Returns:**
java.lang.String - Der Name der Eigenschaft.
### getType() {#getType}
```
public int getType()
```


Ermittelt den Datentyp der Eigenschaft.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```

**Returns:**
int - Der Datentyp der Eigenschaft. Der zurückgegebene Wert ist einer der [PropertyType](../../com.aspose.words/propertytype/) Konstanten.
### getValue() {#getValue}
```
public Object getValue()
```


Ermittelt den Wert der Eigenschaft.

 **Remarks:** 

Darf nicht  null  sein.

**Returns:**
java.lang.Object - Der Wert der Eigenschaft.
### isLinkToContent() {#isLinkToContent}
```
public boolean isLinkToContent()
```


Zeigt an, ob diese Eigenschaft mit Inhalt verknüpft ist oder nicht.

 **Examples:** 

Zeigt, wie man eine benutzerdefinierte Dokumenteigenschaft mit einem Lesezeichen verknüpft.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startBookmark("MyBookmark");
 builder.write("Hello world!");
 builder.endBookmark("MyBookmark");

 // Link a new custom property to a bookmark. The value of this property
 // will be the contents of the bookmark that it references in the "LinkSource" member.
 CustomDocumentProperties customProperties = doc.getCustomDocumentProperties();
 DocumentProperty customProperty = customProperties.addLinkToContent("Bookmark", "MyBookmark");

 Assert.assertEquals(true, customProperty.isLinkToContent());
 Assert.assertEquals("MyBookmark", customProperty.getLinkSource());
 Assert.assertEquals("Hello world!", customProperty.getValue());

 doc.save(getArtifactsDir() + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### setValue(Object value) {#setValue-java.lang.Object}
```
public void setValue(Object value)
```


Setzt den Wert der Eigenschaft.

 **Remarks:** 

Darf nicht  null  sein.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.Object | Der Wert der Eigenschaft. |

### toBool() {#toBool}
```
public boolean toBool()
```


Gibt den Eigenschaftswert als bool zurück.

 **Remarks:** 

Wirft eine Ausnahme, wenn der Eigenschaftstyp nicht [PropertyType.BOOLEAN](../../com.aspose.words/propertytype/\#BOOLEAN) ist.

 **Examples:** 

Zeigt verschiedene Typkonvertierungsmethoden für benutzerdefinierte Dokumenteigenschaften.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Date authDate = new Date();
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", authDate);
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 Assert.assertEquals(true, properties.get("Authorized").toBool());
 Assert.assertEquals("John Doe", properties.get("Authorized By").toString());
 Assert.assertEquals(authDate, properties.get("Authorized Date").toDateTime());
 Assert.assertEquals(1, properties.get("Authorized Revision").toInt());
 Assert.assertEquals(123.45d, properties.get("Authorized Amount").toDouble());
 
```

**Returns:**
boolean
### toByteArray() {#toByteArray}
```
public byte[] toByteArray()
```


Gibt den Eigenschaftswert als Byte-Array zurück.

 **Remarks:** 

Wirft eine Ausnahme, wenn der Eigenschaftstyp nicht [PropertyType.BYTE\_ARRAY](../../com.aspose.words/propertytype/\#BYTE-ARRAY) ist.

 **Examples:** 

Zeigt, wie man einem Dokument, das wir als Epub speichern, ein Vorschaubild hinzufügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // If we save a document, whose "Thumbnail" property contains image data that we added, as an Epub,
 // a reader that opens that document may display the image before the first page.
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 byte[] thumbnailBytes = DocumentHelper.getBytesFromStream(new FileInputStream(getImageDir() + "Logo.jpg"));
 properties.setThumbnail(thumbnailBytes);

 doc.save(getArtifactsDir() + "DocumentProperties.Thumbnail.epub");

 // We can extract a document's thumbnail image and save it to the local file system.
 DocumentProperty thumbnail = doc.getBuiltInDocumentProperties().get("Thumbnail");
 FileUtils.writeByteArrayToFile(new File(getArtifactsDir() + "DocumentProperties.Thumbnail.gif"), thumbnail.toByteArray());
 
```

**Returns:**
byte[]
### toDateTime() {#toDateTime}
```
public Date toDateTime()
```


Gibt den Eigenschaftswert als **DateTime** in UTC zurück.

 **Remarks:** 

Wirft eine Ausnahme, wenn der Eigenschaftstyp nicht [PropertyType.DATE\_TIME](../../com.aspose.words/propertytype/\#DATE-TIME) ist.

Microsoft Word speichert für benutzerdefinierte Datums-Eigenschaften nur den Datumsteil (keine Zeit).

 **Examples:** 

Zeigt, wie man eine benutzerdefinierte Dokumenteigenschaft erstellt, die ein Datum und eine Uhrzeit enthält.

```

 Document doc = new Document();

 doc.getCustomDocumentProperties().add("AuthorizationDate", new Date());

 System.out.println(MessageFormat.format("Document authorized on {0}", doc.getCustomDocumentProperties().get("AuthorizationDate")));
 
```

Zeigt verschiedene Typkonvertierungsmethoden für benutzerdefinierte Dokumenteigenschaften.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Date authDate = new Date();
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", authDate);
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 Assert.assertEquals(true, properties.get("Authorized").toBool());
 Assert.assertEquals("John Doe", properties.get("Authorized By").toString());
 Assert.assertEquals(authDate, properties.get("Authorized Date").toDateTime());
 Assert.assertEquals(1, properties.get("Authorized Revision").toInt());
 Assert.assertEquals(123.45d, properties.get("Authorized Amount").toDouble());
 
```

**Returns:**
java.util.Date
### toDouble() {#toDouble}
```
public double toDouble()
```


Gibt den Eigenschaftswert als double zurück.

 **Remarks:** 

Wirft eine Ausnahme, wenn der Eigenschaftstyp nicht [PropertyType.NUMBER](../../com.aspose.words/propertytype/\#NUMBER) ist.

 **Examples:** 

Zeigt verschiedene Typkonvertierungsmethoden für benutzerdefinierte Dokumenteigenschaften.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Date authDate = new Date();
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", authDate);
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 Assert.assertEquals(true, properties.get("Authorized").toBool());
 Assert.assertEquals("John Doe", properties.get("Authorized By").toString());
 Assert.assertEquals(authDate, properties.get("Authorized Date").toDateTime());
 Assert.assertEquals(1, properties.get("Authorized Revision").toInt());
 Assert.assertEquals(123.45d, properties.get("Authorized Amount").toDouble());
 
```

**Returns:**
double
### toInt() {#toInt}
```
public int toInt()
```


Gibt den Eigenschaftswert als integer zurück.

 **Remarks:** 

Wirft eine Ausnahme, wenn der Eigenschaftstyp nicht [PropertyType.NUMBER](../../com.aspose.words/propertytype/\#NUMBER) ist.

 **Examples:** 

Zeigt verschiedene Typkonvertierungsmethoden für benutzerdefinierte Dokumenteigenschaften.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Date authDate = new Date();
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", authDate);
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 Assert.assertEquals(true, properties.get("Authorized").toBool());
 Assert.assertEquals("John Doe", properties.get("Authorized By").toString());
 Assert.assertEquals(authDate, properties.get("Authorized Date").toDateTime());
 Assert.assertEquals(1, properties.get("Authorized Revision").toInt());
 Assert.assertEquals(123.45d, properties.get("Authorized Amount").toDouble());
 
```

**Returns:**
int
### toString() {#toString}
```
public String toString()
```


Gibt den Eigenschaftswert als Zeichenkette zurück, formatiert nach dem aktuellen Gebietsschema.

 **Remarks:** 

Konvertiert eine boolesche Eigenschaft in "Y" oder "N". Konvertiert eine Datumseigenschaft in eine kurze Datumszeichenkette. Für alle anderen Typen wird eine Eigenschaft mit Object.ToString() konvertiert.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteigenschaften arbeitet.

```

 Document doc = new Document(getMyDir() + "Properties.docx");

 // Every document contains a collection of custom properties, which, like the built-in properties, are key-value pairs.
 // The document has a fixed list of built-in properties. The user creates all of the custom properties.
 Assert.assertEquals("Value of custom document property", doc.getCustomDocumentProperties().get("CustomProperty").toString());

 doc.getCustomDocumentProperties().add("CustomProperty2", "Value of custom document property #2");

 System.out.println("Custom Properties:");
 for (DocumentProperty customDocumentProperty : doc.getCustomDocumentProperties()) {
     System.out.println(customDocumentProperty.getName());
     System.out.println(MessageFormat.format("\tType:\t{0}", customDocumentProperty.getType()));
     System.out.println(MessageFormat.format("\tValue:\t\"{0}\"", customDocumentProperty.getValue()));
 }
 
```

Zeigt verschiedene Typkonvertierungsmethoden für benutzerdefinierte Dokumenteigenschaften.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Date authDate = new Date();
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", authDate);
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 Assert.assertEquals(true, properties.get("Authorized").toBool());
 Assert.assertEquals("John Doe", properties.get("Authorized By").toString());
 Assert.assertEquals(authDate, properties.get("Authorized Date").toDateTime());
 Assert.assertEquals(1, properties.get("Authorized Revision").toInt());
 Assert.assertEquals(123.45d, properties.get("Authorized Amount").toDouble());
 
```

**Returns:**
java.lang.String
