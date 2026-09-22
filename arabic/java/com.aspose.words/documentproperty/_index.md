---
title: "DocumentProperty"
linktitle: "DocumentProperty"
second_title: "Aspose.Words لـ Java"
description: "يمثل خاصية مستند مخصصة أو مدمجة في Java."
type: docs
weight: 168
url: /ar/java/com.aspose.words/documentproperty/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class DocumentProperty implements Cloneable
```

يمثل خاصية مستند مخصصة أو مدمجة.

للتعرف على المزيد، زر مقالة الوثائق [ Work with Document Properties ][Work with Document Properties].


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getLinkSource()](#getLinkSource) | يحصل على مصدر خاصية المستند المخصصة المرتبطة. |
| [getName()](#getName) | يعيد اسم الخاصية. |
| [getType()](#getType) | يحصل على نوع البيانات للخاصية. |
| [getValue()](#getValue) | يحصل على قيمة الخاصية. |
| [isLinkToContent()](#isLinkToContent) | يوضح ما إذا كانت هذه الخاصية مرتبطة بالمحتوى أم لا. |
| [setValue(Object value)](#setValue-java.lang.Object) | يضبط قيمة الخاصية. |
| [toBool()](#toBool) | يعيد قيمة الخاصية كقيمة منطقية (bool). |
| [toByteArray()](#toByteArray) | يعيد قيمة الخاصية كمصفوفة بايت. |
| [toDateTime()](#toDateTime) | يعيد قيمة الخاصية كـ **DateTime** بتوقيت UTC. |
| [toDouble()](#toDouble) | يعيد قيمة الخاصية كقيمة مزدوجة (double). |
| [toInt()](#toInt) | يعيد قيمة الخاصية كعدد صحيح (integer). |
| [toString()](#toString) | يعيد قيمة الخاصية كسلسلة نصية مُنسقة وفقًا للمنطقة الحالية. |
### getLinkSource() {#getLinkSource}
```
public String getLinkSource()
```


يحصل على مصدر خاصية المستند المخصصة المرتبطة.

 **Examples:** 

يوضح كيفية ربط خاصية مستند مخصصة بإشارة مرجعية.

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
java.lang.String - مصدر خاصية المستند المخصصة المرتبطة.
### getName() {#getName}
```
public String getName()
```


يعيد اسم الخاصية.

 **Remarks:** 

لا يمكن أن تكون null ولا يمكن أن تكون سلسلة فارغة.

**Returns:**
java.lang.String - اسم الخاصية.
### getType() {#getType}
```
public int getType()
```


يحصل على نوع البيانات للخاصية.

 **Examples:** 

يوضح كيفية العمل مع خصائص المستند المخصصة.

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
int - نوع البيانات للخاصية. القيمة المرجعة هي واحدة من ثوابت [PropertyType](../../com.aspose.words/propertytype/).
### getValue() {#getValue}
```
public Object getValue()
```


يحصل على قيمة الخاصية.

 **Remarks:** 

لا يمكن أن تكون  null .

**Returns:**
java.lang.Object - قيمة الخاصية.
### isLinkToContent() {#isLinkToContent}
```
public boolean isLinkToContent()
```


يوضح ما إذا كانت هذه الخاصية مرتبطة بالمحتوى أم لا.

 **Examples:** 

يوضح كيفية ربط خاصية مستند مخصصة بإشارة مرجعية.

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
boolean - القيمة المنطقية المقابلة.
### setValue(Object value) {#setValue-java.lang.Object}
```
public void setValue(Object value)
```


يضبط قيمة الخاصية.

 **Remarks:** 

لا يمكن أن تكون  null .

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.Object | قيمة الخاصية. |

### toBool() {#toBool}
```
public boolean toBool()
```


يعيد قيمة الخاصية كقيمة منطقية (bool).

 **Remarks:** 

يرمي استثناءً إذا لم يكن نوع الخاصية [PropertyType.BOOLEAN](../../com.aspose.words/propertytype/\#BOOLEAN).

 **Examples:** 

يعرض طرق تحويل الأنواع المختلفة لخصائص المستند المخصصة.

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


يعيد قيمة الخاصية كمصفوفة بايت.

 **Remarks:** 

يرمي استثناءً إذا لم يكن نوع الخاصية [PropertyType.BYTE\_ARRAY](../../com.aspose.words/propertytype/\#BYTE-ARRAY).

 **Examples:** 

يعرض كيفية إضافة صورة مصغرة إلى مستند نحفظه كملف Epub.

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


يعيد قيمة الخاصية كـ **DateTime** بتوقيت UTC.

 **Remarks:** 

يرمي استثناءً إذا لم يكن نوع الخاصية [PropertyType.DATE\_TIME](../../com.aspose.words/propertytype/\#DATE-TIME).

يخزن Microsoft Word جزء التاريخ فقط (بدون وقت) لخصائص التاريخ المخصصة.

 **Examples:** 

يوضح كيفية إنشاء خاصية مستند مخصصة تحتوي على تاريخ ووقت.

```

 Document doc = new Document();

 doc.getCustomDocumentProperties().add("AuthorizationDate", new Date());

 System.out.println(MessageFormat.format("Document authorized on {0}", doc.getCustomDocumentProperties().get("AuthorizationDate")));
 
```

يعرض طرق تحويل الأنواع المختلفة لخصائص المستند المخصصة.

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


يعيد قيمة الخاصية كقيمة مزدوجة (double).

 **Remarks:** 

يرمي استثناءً إذا لم يكن نوع الخاصية هو [PropertyType.NUMBER](../../com.aspose.words/propertytype/\#NUMBER).

 **Examples:** 

يعرض طرق تحويل الأنواع المختلفة لخصائص المستند المخصصة.

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


يعيد قيمة الخاصية كعدد صحيح (integer).

 **Remarks:** 

يرمي استثناءً إذا لم يكن نوع الخاصية هو [PropertyType.NUMBER](../../com.aspose.words/propertytype/\#NUMBER).

 **Examples:** 

يعرض طرق تحويل الأنواع المختلفة لخصائص المستند المخصصة.

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


يعيد قيمة الخاصية كسلسلة نصية مُنسقة وفقًا للمنطقة الحالية.

 **Remarks:** 

يقوم بتحويل خاصية منطقية إلى "Y" أو "N". يحول خاصية تاريخ إلى سلسلة تاريخ قصيرة. لجميع الأنواع الأخرى يحول الخاصية باستخدام Object.ToString().

 **Examples:** 

يوضح كيفية العمل مع خصائص المستند المخصصة.

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

يعرض طرق تحويل الأنواع المختلفة لخصائص المستند المخصصة.

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
