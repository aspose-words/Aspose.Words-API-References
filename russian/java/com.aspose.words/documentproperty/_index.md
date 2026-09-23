---
title: "DocumentProperty"
linktitle: "DocumentProperty"
second_title: "Aspose.Words для Java"
description: "Представляет пользовательское или встроенное свойство документа в Java."
type: docs
weight: 168
url: /ru/java/com.aspose.words/documentproperty/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class DocumentProperty implements Cloneable
```

Представляет пользовательское или встроенное свойство документа.

Чтобы узнать больше, посетите статью документации [ Work with Document Properties ][Work with Document Properties].


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Методы

| Метод | Описание |
| --- | --- |
| [getLinkSource()](#getLinkSource) | Получает источник связанного пользовательского свойства документа. |
| [getName()](#getName) | Возвращает имя свойства. |
| [getType()](#getType) | Получает тип данных свойства. |
| [getValue()](#getValue) | Получает значение свойства. |
| [isLinkToContent()](#isLinkToContent) | Показывает, связан ли это свойство с содержимым или нет. |
| [setValue(Object value)](#setValue-java.lang.Object) | Устанавливает значение свойства. |
| [toBool()](#toBool) | Возвращает значение свойства как bool. |
| [toByteArray()](#toByteArray) | Возвращает значение свойства как массив байтов. |
| [toDateTime()](#toDateTime) | Возвращает значение свойства как **DateTime** в UTC. |
| [toDouble()](#toDouble) | Возвращает значение свойства как double. |
| [toInt()](#toInt) | Возвращает значение свойства как integer. |
| [toString()](#toString) | Возвращает значение свойства как строку, отформатированную в соответствии с текущей локалью. |
### getLinkSource() {#getLinkSource}
```
public String getLinkSource()
```


Получает источник связанного пользовательского свойства документа.

 **Examples:** 

Показывает, как связать пользовательское свойство документа с закладкой.

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
java.lang.String - Источник связанного пользовательского свойства документа.
### getName() {#getName}
```
public String getName()
```


Возвращает имя свойства.

 **Remarks:** 

Не может быть null и не может быть пустой строкой.

**Returns:**
java.lang.String - Имя свойства.
### getType() {#getType}
```
public int getType()
```


Получает тип данных свойства.

 **Examples:** 

Показывает, как работать с пользовательскими свойствами документа.

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
int - Тип данных свойства. Возвращаемое значение является одной из констант [PropertyType](../../com.aspose.words/propertytype/).
### getValue() {#getValue}
```
public Object getValue()
```


Получает значение свойства.

 **Remarks:** 

Не может быть  null .

**Returns:**
java.lang.Object - Значение свойства.
### isLinkToContent() {#isLinkToContent}
```
public boolean isLinkToContent()
```


Показывает, связан ли это свойство с содержимым или нет.

 **Examples:** 

Показывает, как связать пользовательское свойство документа с закладкой.

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
boolean - Соответствующее  boolean  значение.
### setValue(Object value) {#setValue-java.lang.Object}
```
public void setValue(Object value)
```


Устанавливает значение свойства.

 **Remarks:** 

Не может быть  null .

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.Object | Значение свойства. |

### toBool() {#toBool}
```
public boolean toBool()
```


Возвращает значение свойства как bool.

 **Remarks:** 

Выбрасывает исключение, если тип свойства не является [PropertyType.BOOLEAN](../../com.aspose.words/propertytype/\#BOOLEAN).

 **Examples:** 

Показывает различные методы преобразования типов пользовательских свойств документа.

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


Возвращает значение свойства как массив байтов.

 **Remarks:** 

Выбрасывает исключение, если тип свойства не является [PropertyType.BYTE\_ARRAY](../../com.aspose.words/propertytype/\#BYTE-ARRAY).

 **Examples:** 

Показывает, как добавить миниатюру к документу, который мы сохраняем как Epub.

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


Возвращает значение свойства как **DateTime** в UTC.

 **Remarks:** 

Выбрасывает исключение, если тип свойства не является [PropertyType.DATE\_TIME](../../com.aspose.words/propertytype/\#DATE-TIME).

Microsoft Word сохраняет только часть даты (без времени) для пользовательских свойств даты.

 **Examples:** 

Показывает, как создать пользовательское свойство документа, содержащее дату и время.

```

 Document doc = new Document();

 doc.getCustomDocumentProperties().add("AuthorizationDate", new Date());

 System.out.println(MessageFormat.format("Document authorized on {0}", doc.getCustomDocumentProperties().get("AuthorizationDate")));
 
```

Показывает различные методы преобразования типов пользовательских свойств документа.

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


Возвращает значение свойства как double.

 **Remarks:** 

Выбрасывает исключение, если тип свойства не является [PropertyType.NUMBER](../../com.aspose.words/propertytype/\\#NUMBER).

 **Examples:** 

Показывает различные методы преобразования типов пользовательских свойств документа.

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


Возвращает значение свойства как integer.

 **Remarks:** 

Выбрасывает исключение, если тип свойства не является [PropertyType.NUMBER](../../com.aspose.words/propertytype/\\#NUMBER).

 **Examples:** 

Показывает различные методы преобразования типов пользовательских свойств документа.

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


Возвращает значение свойства как строку, отформатированную в соответствии с текущей локалью.

 **Remarks:** 

Преобразует логическое свойство в \"Y\" или \"N\". Преобразует свойство даты в строку короткой даты. Для всех остальных типов преобразует свойство с помощью Object.ToString().

 **Examples:** 

Показывает, как работать с пользовательскими свойствами документа.

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

Показывает различные методы преобразования типов пользовательских свойств документа.

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
