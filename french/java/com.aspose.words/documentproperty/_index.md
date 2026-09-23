---
title: "DocumentProperty"
linktitle: "DocumentProperty"
second_title: "Aspose.Words pour Java"
description: "Représente une propriété de document personnalisée ou intégrée en Java."
type: docs
weight: 168
url: /fr/java/com.aspose.words/documentproperty/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class DocumentProperty implements Cloneable
```

Représente une propriété de document personnalisée ou intégrée.

Pour en savoir plus, consultez l’article de documentation [ Work with Document Properties ][Work with Document Properties].


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Méthodes

| Méthode | Description |
| --- | --- |
| [getLinkSource()](#getLinkSource) | Obtient la source d'une propriété de document personnalisée liée. |
| [getName()](#getName) | Renvoie le nom de la propriété. |
| [getType()](#getType) | Obtient le type de données de la propriété. |
| [getValue()](#getValue) | Obtient la valeur de la propriété. |
| [isLinkToContent()](#isLinkToContent) | Indique si cette propriété est liée au contenu ou non. |
| [setValue(Object value)](#setValue-java.lang.Object) | Définit la valeur de la propriété. |
| [toBool()](#toBool) | Renvoie la valeur de la propriété en tant que bool. |
| [toByteArray()](#toByteArray) | Renvoie la valeur de la propriété sous forme de tableau d'octets. |
| [toDateTime()](#toDateTime) | Renvoie la valeur de la propriété en tant que **DateTime** en UTC. |
| [toDouble()](#toDouble) | Renvoie la valeur de la propriété en tant que double. |
| [toInt()](#toInt) | Renvoie la valeur de la propriété en tant qu'entier. |
| [toString()](#toString) | Renvoie la valeur de la propriété sous forme de chaîne formatée selon les paramètres régionaux actuels. |
### getLinkSource() {#getLinkSource}
```
public String getLinkSource()
```


Obtient la source d'une propriété de document personnalisée liée.

 **Examples:** 

Montre comment lier une propriété de document personnalisée à un signet.

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
java.lang.String - La source d'une propriété de document personnalisée liée.
### getName() {#getName}
```
public String getName()
```


Renvoie le nom de la propriété.

 **Remarks:** 

Ne peut pas être null et ne peut pas être une chaîne vide.

**Returns:**
java.lang.String - Le nom de la propriété.
### getType() {#getType}
```
public int getType()
```


Obtient le type de données de la propriété.

 **Examples:** 

Montre comment travailler avec les propriétés personnalisées d'un document.

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
int - Le type de données de la propriété. La valeur renvoyée est l'une des constantes [PropertyType](../../com.aspose.words/propertytype/).
### getValue() {#getValue}
```
public Object getValue()
```


Obtient la valeur de la propriété.

 **Remarks:** 

Ne peut pas être  null .

**Returns:**
java.lang.Object - La valeur de la propriété.
### isLinkToContent() {#isLinkToContent}
```
public boolean isLinkToContent()
```


Indique si cette propriété est liée au contenu ou non.

 **Examples:** 

Montre comment lier une propriété de document personnalisée à un signet.

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
boolean - La valeur  boolean  correspondante.
### setValue(Object value) {#setValue-java.lang.Object}
```
public void setValue(Object value)
```


Définit la valeur de la propriété.

 **Remarks:** 

Ne peut pas être  null .

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.Object | La valeur de la propriété. |

### toBool() {#toBool}
```
public boolean toBool()
```


Renvoie la valeur de la propriété en tant que bool.

 **Remarks:** 

Lance une exception si le type de propriété n'est pas [PropertyType.BOOLEAN](../../com.aspose.words/propertytype/\#BOOLEAN).

 **Examples:** 

Présente diverses méthodes de conversion de type des propriétés de document personnalisées.

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


Renvoie la valeur de la propriété sous forme de tableau d'octets.

 **Remarks:** 

Lance une exception si le type de propriété n'est pas [PropertyType.BYTE\_ARRAY](../../com.aspose.words/propertytype/\#BYTE-ARRAY).

 **Examples:** 

Montre comment ajouter une vignette à un document que nous enregistrons au format Epub.

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


Renvoie la valeur de la propriété en tant que **DateTime** en UTC.

 **Remarks:** 

Lance une exception si le type de propriété n'est pas [PropertyType.DATE\_TIME](../../com.aspose.words/propertytype/\#DATE-TIME).

Microsoft Word ne stocke que la partie date (sans l'heure) pour les propriétés de date personnalisées.

 **Examples:** 

Montre comment créer une propriété de document personnalisée contenant une date et une heure.

```

 Document doc = new Document();

 doc.getCustomDocumentProperties().add("AuthorizationDate", new Date());

 System.out.println(MessageFormat.format("Document authorized on {0}", doc.getCustomDocumentProperties().get("AuthorizationDate")));
 
```

Présente diverses méthodes de conversion de type des propriétés de document personnalisées.

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


Renvoie la valeur de la propriété en tant que double.

 **Remarks:** 

Lance une exception si le type de propriété n'est pas [PropertyType.NUMBER](../../com.aspose.words/propertytype/\#NUMBER).

 **Examples:** 

Présente diverses méthodes de conversion de type des propriétés de document personnalisées.

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


Renvoie la valeur de la propriété en tant qu'entier.

 **Remarks:** 

Lance une exception si le type de propriété n'est pas [PropertyType.NUMBER](../../com.aspose.words/propertytype/\#NUMBER).

 **Examples:** 

Présente diverses méthodes de conversion de type des propriétés de document personnalisées.

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


Renvoie la valeur de la propriété sous forme de chaîne formatée selon les paramètres régionaux actuels.

 **Remarks:** 

Convertit une propriété booléenne en "Y" ou "N". Convertit une propriété de date en une chaîne de date courte. Pour tous les autres types, convertit une propriété en utilisant Object.ToString().

 **Examples:** 

Montre comment travailler avec des propriétés de document personnalisées.

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

Présente diverses méthodes de conversion de type des propriétés de document personnalisées.

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
