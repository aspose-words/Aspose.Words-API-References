---
title: "DocumentProperty"
linktitle: "DocumentProperty"
second_title: "Aspose.Words Java için"
description: "Java'da özel veya yerleşik bir belge özelliğini temsil eder."
type: docs
weight: 168
url: /tr/java/com.aspose.words/documentproperty/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class DocumentProperty implements Cloneable
```

Özel veya yerleşik bir belge özelliğini temsil eder.

Daha fazla bilgi edinmek için, [ Work with Document Properties ][Work with Document Properties] dokümantasyon makalesini ziyaret edin.


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getLinkSource()](#getLinkSource) | Bağlantılı özel belge özelliğinin kaynağını alır. |
| [getName()](#getName) | Özelliğin adını döndürür. |
| [getType()](#getType) | Özelliğin veri tipini alır. |
| [getValue()](#getValue) | Özelliğin değerini alır. |
| [isLinkToContent()](#isLinkToContent) | Bu özelliğin içeriğe bağlı olup olmadığını gösterir. |
| [setValue(Object value)](#setValue-java.lang.Object) | Özelliğin değerini ayarlar. |
| [toBool()](#toBool) | Özellik değerini bool olarak döndürür. |
| [toByteArray()](#toByteArray) | Özellik değerini bayt dizisi olarak döndürür. |
| [toDateTime()](#toDateTime) | Özellik değerini UTC'de **DateTime** olarak döndürür. |
| [toDouble()](#toDouble) | Özellik değerini double olarak döndürür. |
| [toInt()](#toInt) | Özellik değerini integer olarak döndürür. |
| [toString()](#toString) | Özellik değerini geçerli yerel ayara göre biçimlendirilmiş bir dize olarak döndürür. |
### getLinkSource() {#getLinkSource}
```
public String getLinkSource()
```


Bağlantılı özel belge özelliğinin kaynağını alır.

 **Examples:** 

Bir özel belge özelliğini bir yer imine bağlamanın nasıl yapılacağını gösterir.

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
java.lang.String - Bağlantılı özel belge özelliğinin kaynağı.
### getName() {#getName}
```
public String getName()
```


Özelliğin adını döndürür.

 **Remarks:** 

null olamaz ve boş bir dize olamaz.

**Returns:**
java.lang.String - Özelliğin adı.
### getType() {#getType}
```
public int getType()
```


Özelliğin veri tipini alır.

 **Examples:** 

Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.

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
int - Özelliğin veri tipi. Döndürülen değer, [PropertyType](../../com.aspose.words/propertytype/) sabitlerinden biridir.
### getValue() {#getValue}
```
public Object getValue()
```


Özelliğin değerini alır.

 **Remarks:** 

null olamaz.

**Returns:**
java.lang.Object - Özelliğin değeri.
### isLinkToContent() {#isLinkToContent}
```
public boolean isLinkToContent()
```


Bu özelliğin içeriğe bağlı olup olmadığını gösterir.

 **Examples:** 

Bir özel belge özelliğini bir yer imine bağlamanın nasıl yapılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### setValue(Object value) {#setValue-java.lang.Object}
```
public void setValue(Object value)
```


Özelliğin değerini ayarlar.

 **Remarks:** 

null olamaz.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.Object | Özelliğin değeri. |

### toBool() {#toBool}
```
public boolean toBool()
```


Özellik değerini bool olarak döndürür.

 **Remarks:** 

Özellik tipi [PropertyType.BOOLEAN](../../com.aspose.words/propertytype/\#BOOLEAN) değilse bir istisna fırlatır.

 **Examples:** 

Özel belge özelliklerinin çeşitli tip dönüşüm yöntemlerini gösterir.

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


Özellik değerini bayt dizisi olarak döndürür.

 **Remarks:** 

Özellik tipi [PropertyType.BYTE\_ARRAY](../../com.aspose.words/propertytype/\#BYTE-ARRAY) değilse bir istisna fırlatır.

 **Examples:** 

Bir belgeyi Epub olarak kaydederken nasıl bir küçük resim ekleyeceğimizi gösterir.

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


Özellik değerini UTC'de **DateTime** olarak döndürür.

 **Remarks:** 

Özellik tipi [PropertyType.DATE\_TIME](../../com.aspose.words/propertytype/\#DATE-TIME) değilse bir istisna fırlatır.

Microsoft Word, özel tarih özellikleri için yalnızca tarih kısmını (zaman yok) depolar.

 **Examples:** 

Tarih ve saat içeren bir özel belge özelliğinin nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();

 doc.getCustomDocumentProperties().add("AuthorizationDate", new Date());

 System.out.println(MessageFormat.format("Document authorized on {0}", doc.getCustomDocumentProperties().get("AuthorizationDate")));
 
```

Özel belge özelliklerinin çeşitli tip dönüşüm yöntemlerini gösterir.

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


Özellik değerini double olarak döndürür.

 **Remarks:** 

Özellik türü [PropertyType.NUMBER](../../com.aspose.words/propertytype/\#NUMBER) değilse bir istisna fırlatır.

 **Examples:** 

Özel belge özelliklerinin çeşitli tip dönüşüm yöntemlerini gösterir.

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


Özellik değerini integer olarak döndürür.

 **Remarks:** 

Özellik türü [PropertyType.NUMBER](../../com.aspose.words/propertytype/\#NUMBER) değilse bir istisna fırlatır.

 **Examples:** 

Özel belge özelliklerinin çeşitli tip dönüşüm yöntemlerini gösterir.

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


Özellik değerini geçerli yerel ayara göre biçimlendirilmiş bir dize olarak döndürür.

 **Remarks:** 

Bir boolean özelliği "Y" veya "N" değerine dönüştürür. Bir tarih özelliğini kısa tarih dizesine dönüştürür. Diğer tüm türler için bir özelliği Object.ToString() kullanarak dönüştürür.

 **Examples:** 

Özel belge özellikleriyle nasıl çalışılacağını gösterir.

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

Özel belge özelliklerinin çeşitli tip dönüşüm yöntemlerini gösterir.

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
