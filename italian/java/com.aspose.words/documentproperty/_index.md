---
title: "DocumentProperty"
linktitle: "DocumentProperty"
second_title: "Aspose.Words per Java"
description: "Rappresenta una proprietà di documento personalizzata o incorporata in Java."
type: docs
weight: 168
url: /it/java/com.aspose.words/documentproperty/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class DocumentProperty implements Cloneable
```

Rappresenta una proprietà del documento personalizzata o predefinita.

Per saperne di più, visita l'articolo di documentazione [ Work with Document Properties ][Work with Document Properties].


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getLinkSource()](#getLinkSource) | Ottiene l'origine di una proprietà di documento personalizzata collegata. |
| [getName()](#getName) | Restituisce il nome della proprietà. |
| [getType()](#getType) | Ottiene il tipo di dato della proprietà. |
| [getValue()](#getValue) | Ottiene il valore della proprietà. |
| [isLinkToContent()](#isLinkToContent) | Mostra se questa proprietà è collegata al contenuto o meno. |
| [setValue(Object value)](#setValue-java.lang.Object) | Imposta il valore della proprietà. |
| [toBool()](#toBool) | Restituisce il valore della proprietà come bool. |
| [toByteArray()](#toByteArray) | Restituisce il valore della proprietà come array di byte. |
| [toDateTime()](#toDateTime) | Restituisce il valore della proprietà come **DateTime** in UTC. |
| [toDouble()](#toDouble) | Restituisce il valore della proprietà come double. |
| [toInt()](#toInt) | Restituisce il valore della proprietà come integer. |
| [toString()](#toString) | Restituisce il valore della proprietà come stringa formattata secondo le impostazioni locali correnti. |
### getLinkSource() {#getLinkSource}
```
public String getLinkSource()
```


Ottiene l'origine di una proprietà di documento personalizzata collegata.

 **Examples:** 

Mostra come collegare una proprietà documento personalizzata a un segnalibro.

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
java.lang.String - L'origine di una proprietà di documento personalizzata collegata.
### getName() {#getName}
```
public String getName()
```


Restituisce il nome della proprietà.

 **Remarks:** 

Non può essere null e non può essere una stringa vuota.

**Returns:**
java.lang.String - Il nome della proprietà.
### getType() {#getType}
```
public int getType()
```


Ottiene il tipo di dato della proprietà.

 **Examples:** 

Mostra come lavorare con le proprietà personalizzate di un documento.

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
int - Il tipo di dato della proprietà. Il valore restituito è una delle costanti [PropertyType](../../com.aspose.words/propertytype/) .
### getValue() {#getValue}
```
public Object getValue()
```


Ottiene il valore della proprietà.

 **Remarks:** 

Non può essere  null .

**Returns:**
java.lang.Object - Il valore della proprietà.
### isLinkToContent() {#isLinkToContent}
```
public boolean isLinkToContent()
```


Mostra se questa proprietà è collegata al contenuto o meno.

 **Examples:** 

Mostra come collegare una proprietà documento personalizzata a un segnalibro.

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
boolean - Il valore booleano corrispondente.
### setValue(Object value) {#setValue-java.lang.Object}
```
public void setValue(Object value)
```


Imposta il valore della proprietà.

 **Remarks:** 

Non può essere  null .

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.Object | Il valore della proprietà. |

### toBool() {#toBool}
```
public boolean toBool()
```


Restituisce il valore della proprietà come bool.

 **Remarks:** 

Genera un'eccezione se il tipo di proprietà non è [PropertyType.BOOLEAN](../../com.aspose.words/propertytype/\#BOOLEAN).

 **Examples:** 

Mostra vari metodi di conversione di tipo delle proprietà di documento personalizzate.

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


Restituisce il valore della proprietà come array di byte.

 **Remarks:** 

Genera un'eccezione se il tipo di proprietà non è [PropertyType.BYTE\_ARRAY](../../com.aspose.words/propertytype/\#BYTE-ARRAY).

 **Examples:** 

Mostra come aggiungere una miniatura a un documento che salviamo come Epub.

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


Restituisce il valore della proprietà come **DateTime** in UTC.

 **Remarks:** 

Genera un'eccezione se il tipo di proprietà non è [PropertyType.DATE\_TIME](../../com.aspose.words/propertytype/\#DATE-TIME).

Microsoft Word memorizza solo la parte della data (senza l'ora) per le proprietà data personalizzate.

 **Examples:** 

Mostra come creare una proprietà documento personalizzata che contiene una data e un'ora.

```

 Document doc = new Document();

 doc.getCustomDocumentProperties().add("AuthorizationDate", new Date());

 System.out.println(MessageFormat.format("Document authorized on {0}", doc.getCustomDocumentProperties().get("AuthorizationDate")));
 
```

Mostra vari metodi di conversione di tipo delle proprietà di documento personalizzate.

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


Restituisce il valore della proprietà come double.

 **Remarks:** 

Genera un'eccezione se il tipo di proprietà non è [PropertyType.NUMBER](../../com.aspose.words/propertytype/\#NUMBER).

 **Examples:** 

Mostra vari metodi di conversione di tipo delle proprietà di documento personalizzate.

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


Restituisce il valore della proprietà come integer.

 **Remarks:** 

Genera un'eccezione se il tipo di proprietà non è [PropertyType.NUMBER](../../com.aspose.words/propertytype/\#NUMBER).

 **Examples:** 

Mostra vari metodi di conversione di tipo delle proprietà di documento personalizzate.

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


Restituisce il valore della proprietà come stringa formattata secondo le impostazioni locali correnti.

 **Remarks:** 

Converte una proprietà booleana in "Y" o "N". Converte una proprietà data in una stringa di data breve. Per tutti gli altri tipi converte una proprietà usando Object.ToString().

 **Examples:** 

Mostra come lavorare con le proprietà personalizzate del documento.

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

Mostra vari metodi di conversione di tipo delle proprietà di documento personalizzate.

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
