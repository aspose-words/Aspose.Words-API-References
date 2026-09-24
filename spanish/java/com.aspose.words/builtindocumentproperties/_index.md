---
title: "BuiltInDocumentProperties"
linktitle: "BuiltInDocumentProperties"
second_title: "Aspose.Words para Java"
description: "Una colección de propiedades de documento integradas en Java."
type: docs
weight: 57
url: /es/java/com.aspose.words/builtindocumentproperties/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.DocumentPropertyCollection](../../com.aspose.words/documentpropertycollection/)
```
public class BuiltInDocumentProperties extends DocumentPropertyCollection
```

Una colección de propiedades de documento incorporadas.

Para obtener más información, visite el artículo de documentación [ Work with Document Properties ][Work with Document Properties].

 **Remarks:** 

Proporciona acceso a objetos [DocumentProperty](../../com.aspose.words/documentproperty/) por sus nombres (usando un indexador) y mediante un conjunto de propiedades tipadas que devuelven valores de los tipos apropiados.

Los nombres de las propiedades no distinguen entre mayúsculas y minúsculas.

Las propiedades en la colección se ordenan alfabéticamente por nombre.


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Métodos

| Método | Descripción |
| --- | --- |
| [clear()](#clear) | Elimina todas las propiedades de la colección. |
| [contains(String name)](#contains-java.lang.String) | Devuelve  true  si una propiedad con el nombre especificado existe en la colección. |
| [get(int index)](#get-int) | Devuelve un objeto [DocumentProperty](../../com.aspose.words/documentproperty/) por índice. |
| [get(String name)](#get-java.lang.String) | Devuelve un objeto [DocumentProperty](../../com.aspose.words/documentproperty/). |
| [getAuthor()](#getAuthor) | Obtiene el nombre del autor del documento. |
| [getBytes()](#getBytes) | Representa una estimación del número de bytes en el documento. |
| [getCategory()](#getCategory) | Obtiene la categoría del documento. |
| [getCharacters()](#getCharacters) | Representa una estimación del número de caracteres en el documento. |
| [getCharactersWithSpaces()](#getCharactersWithSpaces) | Representa una estimación del número de caracteres (incluidos los espacios) en el documento. |
| [getComments()](#getComments) | Obtiene los comentarios del documento. |
| [getCompany()](#getCompany) | Obtiene la propiedad de la empresa. |
| [getContentStatus()](#getContentStatus) | Obtiene el estado del contenido del documento. |
| [getContentType()](#getContentType) | Obtiene el tipo de contenido del documento. |
| [getCount()](#getCount) | Obtiene el número de elementos en la colección. |
| [getCreatedTime()](#getCreatedTime) | Obtiene la fecha de creación del documento en UTC. |
| [getHeadingPairs()](#getHeadingPairs) | Especifica los encabezados del documento y sus nombres. |
| [getHyperlinkBase()](#getHyperlinkBase) | Especifica la cadena base utilizada para evaluar los hipervínculos relativos en este documento. |
| [getHyperlinksChanged()](#getHyperlinksChanged) | Indica si los hipervínculos en un documento fueron modificados. |
| [getKeywords()](#getKeywords) | Obtiene las palabras clave del documento. |
| [getLastPrinted()](#getLastPrinted) | Obtiene la fecha en que el documento se imprimió por última vez en UTC. |
| [getLastSavedBy()](#getLastSavedBy) | Obtiene el nombre del último autor. |
| [getLastSavedTime()](#getLastSavedTime) | Obtiene la hora de la última vez que se guardó en UTC. |
| [getLines()](#getLines) | Representa una estimación del número de líneas en el documento. |
| [getLinksUpToDate()](#getLinksUpToDate) | Indica si los hipervínculos en un documento están actualizados. |
| [getManager()](#getManager) | Obtiene la propiedad manager. |
| [getNameOfApplication()](#getNameOfApplication) | Obtiene el nombre de la aplicación. |
| [getPages()](#getPages) | Representa una estimación del número de páginas en el documento. |
| [getParagraphs()](#getParagraphs) | Representa una estimación del número de párrafos en el documento. |
| [getRevisionNumber()](#getRevisionNumber) | Obtiene el número de revisión del documento. |
| [getScaleCrop()](#getScaleCrop) | Indica si la miniatura del documento está recortada o escalada para ajustarse a la pantalla. |
| [getSecurity()](#getSecurity) | Especifica el nivel de seguridad de un documento como un valor numérico. |
| [getSharedDocument()](#getSharedDocument) | Indica si el documento es un documento compartido. |
| [getSubject()](#getSubject) | Obtiene el asunto del documento. |
| [getTemplate()](#getTemplate) | Obtiene el nombre informativo de la plantilla del documento. |
| [getThumbnail()](#getThumbnail) | Obtiene o establece la miniatura del documento. |
| [getTitle()](#getTitle) | Obtiene el título del documento. |
| [getTitlesOfParts()](#getTitlesOfParts) | Cada cadena en la matriz especifica el nombre de una parte del documento. |
| [getTotalEditingTime()](#getTotalEditingTime) | Obtiene el tiempo total de edición en minutos. |
| [getVersion()](#getVersion) | Representa el número de versión de la aplicación que creó el documento. |
| [getWords()](#getWords) | Representa una estimación del número de palabras en el documento. |
| [indexOf(String name)](#indexOf-java.lang.String) | Obtiene el índice de una propiedad por nombre. |
| [iterator()](#iterator) | Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección. |
| [remove(String name)](#remove-java.lang.String) | Elimina una propiedad con el nombre especificado de la colección. |
| [removeAt(int index)](#removeAt-int) | Elimina una propiedad en el índice especificado. |
| [setAuthor(String value)](#setAuthor-java.lang.String) | Establece el nombre del autor del documento. |
| [setBytes(int value)](#setBytes-int) | Representa una estimación del número de bytes en el documento. |
| [setCategory(String value)](#setCategory-java.lang.String) | Establece la categoría del documento. |
| [setCharacters(int value)](#setCharacters-int) | Representa una estimación del número de caracteres en el documento. |
| [setCharactersWithSpaces(int value)](#setCharactersWithSpaces-int) | Representa una estimación del número de caracteres (incluidos los espacios) en el documento. |
| [setComments(String value)](#setComments-java.lang.String) | Establece los comentarios del documento. |
| [setCompany(String value)](#setCompany-java.lang.String) | Establece la propiedad de la empresa. |
| [setContentStatus(String value)](#setContentStatus-java.lang.String) | Establece el estado del contenido del documento. |
| [setContentType(String value)](#setContentType-java.lang.String) | Establece el tipo de contenido del documento. |
| [setCreatedTime(Date value)](#setCreatedTime-java.util.Date) | Establece la fecha de creación del documento en UTC. |
| [setHeadingPairs(Object[] value)](#setHeadingPairs-java.lang.Object) | Especifica los encabezados del documento y sus nombres. |
| [setHyperlinkBase(String value)](#setHyperlinkBase-java.lang.String) | Especifica la cadena base utilizada para evaluar los hipervínculos relativos en este documento. |
| [setKeywords(String value)](#setKeywords-java.lang.String) | Establece las palabras clave del documento. |
| [setLastPrinted(Date value)](#setLastPrinted-java.util.Date) | Establece la fecha en que el documento se imprimió por última vez en UTC. |
| [setLastSavedBy(String value)](#setLastSavedBy-java.lang.String) | Establece el nombre del último autor. |
| [setLastSavedTime(Date value)](#setLastSavedTime-java.util.Date) | Establece la hora del último guardado en UTC. |
| [setLines(int value)](#setLines-int) | Representa una estimación del número de líneas en el documento. |
| [setLinksUpToDate(boolean value)](#setLinksUpToDate-boolean) | Indica si los hipervínculos en un documento están actualizados. |
| [setManager(String value)](#setManager-java.lang.String) | Establece la propiedad del administrador. |
| [setNameOfApplication(String value)](#setNameOfApplication-java.lang.String) | Establece el nombre de la aplicación. |
| [setPages(int value)](#setPages-int) | Representa una estimación del número de páginas en el documento. |
| [setParagraphs(int value)](#setParagraphs-int) | Representa una estimación del número de párrafos en el documento. |
| [setRevisionNumber(int value)](#setRevisionNumber-int) | Establece el número de revisión del documento. |
| [setSecurity(int value)](#setSecurity-int) | Especifica el nivel de seguridad de un documento como un valor numérico. |
| [setSubject(String value)](#setSubject-java.lang.String) | Establece el asunto del documento. |
| [setTemplate(String value)](#setTemplate-java.lang.String) | Establece el nombre informativo de la plantilla del documento. |
| [setThumbnail(byte[] value)](#setThumbnail-byte) | Obtiene o establece la miniatura del documento. |
| [setTitle(String value)](#setTitle-java.lang.String) | Establece el título del documento. |
| [setTitlesOfParts(String[] value)](#setTitlesOfParts-java.lang.String) | Cada cadena en la matriz especifica el nombre de una parte del documento. |
| [setTotalEditingTime(int value)](#setTotalEditingTime-int) | Establece el tiempo total de edición en minutos. |
| [setVersion(int value)](#setVersion-int) | Representa el número de versión de la aplicación que creó el documento. |
| [setWords(int value)](#setWords-int) | Representa una estimación del número de palabras en el documento. |
### clear() {#clear}
```
public void clear()
```


Elimina todas las propiedades de la colección.

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

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Devuelve  true  si una propiedad con el nombre especificado existe en la colección.

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre de la propiedad sin distinción entre mayúsculas y minúsculas. |

**Returns:**
boolean -  true  si la propiedad existe en la colección;  false  de lo contrario.
### get(int index) {#get-int}
```
public DocumentProperty get(int index)
```


Devuelve un objeto [DocumentProperty](../../com.aspose.words/documentproperty/) por índice.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int | Índice basado en cero del [DocumentProperty](../../com.aspose.words/documentproperty/) a recuperar. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - A [DocumentProperty](../../com.aspose.words/documentproperty/) object by index.
### get(String name) {#get-java.lang.String}
```
public DocumentProperty get(String name)
```


Devuelve un objeto [DocumentProperty](../../com.aspose.words/documentproperty/).  Devuelve un objeto [DocumentProperty](../../com.aspose.words/documentproperty/) por el nombre de la propiedad.

 **Remarks:** 

Los nombres de cadena de las propiedades corresponden a los nombres de las propiedades tipadas disponibles en [BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties/).

Si solicita una propiedad que no está presente en el documento, pero el nombre de la propiedad se reconoce como un nombre incorporado válido, se crea una nueva [DocumentProperty](../../com.aspose.words/documentproperty/), se agrega a la colección y se devuelve. La propiedad recién creada se asigna a un valor predeterminado (cadena vacía, cero,  false  o DateTime.MinValue según el tipo de la propiedad incorporada).

Si solicita una propiedad que no está presente en el documento y el nombre no se reconoce como un nombre incorporado, se devuelve un  null .

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre de la propiedad sin distinción entre mayúsculas y minúsculas a recuperar. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The corresponding [DocumentProperty](../../com.aspose.words/documentproperty/) value.
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Obtiene el nombre del autor del documento.

 **Examples:** 

Muestra cómo trabajar con propiedades de documento incorporadas en la categoría "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Returns:**
java.lang.String - El nombre del autor del documento.
### getBytes() {#getBytes}
```
public int getBytes()
```


Representa una estimación del número de bytes en el documento.

 **Remarks:** 

Microsoft Word no siempre establece esta propiedad.

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
int - El valor  int  correspondiente.
### getCategory() {#getCategory}
```
public String getCategory()
```


Obtiene la categoría del documento.

 **Examples:** 

Muestra cómo trabajar con propiedades de documento incorporadas en la categoría "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Returns:**
java.lang.String - La categoría del documento.
### getCharacters() {#getCharacters}
```
public int getCharacters()
```


Representa una estimación del número de caracteres en el documento.

 **Remarks:** 

Aspose.Words actualiza esta propiedad cuando llamas a [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Muestra cómo actualizar todas las etiquetas de lista en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
int - El valor  int  correspondiente.
### getCharactersWithSpaces() {#getCharactersWithSpaces}
```
public int getCharactersWithSpaces()
```


Representa una estimación del número de caracteres (incluidos los espacios) en el documento.

 **Remarks:** 

Aspose.Words actualiza esta propiedad cuando llamas a [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
int - El valor  int  correspondiente.
### getComments() {#getComments}
```
public String getComments()
```


Obtiene los comentarios del documento.

 **Examples:** 

Muestra cómo trabajar con propiedades de documento incorporadas en la categoría "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Returns:**
java.lang.String - Los comentarios del documento.
### getCompany() {#getCompany}
```
public String getCompany()
```


Obtiene la propiedad de la empresa.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
java.lang.String - La propiedad de la empresa.
### getContentStatus() {#getContentStatus}
```
public String getContentStatus()
```


Obtiene el estado del contenido del documento.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
java.lang.String - El estado del contenido del documento.
### getContentType() {#getContentType}
```
public String getContentType()
```


Obtiene el tipo de contenido del documento.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
java.lang.String - El tipo de contenido del documento.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de elementos en la colección.

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

**Returns:**
int - Número de elementos en la colección.
### getCreatedTime() {#getCreatedTime}
```
public Date getCreatedTime()
```


Obtiene la fecha de creación del documento en UTC.

 **Remarks:** 

Para documentos originados del formato RTF, esta propiedad devuelve la hora local de la máquina del autor en el momento de la creación del documento.

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
java.util.Date - Fecha de creación del documento en UTC.
### getHeadingPairs() {#getHeadingPairs}
```
public Object[] getHeadingPairs()
```


Especifica los encabezados del documento y sus nombres.

 **Remarks:** 

Cada par de encabezados ocupa dos elementos en esta matriz.

El primer elemento del par es un java.lang.String y especifica el nombre del encabezado. El segundo elemento del par es un int y especifica la cantidad de partes del documento para este encabezado en la propiedad [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String).

La suma total de los recuentos de todos los pares de encabezados en esta propiedad debe ser igual al número de elementos en la propiedad [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String).

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra la relación entre las propiedades "HeadingPairs" y "TitlesOfParts".

```

 Document doc = new Document(getMyDir() + "Heading pairs and titles of parts.docx");

 // We can find the combined values of these collections via
 // "File" -> "Properties" -> "Advanced Properties" -> "Contents" tab.
 // The HeadingPairs property is a collection of  pairs that
 // determines how many document parts a heading spans across.
 Object[] headingPairs = doc.getBuiltInDocumentProperties().getHeadingPairs();

 // The TitlesOfParts property contains the names of parts that belong to the above headings.
 String[] titlesOfParts = doc.getBuiltInDocumentProperties().getTitlesOfParts();

 int headingPairsIndex = 0;
 int titlesOfPartsIndex = 0;
 while (headingPairsIndex < headingPairs.length) {
     System.out.println(MessageFormat.format("Parts for {0}:", headingPairs[headingPairsIndex++]));
     int partsCount = (int) headingPairs[headingPairsIndex++];

     for (int i = 0; i < partsCount; i++)
         System.out.println(MessageFormat.format("\t\"{0}\"", titlesOfParts[titlesOfPartsIndex++]));
 }
 
```

**Returns:**
java.lang.Object[] - El valor correspondiente de java.lang.Object[].
### getHyperlinkBase() {#getHyperlinkBase}
```
public String getHyperlinkBase()
```


Especifica la cadena base utilizada para evaluar los hipervínculos relativos en este documento.

 **Remarks:** 

Aspose.Words no utiliza esta propiedad.

 **Examples:** 

Muestra cómo almacenar la parte base de un hipervínculo en las propiedades del documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a relative hyperlink to a document in the local file system named "Document.docx".
 // Clicking on the link in Microsoft Word will open the designated document, if it is available.
 builder.insertHyperlink("Relative hyperlink", "Document.docx", false);

 // This link is relative. If there is no "Document.docx" in the same folder
 // as the document that contains this link, the link will be broken.
 Assert.assertFalse(new File(getArtifactsDir() + "Document.docx").exists());
 doc.save(getArtifactsDir() + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

 // The document we are trying to link to is in a different directory to the one we are planning to save the document in.
 // We could fix links like this by putting an absolute filename in each one.
 // Alternatively, we could provide a base link that every hyperlink with a relative filename
 // will prepend to its link when we click on it.
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();
 properties.setHyperlinkBase(getMyDir());

 Assert.assertTrue(new File(properties.getHyperlinkBase() + ((FieldHyperlink) doc.getRange().getFields().get(0)).getAddress()).exists());

 doc.save(getArtifactsDir() + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
 
```

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### getHyperlinksChanged() {#getHyperlinksChanged}
```
public boolean getHyperlinksChanged()
```


Indica si los hipervínculos en un documento fueron modificados.

 **Remarks:** 

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo obtener propiedades extendidas.

```

 Document doc = new Document(getMyDir() + "Extended properties.docx");
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getScaleCrop());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getSharedDocument());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getHyperlinksChanged());
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getKeywords() {#getKeywords}
```
public String getKeywords()
```


Obtiene las palabras clave del documento.

 **Examples:** 

Muestra cómo trabajar con propiedades de documento incorporadas en la categoría "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Returns:**
java.lang.String - Las palabras clave del documento.
### getLastPrinted() {#getLastPrinted}
```
public Date getLastPrinted()
```


Obtiene la fecha en que el documento se imprimió por última vez en UTC.

 **Remarks:** 

Para documentos originados del formato RTF, esta propiedad devuelve la hora local de la última operación de impresión.

Si el documento nunca se imprimió, esta propiedad devolverá DateTime.MinValue.

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
java.util.Date - La fecha en que el documento se imprimió por última vez en UTC.
### getLastSavedBy() {#getLastSavedBy}
```
public String getLastSavedBy()
```


Obtiene el nombre del último autor.

 **Remarks:** 

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
java.lang.String - El nombre del último autor.
### getLastSavedTime() {#getLastSavedTime}
```
public Date getLastSavedTime()
```


Obtiene la hora de la última vez que se guardó en UTC.

 **Remarks:** 

Para documentos originados del formato RTF, esta propiedad devuelve la hora local de la última operación de guardado.

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

Muestra cómo usar el campo SAVEDATE para mostrar la fecha/hora de la operación de guardado más reciente del documento realizada con Microsoft Word.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln(" Date this document was last saved:");

 // We can use the SAVEDATE field to display the last save operation's date and time on the document.
 // The save operation that these fields refer to is the manual save in an application like Microsoft Word,
 // not the document's Save method.
 // Below are three different calendar types according to which the SAVEDATE field can display the date/time.
 // 1 -  Islamic Lunar Calendar:
 builder.write("According to the Lunar Calendar - ");
 FieldSaveDate field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseLunarCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\h", field.getFieldCode());

 // 2 -  Umm al-Qura calendar:
 builder.write("\nAccording to the Umm al-Qura calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseUmAlQuraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\u", field.getFieldCode());

 // 3 -  Indian National calendar:
 builder.write("\nAccording to the Indian National calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseSakaEraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\s", field.getFieldCode());

 // The SAVEDATE fields draw their date/time values from the LastSavedTime built-in property.
 // The document's Save method will not update this value, but we can still update it manually.
 doc.getBuiltInDocumentProperties().setLastSavedTime(new Date());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SAVEDATE.docx");
 
```

**Returns:**
java.util.Date - La hora del último guardado en UTC.
### getLines() {#getLines}
```
public int getLines()
```


Representa una estimación del número de líneas en el documento.

 **Remarks:** 

Aspose.Words actualiza esta propiedad cuando llamas a [Document.updateWordCount(boolean)](../../com.aspose.words/document/\#updateWordCount-boolean).

 **Examples:** 

Muestra cómo actualizar todas las etiquetas de lista en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
int - El valor  int  correspondiente.
### getLinksUpToDate() {#getLinksUpToDate}
```
public boolean getLinksUpToDate()
```


Indica si los hipervínculos en un documento están actualizados.

 **Remarks:** 

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getManager() {#getManager}
```
public String getManager()
```


Obtiene la propiedad manager.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
java.lang.String - La propiedad manager.
### getNameOfApplication() {#getNameOfApplication}
```
public String getNameOfApplication()
```


Obtiene el nombre de la aplicación.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
java.lang.String - El nombre de la aplicación.
### getPages() {#getPages}
```
public int getPages()
```


Representa una estimación del número de páginas en el documento.

 **Remarks:** 

Aspose.Words actualiza esta propiedad cuando llamas a [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
int - El valor  int  correspondiente.
### getParagraphs() {#getParagraphs}
```
public int getParagraphs()
```


Representa una estimación del número de párrafos en el documento.

 **Remarks:** 

Aspose.Words actualiza esta propiedad cuando llamas a [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Muestra cómo actualizar todas las etiquetas de lista en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
int - El valor  int  correspondiente.
### getRevisionNumber() {#getRevisionNumber}
```
public int getRevisionNumber()
```


Obtiene el número de revisión del documento.

 **Remarks:** 

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

Muestra cómo trabajar con los campos REVNUM.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Current revision #");

 // Insert a REVNUM field, which displays the document's current revision number property.
 FieldRevNum field = (FieldRevNum) builder.insertField(FieldType.FIELD_REVISION_NUM, true);

 Assert.assertEquals(" REVNUM ", field.getFieldCode());
 Assert.assertEquals("1", field.getResult());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getRevisionNumber());

 // This property counts how many times a document has been saved in Microsoft Word,
 // and is unrelated to tracked revisions. We can find it by right clicking the document in Windows Explorer
 // via Properties -> Details. We can update this property manually.
 doc.getBuiltInDocumentProperties().setRevisionNumber(doc.getBuiltInDocumentProperties().getRevisionNumber() + 1);
 field.update();

 Assert.assertEquals("2", field.getResult());
 
```

**Returns:**
int - El número de revisión del documento.
### getScaleCrop() {#getScaleCrop}
```
public boolean getScaleCrop()
```


Indica si la miniatura del documento está recortada o escalada para ajustarse a la pantalla.

 **Remarks:** 

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo obtener propiedades extendidas.

```

 Document doc = new Document(getMyDir() + "Extended properties.docx");
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getScaleCrop());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getSharedDocument());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getHyperlinksChanged());
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getSecurity() {#getSecurity}
```
public int getSecurity()
```


Especifica el nivel de seguridad de un documento como un valor numérico.

 **Remarks:** 

Utiliza esta propiedad solo con fines informativos porque Microsoft Word no siempre establece esta propiedad. Esta propiedad está disponible solo en documentos DOC y OOXML.

Para proteger o desproteger un documento usa los métodos **M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** y [Document.unprotect()](../../com.aspose.words/document/\#unprotect).

Aspose.Words actualiza esta propiedad a un valor correcto antes de guardar un documento.

 **Examples:** 

Muestra cómo usar las propiedades del documento para mostrar el nivel de seguridad de un documento.

```

 Document doc = new Document();

 Assert.assertEquals(DocumentSecurity.NONE, doc.getBuiltInDocumentProperties().getSecurity());

 // If we configure a document to be read-only, it will display this status using the "Security" built-in property.
 doc.getWriteProtection().setReadOnlyRecommended(true);
 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyRecommended.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_RECOMMENDED,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyRecommended.docx").getBuiltInDocumentProperties().getSecurity());

 // Write-protect a document, and then verify its security level.
 doc = new Document();

 Assert.assertFalse(doc.getWriteProtection().isWriteProtected());

 doc.getWriteProtection().setPassword("MyPassword");

 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));
 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyEnforced.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_ENFORCED,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyEnforced.docx").getBuiltInDocumentProperties().getSecurity());

 // "Security" is a descriptive property. We can edit its value manually.
 doc = new Document();

 doc.protect(ProtectionType.ALLOW_ONLY_COMMENTS, "MyPassword");
 doc.getBuiltInDocumentProperties().setSecurity(DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS);
 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").getBuiltInDocumentProperties().getSecurity());
 
```

**Returns:**
int - El valor int correspondiente. El valor devuelto es una combinación bit a bit de las constantes [DocumentSecurity](../../com.aspose.words/documentsecurity/).
### getSharedDocument() {#getSharedDocument}
```
public boolean getSharedDocument()
```


Indica si el documento es un documento compartido.

 **Remarks:** 

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo obtener propiedades extendidas.

```

 Document doc = new Document(getMyDir() + "Extended properties.docx");
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getScaleCrop());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getSharedDocument());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getHyperlinksChanged());
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getSubject() {#getSubject}
```
public String getSubject()
```


Obtiene el asunto del documento.

 **Examples:** 

Muestra cómo trabajar con propiedades de documento incorporadas en la categoría "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Returns:**
java.lang.String - El asunto del documento.
### getTemplate() {#getTemplate}
```
public String getTemplate()
```


Obtiene el nombre informativo de la plantilla del documento.

 **Remarks:** 

En Microsoft Word, esta propiedad es solo con fines informativos y generalmente contiene solo el nombre de archivo de la plantilla sin la ruta.

Una cadena vacía significa que el documento está adjunto a la plantilla Normal.

Para obtener o establecer el nombre real de la plantilla adjunta, usa la propiedad [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String).

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
java.lang.String - El nombre informativo de la plantilla del documento.
### getThumbnail() {#getThumbnail}
```
public byte[] getThumbnail()
```


Obtiene o establece la miniatura del documento.

**Returns:**
byte[] - El valor byte[] correspondiente.
### getTitle() {#getTitle}
```
public String getTitle()
```


Obtiene el título del documento.

 **Examples:** 

Muestra cómo trabajar con propiedades de documento incorporadas en la categoría "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Returns:**
java.lang.String - El título del documento.
### getTitlesOfParts() {#getTitlesOfParts}
```
public String[] getTitlesOfParts()
```


Cada cadena en la matriz especifica el nombre de una parte del documento.

 **Remarks:** 

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra la relación entre las propiedades "HeadingPairs" y "TitlesOfParts".

```

 Document doc = new Document(getMyDir() + "Heading pairs and titles of parts.docx");

 // We can find the combined values of these collections via
 // "File" -> "Properties" -> "Advanced Properties" -> "Contents" tab.
 // The HeadingPairs property is a collection of  pairs that
 // determines how many document parts a heading spans across.
 Object[] headingPairs = doc.getBuiltInDocumentProperties().getHeadingPairs();

 // The TitlesOfParts property contains the names of parts that belong to the above headings.
 String[] titlesOfParts = doc.getBuiltInDocumentProperties().getTitlesOfParts();

 int headingPairsIndex = 0;
 int titlesOfPartsIndex = 0;
 while (headingPairsIndex < headingPairs.length) {
     System.out.println(MessageFormat.format("Parts for {0}:", headingPairs[headingPairsIndex++]));
     int partsCount = (int) headingPairs[headingPairsIndex++];

     for (int i = 0; i < partsCount; i++)
         System.out.println(MessageFormat.format("\t\"{0}\"", titlesOfParts[titlesOfPartsIndex++]));
 }
 
```

**Returns:**
java.lang.String[] - El valor java.lang.String[] correspondiente.
### getTotalEditingTime() {#getTotalEditingTime}
```
public int getTotalEditingTime()
```


Obtiene el tiempo total de edición en minutos.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
int - El tiempo total de edición en minutos.
### getVersion() {#getVersion}
```
public int getVersion()
```


Representa el número de versión de la aplicación que creó el documento.

 **Remarks:** 

Cuando un documento fue creado por Microsoft Word, los 16 bits altos representan la versión principal y los 16 bits bajos representan el número de compilación.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Returns:**
int - El valor  int  correspondiente.
### getWords() {#getWords}
```
public int getWords()
```


Representa una estimación del número de palabras en el documento.

 **Remarks:** 

Aspose.Words actualiza esta propiedad cuando llamas a [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Muestra cómo actualizar todas las etiquetas de lista en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Returns:**
int - El valor  int  correspondiente.
### indexOf(String name) {#indexOf-java.lang.String}
```
public int indexOf(String name)
```


Obtiene el índice de una propiedad por nombre.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre de la propiedad sin distinción entre mayúsculas y minúsculas. |

**Returns:**
int - El índice basado en cero. Valor negativo si no se encuentra.
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un objeto iterador que puede usarse para iterar sobre todos los elementos de la colección.

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
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Elimina una propiedad con el nombre especificado de la colección.

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| nombre | java.lang.String | El nombre de la propiedad sin distinción entre mayúsculas y minúsculas. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Elimina una propiedad en el índice especificado.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | El índice basado en cero. |

### setAuthor(String value) {#setAuthor-java.lang.String}
```
public void setAuthor(String value)
```


Establece el nombre del autor del documento.

 **Examples:** 

Muestra cómo trabajar con propiedades de documento incorporadas en la categoría "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El nombre del autor del documento. |

### setBytes(int value) {#setBytes-int}
```
public void setBytes(int value)
```


Representa una estimación del número de bytes en el documento.

 **Remarks:** 

Microsoft Word no siempre establece esta propiedad.

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setCategory(String value) {#setCategory-java.lang.String}
```
public void setCategory(String value)
```


Establece la categoría del documento.

 **Examples:** 

Muestra cómo trabajar con propiedades de documento incorporadas en la categoría "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | La categoría del documento. |

### setCharacters(int value) {#setCharacters-int}
```
public void setCharacters(int value)
```


Representa una estimación del número de caracteres en el documento.

 **Remarks:** 

Aspose.Words actualiza esta propiedad cuando llamas a [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Muestra cómo actualizar todas las etiquetas de lista en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setCharactersWithSpaces(int value) {#setCharactersWithSpaces-int}
```
public void setCharactersWithSpaces(int value)
```


Representa una estimación del número de caracteres (incluidos los espacios) en el documento.

 **Remarks:** 

Aspose.Words actualiza esta propiedad cuando llamas a [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setComments(String value) {#setComments-java.lang.String}
```
public void setComments(String value)
```


Establece los comentarios del documento.

 **Examples:** 

Muestra cómo trabajar con propiedades de documento incorporadas en la categoría "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Los comentarios del documento. |

### setCompany(String value) {#setCompany-java.lang.String}
```
public void setCompany(String value)
```


Establece la propiedad de la empresa.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | La propiedad de la empresa. |

### setContentStatus(String value) {#setContentStatus-java.lang.String}
```
public void setContentStatus(String value)
```


Establece el estado del contenido del documento.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El estado del contenido del documento. |

### setContentType(String value) {#setContentType-java.lang.String}
```
public void setContentType(String value)
```


Establece el tipo de contenido del documento.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El tipo de contenido del documento. |

### setCreatedTime(Date value) {#setCreatedTime-java.util.Date}
```
public void setCreatedTime(Date value)
```


Establece la fecha de creación del documento en UTC.

 **Remarks:** 

Para documentos originados del formato RTF, esta propiedad devuelve la hora local de la máquina del autor en el momento de la creación del documento.

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.util.Date | Fecha de creación del documento en UTC. |

### setHeadingPairs(Object[] value) {#setHeadingPairs-java.lang.Object}
```
public void setHeadingPairs(Object[] value)
```


Especifica los encabezados del documento y sus nombres.

 **Remarks:** 

Cada par de encabezados ocupa dos elementos en esta matriz.

El primer elemento del par es un java.lang.String y especifica el nombre del encabezado. El segundo elemento del par es un int y especifica la cantidad de partes del documento para este encabezado en la propiedad [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String).

La suma total de los recuentos de todos los pares de encabezados en esta propiedad debe ser igual al número de elementos en la propiedad [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String).

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra la relación entre las propiedades "HeadingPairs" y "TitlesOfParts".

```

 Document doc = new Document(getMyDir() + "Heading pairs and titles of parts.docx");

 // We can find the combined values of these collections via
 // "File" -> "Properties" -> "Advanced Properties" -> "Contents" tab.
 // The HeadingPairs property is a collection of  pairs that
 // determines how many document parts a heading spans across.
 Object[] headingPairs = doc.getBuiltInDocumentProperties().getHeadingPairs();

 // The TitlesOfParts property contains the names of parts that belong to the above headings.
 String[] titlesOfParts = doc.getBuiltInDocumentProperties().getTitlesOfParts();

 int headingPairsIndex = 0;
 int titlesOfPartsIndex = 0;
 while (headingPairsIndex < headingPairs.length) {
     System.out.println(MessageFormat.format("Parts for {0}:", headingPairs[headingPairsIndex++]));
     int partsCount = (int) headingPairs[headingPairsIndex++];

     for (int i = 0; i < partsCount; i++)
         System.out.println(MessageFormat.format("\t\"{0}\"", titlesOfParts[titlesOfPartsIndex++]));
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.Object[] | El valor correspondiente de java.lang.Object[]. |

### setHyperlinkBase(String value) {#setHyperlinkBase-java.lang.String}
```
public void setHyperlinkBase(String value)
```


Especifica la cadena base utilizada para evaluar los hipervínculos relativos en este documento.

 **Remarks:** 

Aspose.Words no utiliza esta propiedad.

 **Examples:** 

Muestra cómo almacenar la parte base de un hipervínculo en las propiedades del documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a relative hyperlink to a document in the local file system named "Document.docx".
 // Clicking on the link in Microsoft Word will open the designated document, if it is available.
 builder.insertHyperlink("Relative hyperlink", "Document.docx", false);

 // This link is relative. If there is no "Document.docx" in the same folder
 // as the document that contains this link, the link will be broken.
 Assert.assertFalse(new File(getArtifactsDir() + "Document.docx").exists());
 doc.save(getArtifactsDir() + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

 // The document we are trying to link to is in a different directory to the one we are planning to save the document in.
 // We could fix links like this by putting an absolute filename in each one.
 // Alternatively, we could provide a base link that every hyperlink with a relative filename
 // will prepend to its link when we click on it.
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();
 properties.setHyperlinkBase(getMyDir());

 Assert.assertTrue(new File(properties.getHyperlinkBase() + ((FieldHyperlink) doc.getRange().getFields().get(0)).getAddress()).exists());

 doc.save(getArtifactsDir() + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setKeywords(String value) {#setKeywords-java.lang.String}
```
public void setKeywords(String value)
```


Establece las palabras clave del documento.

 **Examples:** 

Muestra cómo trabajar con propiedades de documento incorporadas en la categoría "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Las palabras clave del documento. |

### setLastPrinted(Date value) {#setLastPrinted-java.util.Date}
```
public void setLastPrinted(Date value)
```


Establece la fecha en que el documento se imprimió por última vez en UTC.

 **Remarks:** 

Para documentos originados del formato RTF, esta propiedad devuelve la hora local de la última operación de impresión.

Si el documento nunca se imprimió, esta propiedad devolverá DateTime.MinValue.

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.util.Date | La fecha en que el documento se imprimió por última vez en UTC. |

### setLastSavedBy(String value) {#setLastSavedBy-java.lang.String}
```
public void setLastSavedBy(String value)
```


Establece el nombre del último autor.

 **Remarks:** 

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El nombre del último autor. |

### setLastSavedTime(Date value) {#setLastSavedTime-java.util.Date}
```
public void setLastSavedTime(Date value)
```


Establece la hora del último guardado en UTC.

 **Remarks:** 

Para documentos originados del formato RTF, esta propiedad devuelve la hora local de la última operación de guardado.

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

Muestra cómo usar el campo SAVEDATE para mostrar la fecha/hora de la operación de guardado más reciente del documento realizada con Microsoft Word.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln(" Date this document was last saved:");

 // We can use the SAVEDATE field to display the last save operation's date and time on the document.
 // The save operation that these fields refer to is the manual save in an application like Microsoft Word,
 // not the document's Save method.
 // Below are three different calendar types according to which the SAVEDATE field can display the date/time.
 // 1 -  Islamic Lunar Calendar:
 builder.write("According to the Lunar Calendar - ");
 FieldSaveDate field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseLunarCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\h", field.getFieldCode());

 // 2 -  Umm al-Qura calendar:
 builder.write("\nAccording to the Umm al-Qura calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseUmAlQuraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\u", field.getFieldCode());

 // 3 -  Indian National calendar:
 builder.write("\nAccording to the Indian National calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseSakaEraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\s", field.getFieldCode());

 // The SAVEDATE fields draw their date/time values from the LastSavedTime built-in property.
 // The document's Save method will not update this value, but we can still update it manually.
 doc.getBuiltInDocumentProperties().setLastSavedTime(new Date());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SAVEDATE.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.util.Date | La hora del último guardado en UTC. |

### setLines(int value) {#setLines-int}
```
public void setLines(int value)
```


Representa una estimación del número de líneas en el documento.

 **Remarks:** 

Aspose.Words actualiza esta propiedad cuando llamas a [Document.updateWordCount(boolean)](../../com.aspose.words/document/\#updateWordCount-boolean).

 **Examples:** 

Muestra cómo actualizar todas las etiquetas de lista en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setLinksUpToDate(boolean value) {#setLinksUpToDate-boolean}
```
public void setLinksUpToDate(boolean value)
```


Indica si los hipervínculos en un documento están actualizados.

 **Remarks:** 

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setManager(String value) {#setManager-java.lang.String}
```
public void setManager(String value)
```


Establece la propiedad del administrador.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | La propiedad manager. |

### setNameOfApplication(String value) {#setNameOfApplication-java.lang.String}
```
public void setNameOfApplication(String value)
```


Establece el nombre de la aplicación.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El nombre de la aplicación. |

### setPages(int value) {#setPages-int}
```
public void setPages(int value)
```


Representa una estimación del número de páginas en el documento.

 **Remarks:** 

Aspose.Words actualiza esta propiedad cuando llamas a [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setParagraphs(int value) {#setParagraphs-int}
```
public void setParagraphs(int value)
```


Representa una estimación del número de párrafos en el documento.

 **Remarks:** 

Aspose.Words actualiza esta propiedad cuando llamas a [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Muestra cómo actualizar todas las etiquetas de lista en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setRevisionNumber(int value) {#setRevisionNumber-int}
```
public void setRevisionNumber(int value)
```


Establece el número de revisión del documento.

 **Remarks:** 

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

Muestra cómo trabajar con los campos REVNUM.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Current revision #");

 // Insert a REVNUM field, which displays the document's current revision number property.
 FieldRevNum field = (FieldRevNum) builder.insertField(FieldType.FIELD_REVISION_NUM, true);

 Assert.assertEquals(" REVNUM ", field.getFieldCode());
 Assert.assertEquals("1", field.getResult());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getRevisionNumber());

 // This property counts how many times a document has been saved in Microsoft Word,
 // and is unrelated to tracked revisions. We can find it by right clicking the document in Windows Explorer
 // via Properties -> Details. We can update this property manually.
 doc.getBuiltInDocumentProperties().setRevisionNumber(doc.getBuiltInDocumentProperties().getRevisionNumber() + 1);
 field.update();

 Assert.assertEquals("2", field.getResult());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El número de revisión del documento. |

### setSecurity(int value) {#setSecurity-int}
```
public void setSecurity(int value)
```


Especifica el nivel de seguridad de un documento como un valor numérico.

 **Remarks:** 

Utiliza esta propiedad solo con fines informativos porque Microsoft Word no siempre establece esta propiedad. Esta propiedad está disponible solo en documentos DOC y OOXML.

Para proteger o desproteger un documento usa los métodos **M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** y [Document.unprotect()](../../com.aspose.words/document/\#unprotect).

Aspose.Words actualiza esta propiedad a un valor correcto antes de guardar un documento.

 **Examples:** 

Muestra cómo usar las propiedades del documento para mostrar el nivel de seguridad de un documento.

```

 Document doc = new Document();

 Assert.assertEquals(DocumentSecurity.NONE, doc.getBuiltInDocumentProperties().getSecurity());

 // If we configure a document to be read-only, it will display this status using the "Security" built-in property.
 doc.getWriteProtection().setReadOnlyRecommended(true);
 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyRecommended.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_RECOMMENDED,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyRecommended.docx").getBuiltInDocumentProperties().getSecurity());

 // Write-protect a document, and then verify its security level.
 doc = new Document();

 Assert.assertFalse(doc.getWriteProtection().isWriteProtected());

 doc.getWriteProtection().setPassword("MyPassword");

 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));
 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyEnforced.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_ENFORCED,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyEnforced.docx").getBuiltInDocumentProperties().getSecurity());

 // "Security" is a descriptive property. We can edit its value manually.
 doc = new Document();

 doc.protect(ProtectionType.ALLOW_ONLY_COMMENTS, "MyPassword");
 doc.getBuiltInDocumentProperties().setSecurity(DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS);
 doc.save(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx");

 Assert.assertEquals(DocumentSecurity.READ_ONLY_EXCEPT_ANNOTATIONS,
         new Document(getArtifactsDir() + "DocumentProperties.Security.ReadOnlyExceptAnnotations.docx").getBuiltInDocumentProperties().getSecurity());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor correspondiente  int  . El valor debe ser una combinación bit a bit de los constantes de [DocumentSecurity](../../com.aspose.words/documentsecurity/). |

### setSubject(String value) {#setSubject-java.lang.String}
```
public void setSubject(String value)
```


Establece el asunto del documento.

 **Examples:** 

Muestra cómo trabajar con propiedades de documento incorporadas en la categoría "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El asunto del documento. |

### setTemplate(String value) {#setTemplate-java.lang.String}
```
public void setTemplate(String value)
```


Establece el nombre informativo de la plantilla del documento.

 **Remarks:** 

En Microsoft Word, esta propiedad es solo con fines informativos y generalmente contiene solo el nombre de archivo de la plantilla sin la ruta.

Una cadena vacía significa que el documento está adjunto a la plantilla Normal.

Para obtener o establecer el nombre real de la plantilla adjunta, usa la propiedad [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String).

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El nombre informativo de la plantilla del documento. |

### setThumbnail(byte[] value) {#setThumbnail-byte}
```
public void setThumbnail(byte[] value)
```


Obtiene o establece la miniatura del documento.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | byte[] | El valor byte[] correspondiente. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


Establece el título del documento.

 **Examples:** 

Muestra cómo trabajar con propiedades de documento incorporadas en la categoría "Description".

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // Below are four built-in document properties that have fields that can display their values in the document body.
 // 1 -  "Author" property, which we can display using an AUTHOR field:
 properties.setAuthor("John Doe");
 builder.write("Author:\t");
 builder.insertField(FieldType.FIELD_AUTHOR, true);

 // 2 -  "Title" property, which we can display using a TITLE field:
 properties.setTitle("John's Document");
 builder.write("\nDoc title:\t");
 builder.insertField(FieldType.FIELD_TITLE, true);

 // 3 -  "Subject" property, which we can display using a SUBJECT field:
 properties.setSubject("My subject");
 builder.write("\nSubject:\t");
 builder.insertField(FieldType.FIELD_SUBJECT, true);

 // 4 -  "Comments" property, which we can display using a COMMENTS field:
 properties.setComments(MessageFormat.format("This is {0}''s document about {1}", properties.getAuthor(), properties.getSubject()));
 builder.write("\nComments:\t\"");
 builder.insertField(FieldType.FIELD_COMMENTS, true);
 builder.write("\"");

 // The "Category" built-in property does not have a field that can display its value.
 properties.setCategory("My category");

 // We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
 properties.setKeywords("Tag 1; Tag 2; Tag 3");

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
 // The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
 doc.save(getArtifactsDir() + "DocumentProperties.Description.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El título del documento. |

### setTitlesOfParts(String[] value) {#setTitlesOfParts-java.lang.String}
```
public void setTitlesOfParts(String[] value)
```


Cada cadena en la matriz especifica el nombre de una parte del documento.

 **Remarks:** 

Aspose.Words no actualiza esta propiedad.

 **Examples:** 

Muestra la relación entre las propiedades "HeadingPairs" y "TitlesOfParts".

```

 Document doc = new Document(getMyDir() + "Heading pairs and titles of parts.docx");

 // We can find the combined values of these collections via
 // "File" -> "Properties" -> "Advanced Properties" -> "Contents" tab.
 // The HeadingPairs property is a collection of  pairs that
 // determines how many document parts a heading spans across.
 Object[] headingPairs = doc.getBuiltInDocumentProperties().getHeadingPairs();

 // The TitlesOfParts property contains the names of parts that belong to the above headings.
 String[] titlesOfParts = doc.getBuiltInDocumentProperties().getTitlesOfParts();

 int headingPairsIndex = 0;
 int titlesOfPartsIndex = 0;
 while (headingPairsIndex < headingPairs.length) {
     System.out.println(MessageFormat.format("Parts for {0}:", headingPairs[headingPairsIndex++]));
     int partsCount = (int) headingPairs[headingPairsIndex++];

     for (int i = 0; i < partsCount; i++)
         System.out.println(MessageFormat.format("\t\"{0}\"", titlesOfParts[titlesOfPartsIndex++]));
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String[] | El valor correspondiente de java.lang.String[]. |

### setTotalEditingTime(int value) {#setTotalEditingTime-int}
```
public void setTotalEditingTime(int value)
```


Establece el tiempo total de edición en minutos.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El tiempo total de edición en minutos. |

### setVersion(int value) {#setVersion-int}
```
public void setVersion(int value)
```


Representa el número de versión de la aplicación que creó el documento.

 **Remarks:** 

Cuando un documento fue creado por Microsoft Word, los 16 bits altos representan la versión principal y los 16 bits bajos representan el número de compilación.

 **Examples:** 

Muestra cómo trabajar con las propiedades del documento en la categoría "Origin".

```

 // Open a document that we have created and edited using Microsoft Word.
 Document doc = new Document(getMyDir() + "Properties.docx");
 BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

 // The following built-in properties contain information regarding the creation and editing of this document.
 // We can right-click this document in Windows Explorer and find
 // these properties via "Properties" -> "Details" -> "Origin" category.
 // Fields such as PRINTDATE and EDITTIME can display these values in the document body.
 System.out.println(MessageFormat.format("Created using {0}, on {1}", properties.getNameOfApplication(), properties.getCreatedTime()));
 System.out.println(MessageFormat.format("Minutes spent editing: {0}", properties.getTotalEditingTime()));
 System.out.println(MessageFormat.format("Date/time last printed: {0}", properties.getLastPrinted()));
 System.out.println(MessageFormat.format("Template document: {0}", properties.getTemplate()));

 // We can also change the values of built-in properties.
 properties.setCompany("Doe Ltd.");
 properties.setManager("Jane Doe");
 properties.setVersion(5);
 properties.setRevisionNumber(properties.getRevisionNumber() + 1);

 // Microsoft Word updates the following properties automatically when we save the document.
 // To use these properties with Aspose.Words, we will need to set values for them manually.
 properties.setLastSavedBy("John Doe");
 properties.setLastSavedTime(new Date());

 // We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details" -> "Origin".
 doc.save(getArtifactsDir() + "DocumentProperties.Origin.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setWords(int value) {#setWords-int}
```
public void setWords(int value)
```


Representa una estimación del número de palabras en el documento.

 **Remarks:** 

Aspose.Words actualiza esta propiedad cuando llamas a [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Muestra cómo actualizar todas las etiquetas de lista en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

Muestra cómo trabajar con las propiedades del documento en la categoría "Content".

```

 public void content() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");
     BuiltInDocumentProperties properties = doc.getBuiltInDocumentProperties();

     // By using built in properties,
     // we can treat document statistics such as word/page/character counts as metadata that can be glanced at without opening the document
     // These properties are accessed by right clicking the file in Windows Explorer and navigating to Properties > Details > Content
     // If we want to display this data inside the document, we can use fields such as NUMPAGES, NUMWORDS, NUMCHARS etc.
     // Also, these values can also be viewed in Microsoft Word by navigating File > Properties > Advanced Properties > Statistics
     // Page count: The PageCount property shows the page count in real time and its value can be assigned to the Pages property

     // The "Pages" property stores the page count of the document.
     Assert.assertEquals(6, properties.getPages());

     // The "Words", "Characters", and "CharactersWithSpaces" built-in properties also display various document statistics,
     // but we need to call the "UpdateWordCount" method on the whole document before we can expect them to contain accurate values.
     doc.updateWordCount();

     Assert.assertEquals(1035, properties.getWords());
     Assert.assertEquals(6026, properties.getCharacters());
     Assert.assertEquals(7041, properties.getCharactersWithSpaces());

     // Count the number of lines in the document, and then assign the result to the "Lines" built-in property.
     LineCounter lineCounter = new LineCounter(doc);
     properties.setLines(lineCounter.getLineCount());

     Assert.assertEquals(142, properties.getLines());

     // Assign the number of Paragraph nodes in the document to the "Paragraphs" built-in property.
     properties.setParagraphs(doc.getChildNodes(NodeType.PARAGRAPH, true).getCount());
     Assert.assertEquals(29, properties.getParagraphs());

     // Get an estimate of the file size of our document via the "Bytes" built-in property.
     Assert.assertEquals(20310, properties.getBytes());

     // Set a different template for our document, and then update the "Template" built-in property manually to reflect this change.
     doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");

     Assert.assertEquals("Normal", properties.getTemplate());

     properties.setTemplate(doc.getAttachedTemplate());

     // "ContentStatus" is a descriptive built-in property.
     properties.setContentStatus("Draft");

     // Upon saving, the "ContentType" built-in property will contain the MIME type of the output save format.
     Assert.assertEquals("", properties.getContentType());

     // If the document contains links, and they are all up to date, we can set the "LinksUpToDate" property to "true".
     Assert.assertFalse(properties.getLinksUpToDate());

     doc.save(getArtifactsDir() + "DocumentProperties.Content.docx");
 }

 /// 
 /// Counts the lines in a document.
 /// Traverses the document's layout entities tree upon construction,
 /// counting entities of the "Line" type that also contain real text.
 /// 
 private static class LineCounter {
     public LineCounter(Document doc) throws Exception {
         mLayoutEnumerator = new LayoutEnumerator(doc);

         countLines();
     }

     public int getLineCount() {
         return mLineCount;
     }

     private void countLines() throws Exception {
         do {
             if (mLayoutEnumerator.getType() == LayoutEntityType.LINE) {
                 mScanningLineForRealText = true;
             }

             if (mLayoutEnumerator.moveFirstChild()) {
                 if (mScanningLineForRealText && mLayoutEnumerator.getKind().startsWith("TEXT")) {
                     mLineCount++;
                     mScanningLineForRealText = false;
                 }
                 countLines();
                 mLayoutEnumerator.moveParent();
             }
         } while (mLayoutEnumerator.moveNext());
     }

     private final LayoutEnumerator mLayoutEnumerator;
     private int mLineCount;
     private boolean mScanningLineForRealText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

