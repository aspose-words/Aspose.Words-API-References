---
title: "DocumentProperty"
linktitle: "DocumentProperty"
second_title: "Aspose.Words para Java"
description: "Representa una propiedad de documento personalizada o incorporada en Java."
type: docs
weight: 168
url: /es/java/com.aspose.words/documentproperty/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class DocumentProperty implements Cloneable
```

Representa una propiedad de documento personalizada o incorporada.

Para obtener más información, visite el artículo de documentación [ Work with Document Properties ][Work with Document Properties].


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Métodos

| Método | Descripción |
| --- | --- |
| [getLinkSource()](#getLinkSource) | Obtiene la fuente de una propiedad de documento personalizada vinculada. |
| [getName()](#getName) | Devuelve el nombre de la propiedad. |
| [getType()](#getType) | Obtiene el tipo de datos de la propiedad. |
| [getValue()](#getValue) | Obtiene el valor de la propiedad. |
| [isLinkToContent()](#isLinkToContent) | Muestra si esta propiedad está vinculada al contenido o no. |
| [setValue(Object value)](#setValue-java.lang.Object) | Establece el valor de la propiedad. |
| [toBool()](#toBool) | Devuelve el valor de la propiedad como bool. |
| [toByteArray()](#toByteArray) | Devuelve el valor de la propiedad como matriz de bytes. |
| [toDateTime()](#toDateTime) | Devuelve el valor de la propiedad como **DateTime** en UTC. |
| [toDouble()](#toDouble) | Devuelve el valor de la propiedad como double. |
| [toInt()](#toInt) | Devuelve el valor de la propiedad como entero. |
| [toString()](#toString) | Devuelve el valor de la propiedad como una cadena formateada según la configuración regional actual. |
### getLinkSource() {#getLinkSource}
```
public String getLinkSource()
```


Obtiene la fuente de una propiedad de documento personalizada vinculada.

 **Examples:** 

Muestra cómo vincular una propiedad de documento personalizada a un marcador.

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
java.lang.String - La fuente de una propiedad de documento personalizada vinculada.
### getName() {#getName}
```
public String getName()
```


Devuelve el nombre de la propiedad.

 **Remarks:** 

No puede ser null y no puede ser una cadena vacía.

**Returns:**
java.lang.String - El nombre de la propiedad.
### getType() {#getType}
```
public int getType()
```


Obtiene el tipo de datos de la propiedad.

 **Examples:** 

Muestra cómo trabajar con las propiedades personalizadas de un documento.

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
int - El tipo de datos de la propiedad. El valor devuelto es una de las constantes de [PropertyType](../../com.aspose.words/propertytype/).
### getValue() {#getValue}
```
public Object getValue()
```


Obtiene el valor de la propiedad.

 **Remarks:** 

No puede ser  null .

**Returns:**
java.lang.Object - El valor de la propiedad.
### isLinkToContent() {#isLinkToContent}
```
public boolean isLinkToContent()
```


Muestra si esta propiedad está vinculada al contenido o no.

 **Examples:** 

Muestra cómo vincular una propiedad de documento personalizada a un marcador.

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
boolean - El valor  boolean  correspondiente.
### setValue(Object value) {#setValue-java.lang.Object}
```
public void setValue(Object value)
```


Establece el valor de la propiedad.

 **Remarks:** 

No puede ser  null .

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.Object | El valor de la propiedad. |

### toBool() {#toBool}
```
public boolean toBool()
```


Devuelve el valor de la propiedad como bool.

 **Remarks:** 

Lanza una excepción si el tipo de propiedad no es [PropertyType.BOOLEAN](../../com.aspose.words/propertytype/\#BOOLEAN).

 **Examples:** 

Muestra varios métodos de conversión de tipos de propiedades de documento personalizadas.

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


Devuelve el valor de la propiedad como matriz de bytes.

 **Remarks:** 

Lanza una excepción si el tipo de propiedad no es [PropertyType.BYTE\_ARRAY](../../com.aspose.words/propertytype/\#BYTE-ARRAY).

 **Examples:** 

Muestra cómo agregar una miniatura a un documento que guardamos como Epub.

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


Devuelve el valor de la propiedad como **DateTime** en UTC.

 **Remarks:** 

Lanza una excepción si el tipo de propiedad no es [PropertyType.DATE\_TIME](../../com.aspose.words/propertytype/\#DATE-TIME).

Microsoft Word solo almacena la parte de fecha (sin hora) para las propiedades de fecha personalizadas.

 **Examples:** 

Muestra cómo crear una propiedad de documento personalizada que contiene una fecha y hora.

```

 Document doc = new Document();

 doc.getCustomDocumentProperties().add("AuthorizationDate", new Date());

 System.out.println(MessageFormat.format("Document authorized on {0}", doc.getCustomDocumentProperties().get("AuthorizationDate")));
 
```

Muestra varios métodos de conversión de tipos de propiedades de documento personalizadas.

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


Devuelve el valor de la propiedad como double.

 **Remarks:** 

Lanza una excepción si el tipo de propiedad no es [PropertyType.NUMBER](../../com.aspose.words/propertytype/\\#NUMBER).

 **Examples:** 

Muestra varios métodos de conversión de tipos de propiedades de documento personalizadas.

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


Devuelve el valor de la propiedad como entero.

 **Remarks:** 

Lanza una excepción si el tipo de propiedad no es [PropertyType.NUMBER](../../com.aspose.words/propertytype/\\#NUMBER).

 **Examples:** 

Muestra varios métodos de conversión de tipos de propiedades de documento personalizadas.

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


Devuelve el valor de la propiedad como una cadena formateada según la configuración regional actual.

 **Remarks:** 

Convierte una propiedad booleana en \"Y\" o \"N\". Convierte una propiedad de fecha en una cadena de fecha corta. Para todos los demás tipos convierte una propiedad usando Object.ToString().

 **Examples:** 

Muestra cómo trabajar con propiedades de documento personalizadas.

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

Muestra varios métodos de conversión de tipos de propiedades de documento personalizadas.

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
