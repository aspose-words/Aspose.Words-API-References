---
title: "BuiltInDocumentProperties"
linktitle: "BuiltInDocumentProperties"
second_title: "Aspose.Words для Java"
description: "Коллекция встроенных свойств документа в Java."
type: docs
weight: 57
url: /ru/java/com.aspose.words/builtindocumentproperties/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.DocumentPropertyCollection](../../com.aspose.words/documentpropertycollection/)
```
public class BuiltInDocumentProperties extends DocumentPropertyCollection
```

Коллекция встроенных свойств документа.

Чтобы узнать больше, посетите статью документации [ Work with Document Properties ][Work with Document Properties].

 **Remarks:** 

Обеспечивает доступ к объектам [DocumentProperty](../../com.aspose.words/documentproperty/) по их именам (с использованием индексатора) и через набор типизированных свойств, возвращающих значения соответствующих типов.

Имена свойств не чувствительны к регистру.

Свойства в коллекции отсортированы в алфавитном порядке по имени.


[Work with Document Properties]: https://docs.aspose.com/words/java/work-with-document-properties/
## Методы

| Метод | Описание |
| --- | --- |
| [clear()](#clear) | Удаляет все свойства из коллекции. |
| [contains(String name)](#contains-java.lang.String) | Возвращает  true  если свойство с указанным именем существует в коллекции. |
| [get(int index)](#get-int) | Возвращает объект [DocumentProperty](../../com.aspose.words/documentproperty/) по индексу. |
| [get(String name)](#get-java.lang.String) | Возвращает объект [DocumentProperty](../../com.aspose.words/documentproperty/). |
| [getAuthor()](#getAuthor) | Получает имя автора документа. |
| [getBytes()](#getBytes) | Представляет оценку количества байтов в документе. |
| [getCategory()](#getCategory) | Получает категорию документа. |
| [getCharacters()](#getCharacters) | Представляет оценку количества символов в документе. |
| [getCharactersWithSpaces()](#getCharactersWithSpaces) | Представляет оценку количества символов (включая пробелы) в документе. |
| [getComments()](#getComments) | Получает комментарии документа. |
| [getCompany()](#getCompany) | Получает свойство компании. |
| [getContentStatus()](#getContentStatus) | Получает статус содержимого документа. |
| [getContentType()](#getContentType) | Получает тип содержимого документа. |
| [getCount()](#getCount) | Получает количество элементов в коллекции. |
| [getCreatedTime()](#getCreatedTime) | Получает дату создания документа в UTC. |
| [getHeadingPairs()](#getHeadingPairs) | Указывает заголовки документа и их названия. |
| [getHyperlinkBase()](#getHyperlinkBase) | Указывает базовую строку, используемую для оценки относительных гиперссылок в этом документе. |
| [getHyperlinksChanged()](#getHyperlinksChanged) | Указывает, были ли изменены гиперссылки в документе. |
| [getKeywords()](#getKeywords) | Получает ключевые слова документа. |
| [getLastPrinted()](#getLastPrinted) | Получает дату последней печати документа в UTC. |
| [getLastSavedBy()](#getLastSavedBy) | Получает имя последнего автора. |
| [getLastSavedTime()](#getLastSavedTime) | Получает время последнего сохранения в UTC. |
| [getLines()](#getLines) | Представляет оценку количества строк в документе. |
| [getLinksUpToDate()](#getLinksUpToDate) | Указывает, актуальны ли гиперссылки в документе. |
| [getManager()](#getManager) | Получает свойство manager. |
| [getNameOfApplication()](#getNameOfApplication) | Получает имя приложения. |
| [getPages()](#getPages) | Представляет оценку количества страниц в документе. |
| [getParagraphs()](#getParagraphs) | Представляет оценку количества абзацев в документе. |
| [getRevisionNumber()](#getRevisionNumber) | Получает номер ревизии документа. |
| [getScaleCrop()](#getScaleCrop) | Указывает, обрезан ли миниатюрный образ документа или масштабирован для соответствия дисплею. |
| [getSecurity()](#getSecurity) | Указывает уровень безопасности документа в виде числового значения. |
| [getSharedDocument()](#getSharedDocument) | Указывает, является ли документ общим. |
| [getSubject()](#getSubject) | Получает тему документа. |
| [getTemplate()](#getTemplate) | Получает информационное имя шаблона документа. |
| [getThumbnail()](#getThumbnail) | Получает или задает миниатюру документа. |
| [getTitle()](#getTitle) | Получает заголовок документа. |
| [getTitlesOfParts()](#getTitlesOfParts) | Каждая строка в массиве указывает имя части документа. |
| [getTotalEditingTime()](#getTotalEditingTime) | Получает общее время редактирования в минутах. |
| [getVersion()](#getVersion) | Представляет номер версии приложения, создавшего документ. |
| [getWords()](#getWords) | Представляет оценку количества слов в документе. |
| [indexOf(String name)](#indexOf-java.lang.String) | Получает индекс свойства по имени. |
| [iterator()](#iterator) | Возвращает объект-итератор, который можно использовать для перебора всех элементов в коллекции. |
| [remove(String name)](#remove-java.lang.String) | Удаляет свойство с указанным именем из коллекции. |
| [removeAt(int index)](#removeAt-int) | Удаляет свойство по указанному индексу. |
| [setAuthor(String value)](#setAuthor-java.lang.String) | Устанавливает имя автора документа. |
| [setBytes(int value)](#setBytes-int) | Представляет оценку количества байтов в документе. |
| [setCategory(String value)](#setCategory-java.lang.String) | Устанавливает категорию документа. |
| [setCharacters(int value)](#setCharacters-int) | Представляет оценку количества символов в документе. |
| [setCharactersWithSpaces(int value)](#setCharactersWithSpaces-int) | Представляет оценку количества символов (включая пробелы) в документе. |
| [setComments(String value)](#setComments-java.lang.String) | Устанавливает комментарии к документу. |
| [setCompany(String value)](#setCompany-java.lang.String) | Устанавливает свойство компании. |
| [setContentStatus(String value)](#setContentStatus-java.lang.String) | Устанавливает статус содержимого документа. |
| [setContentType(String value)](#setContentType-java.lang.String) | Устанавливает тип содержимого документа. |
| [setCreatedTime(Date value)](#setCreatedTime-java.util.Date) | Устанавливает дату создания документа в UTC. |
| [setHeadingPairs(Object[] value)](#setHeadingPairs-java.lang.Object) | Указывает заголовки документа и их названия. |
| [setHyperlinkBase(String value)](#setHyperlinkBase-java.lang.String) | Указывает базовую строку, используемую для оценки относительных гиперссылок в этом документе. |
| [setKeywords(String value)](#setKeywords-java.lang.String) | Устанавливает ключевые слова документа. |
| [setLastPrinted(Date value)](#setLastPrinted-java.util.Date) | Устанавливает дату последней печати документа в UTC. |
| [setLastSavedBy(String value)](#setLastSavedBy-java.lang.String) | Устанавливает имя последнего автора. |
| [setLastSavedTime(Date value)](#setLastSavedTime-java.util.Date) | Устанавливает время последнего сохранения в UTC. |
| [setLines(int value)](#setLines-int) | Представляет оценку количества строк в документе. |
| [setLinksUpToDate(boolean value)](#setLinksUpToDate-boolean) | Указывает, актуальны ли гиперссылки в документе. |
| [setManager(String value)](#setManager-java.lang.String) | Устанавливает свойство менеджера. |
| [setNameOfApplication(String value)](#setNameOfApplication-java.lang.String) | Устанавливает имя приложения. |
| [setPages(int value)](#setPages-int) | Представляет оценку количества страниц в документе. |
| [setParagraphs(int value)](#setParagraphs-int) | Представляет оценку количества абзацев в документе. |
| [setRevisionNumber(int value)](#setRevisionNumber-int) | Устанавливает номер ревизии документа. |
| [setSecurity(int value)](#setSecurity-int) | Указывает уровень безопасности документа в виде числового значения. |
| [setSubject(String value)](#setSubject-java.lang.String) | Устанавливает тему документа. |
| [setTemplate(String value)](#setTemplate-java.lang.String) | Устанавливает информационное имя шаблона документа. |
| [setThumbnail(byte[] value)](#setThumbnail-byte) | Получает или задает миниатюру документа. |
| [setTitle(String value)](#setTitle-java.lang.String) | Устанавливает заголовок документа. |
| [setTitlesOfParts(String[] value)](#setTitlesOfParts-java.lang.String) | Каждая строка в массиве указывает имя части документа. |
| [setTotalEditingTime(int value)](#setTotalEditingTime-int) | Устанавливает общее время редактирования в минутах. |
| [setVersion(int value)](#setVersion-int) | Представляет номер версии приложения, создавшего документ. |
| [setWords(int value)](#setWords-int) | Представляет оценку количества слов в документе. |
### clear() {#clear}
```
public void clear()
```


Удаляет все свойства из коллекции.

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

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Возвращает  true  если свойство с указанным именем существует в коллекции.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя свойства без учета регистра. |

**Returns:**
boolean -  true  если свойство существует в коллекции;  false  в противном случае.
### get(int index) {#get-int}
```
public DocumentProperty get(int index)
```


Возвращает объект [DocumentProperty](../../com.aspose.words/documentproperty/) по индексу.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Нулевой индекс [DocumentProperty](../../com.aspose.words/documentproperty/) для получения. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - A [DocumentProperty](../../com.aspose.words/documentproperty/) object by index.
### get(String name) {#get-java.lang.String}
```
public DocumentProperty get(String name)
```


Возвращает объект [DocumentProperty](../../com.aspose.words/documentproperty/).  Возвращает объект [DocumentProperty](../../com.aspose.words/documentproperty/) по имени свойства.

 **Remarks:** 

Строковые имена свойств соответствуют именам типизированных свойств, доступных из [BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties/).

Если вы запрашиваете свойство, которого нет в документе, но имя свойства распознаётся как допустимое встроенное имя, создаётся новое [DocumentProperty](../../com.aspose.words/documentproperty/), добавляется в коллекцию и возвращается. Ново созданное свойство получает значение по умолчанию (пустая строка, ноль,  false  или DateTime.MinValue в зависимости от типа встроенного свойства).

Если вы запрашиваете свойство, которого нет в документе, и имя не распознаётся как встроенное, возвращается  null .

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя свойства без учета регистра для получения. |

**Returns:**
[DocumentProperty](../../com.aspose.words/documentproperty/) - The corresponding [DocumentProperty](../../com.aspose.words/documentproperty/) value.
### getAuthor() {#getAuthor}
```
public String getAuthor()
```


Получает имя автора документа.

 **Examples:** 

Показывает, как работать со встроенными свойствами документа в категории "Description".

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
java.lang.String - Имя автора документа.
### getBytes() {#getBytes}
```
public int getBytes()
```


Представляет оценку количества байтов в документе.

 **Remarks:** 

Microsoft Word не всегда устанавливает это свойство.

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Content".

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
int — соответствующее значение  int .
### getCategory() {#getCategory}
```
public String getCategory()
```


Получает категорию документа.

 **Examples:** 

Показывает, как работать со встроенными свойствами документа в категории "Description".

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
java.lang.String - Категория документа.
### getCharacters() {#getCharacters}
```
public int getCharacters()
```


Представляет оценку количества символов в документе.

 **Remarks:** 

Aspose.Words обновляет это свойство, когда вы вызываете [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Показывает, как обновить все метки списков в документе.

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

Показывает, как работать со свойствами документа в категории "Content".

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
int — соответствующее значение  int .
### getCharactersWithSpaces() {#getCharactersWithSpaces}
```
public int getCharactersWithSpaces()
```


Представляет оценку количества символов (включая пробелы) в документе.

 **Remarks:** 

Aspose.Words обновляет это свойство, когда вы вызываете [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Content".

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
int — соответствующее значение  int .
### getComments() {#getComments}
```
public String getComments()
```


Получает комментарии документа.

 **Examples:** 

Показывает, как работать со встроенными свойствами документа в категории "Description".

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
java.lang.String - Комментарии к документу.
### getCompany() {#getCompany}
```
public String getCompany()
```


Получает свойство компании.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
java.lang.String - Свойство компании.
### getContentStatus() {#getContentStatus}
```
public String getContentStatus()
```


Получает статус содержимого документа.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Content".

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
java.lang.String - Статус содержимого документа.
### getContentType() {#getContentType}
```
public String getContentType()
```


Получает тип содержимого документа.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Content".

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
java.lang.String - Тип содержимого документа.
### getCount() {#getCount}
```
public int getCount()
```


Получает количество элементов в коллекции.

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

**Returns:**
int - Количество элементов в коллекции.
### getCreatedTime() {#getCreatedTime}
```
public Date getCreatedTime()
```


Получает дату создания документа в UTC.

 **Remarks:** 

Для документов, созданных из формата RTF, это свойство возвращает локальное время машины автора в момент создания документа.

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
java.util.Date - Дата создания документа в UTC.
### getHeadingPairs() {#getHeadingPairs}
```
public Object[] getHeadingPairs()
```


Указывает заголовки документа и их названия.

 **Remarks:** 

Каждая пара заголовков занимает два элемента в этом массиве.

Первый элемент пары — это java.lang.String, указывающий имя заголовка. Второй элемент пары — это int, указывающий количество частей документа для этого заголовка в свойстве [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String).

Общая сумма количеств для всех пар заголовков в этом свойстве должна быть равна количеству элементов в свойстве [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String).

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает взаимосвязь между свойствами "HeadingPairs" и "TitlesOfParts".

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
java.lang.Object[] - Соответствующее значение java.lang.Object[].
### getHyperlinkBase() {#getHyperlinkBase}
```
public String getHyperlinkBase()
```


Указывает базовую строку, используемую для оценки относительных гиперссылок в этом документе.

 **Remarks:** 

Aspose.Words не использует это свойство.

 **Examples:** 

Показывает, как сохранить базовую часть гиперссылки в свойствах документа.

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
java.lang.String - Соответствующее значение java.lang.String.
### getHyperlinksChanged() {#getHyperlinksChanged}
```
public boolean getHyperlinksChanged()
```


Указывает, были ли изменены гиперссылки в документе.

 **Remarks:** 

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как получить расширенные свойства.

```

 Document doc = new Document(getMyDir() + "Extended properties.docx");
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getScaleCrop());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getSharedDocument());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getHyperlinksChanged());
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getKeywords() {#getKeywords}
```
public String getKeywords()
```


Получает ключевые слова документа.

 **Examples:** 

Показывает, как работать со встроенными свойствами документа в категории "Description".

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
java.lang.String - Ключевые слова документа.
### getLastPrinted() {#getLastPrinted}
```
public Date getLastPrinted()
```


Получает дату последней печати документа в UTC.

 **Remarks:** 

Для документов, созданных из формата RTF, это свойство возвращает локальное время последней операции печати.

Если документ никогда не печатался, это свойство вернёт DateTime.MinValue.

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
java.util.Date - Дата последней печати документа в UTC.
### getLastSavedBy() {#getLastSavedBy}
```
public String getLastSavedBy()
```


Получает имя последнего автора.

 **Remarks:** 

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
java.lang.String - Имя последнего автора.
### getLastSavedTime() {#getLastSavedTime}
```
public Date getLastSavedTime()
```


Получает время последнего сохранения в UTC.

 **Remarks:** 

Для документов, созданных из формата RTF, это свойство возвращает локальное время последней операции сохранения.

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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

Показывает, как использовать поле SAVEDATE для отображения даты/времени последней операции сохранения документа, выполненной с помощью Microsoft Word.

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
java.util.Date - Время последнего сохранения в UTC.
### getLines() {#getLines}
```
public int getLines()
```


Представляет оценку количества строк в документе.

 **Remarks:** 

Aspose.Words обновляет это свойство, когда вы вызываете [Document.updateWordCount(boolean)](../../com.aspose.words/document/\#updateWordCount-boolean).

 **Examples:** 

Показывает, как обновить все метки списков в документе.

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

Показывает, как работать со свойствами документа в категории "Content".

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
int — соответствующее значение  int .
### getLinksUpToDate() {#getLinksUpToDate}
```
public boolean getLinksUpToDate()
```


Указывает, актуальны ли гиперссылки в документе.

 **Remarks:** 

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Content".

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
boolean - Соответствующее  boolean  значение.
### getManager() {#getManager}
```
public String getManager()
```


Получает свойство manager.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
java.lang.String - Свойство менеджера.
### getNameOfApplication() {#getNameOfApplication}
```
public String getNameOfApplication()
```


Получает имя приложения.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
java.lang.String - Имя приложения.
### getPages() {#getPages}
```
public int getPages()
```


Представляет оценку количества страниц в документе.

 **Remarks:** 

Aspose.Words обновляет это свойство, когда вы вызываете [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Content".

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
int — соответствующее значение  int .
### getParagraphs() {#getParagraphs}
```
public int getParagraphs()
```


Представляет оценку количества абзацев в документе.

 **Remarks:** 

Aspose.Words обновляет это свойство, когда вы вызываете [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Показывает, как обновить все метки списков в документе.

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

Показывает, как работать со свойствами документа в категории "Content".

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
int — соответствующее значение  int .
### getRevisionNumber() {#getRevisionNumber}
```
public int getRevisionNumber()
```


Получает номер ревизии документа.

 **Remarks:** 

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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

Показывает, как работать с полями REVNUM.

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
int - Номер ревизии документа.
### getScaleCrop() {#getScaleCrop}
```
public boolean getScaleCrop()
```


Указывает, обрезан ли миниатюрный образ документа или масштабирован для соответствия дисплею.

 **Remarks:** 

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как получить расширенные свойства.

```

 Document doc = new Document(getMyDir() + "Extended properties.docx");
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getScaleCrop());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getSharedDocument());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getHyperlinksChanged());
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getSecurity() {#getSecurity}
```
public int getSecurity()
```


Указывает уровень безопасности документа в виде числового значения.

 **Remarks:** 

Используйте это свойство только в информационных целях, поскольку Microsoft Word не всегда устанавливает его. Это свойство доступно только в документах DOC и OOXML.

Чтобы защитить или снять защиту с документа, используйте методы **M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** и [Document.unprotect()](../../com.aspose.words/document/\#unprotect).

Aspose.Words обновляет это свойство до правильного значения перед сохранением документа.

 **Examples:** 

Показывает, как использовать свойства документа для отображения уровня безопасности документа.

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
int - Соответствующее значение int. Возвращаемое значение представляет собой побитовое сочетание констант [DocumentSecurity](../../com.aspose.words/documentsecurity/).
### getSharedDocument() {#getSharedDocument}
```
public boolean getSharedDocument()
```


Указывает, является ли документ общим.

 **Remarks:** 

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как получить расширенные свойства.

```

 Document doc = new Document(getMyDir() + "Extended properties.docx");
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getScaleCrop());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getSharedDocument());
 Assert.assertTrue(doc.getBuiltInDocumentProperties().getHyperlinksChanged());
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getSubject() {#getSubject}
```
public String getSubject()
```


Получает тему документа.

 **Examples:** 

Показывает, как работать со встроенными свойствами документа в категории "Description".

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
java.lang.String - Тема документа.
### getTemplate() {#getTemplate}
```
public String getTemplate()
```


Получает информационное имя шаблона документа.

 **Remarks:** 

В Microsoft Word это свойство предназначено только для информационных целей и обычно содержит только имя файла шаблона без пути.

Пустая строка означает, что документ привязан к шаблону Normal.

Чтобы получить или установить фактическое имя прикреплённого шаблона, используйте свойство [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String).

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
java.lang.String - Информационное имя шаблона документа.
### getThumbnail() {#getThumbnail}
```
public byte[] getThumbnail()
```


Получает или задает миниатюру документа.

**Returns:**
byte[] — соответствующее значение byte[].
### getTitle() {#getTitle}
```
public String getTitle()
```


Получает заголовок документа.

 **Examples:** 

Показывает, как работать со встроенными свойствами документа в категории "Description".

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
java.lang.String - Заголовок документа.
### getTitlesOfParts() {#getTitlesOfParts}
```
public String[] getTitlesOfParts()
```


Каждая строка в массиве указывает имя части документа.

 **Remarks:** 

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает взаимосвязь между свойствами "HeadingPairs" и "TitlesOfParts".

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
java.lang.String[] - Соответствующее значение java.lang.String[].
### getTotalEditingTime() {#getTotalEditingTime}
```
public int getTotalEditingTime()
```


Получает общее время редактирования в минутах.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
int - Общее время редактирования в минутах.
### getVersion() {#getVersion}
```
public int getVersion()
```


Представляет номер версии приложения, создавшего документ.

 **Remarks:** 

Когда документ создан в Microsoft Word, старшие 16 бит представляют основную версию, а младшие 16 бит — номер сборки.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
int — соответствующее значение  int .
### getWords() {#getWords}
```
public int getWords()
```


Представляет оценку количества слов в документе.

 **Remarks:** 

Aspose.Words обновляет это свойство, когда вы вызываете [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Показывает, как обновить все метки списков в документе.

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

Показывает, как работать со свойствами документа в категории "Content".

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
int — соответствующее значение  int .
### indexOf(String name) {#indexOf-java.lang.String}
```
public int indexOf(String name)
```


Получает индекс свойства по имени.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя свойства без учета регистра. |

**Returns:**
int - Индекс, начинающийся с нуля. Отрицательное значение, если не найден.
### iterator() {#iterator}
```
public Iterator iterator()
```


Возвращает объект-итератор, который можно использовать для перебора всех элементов в коллекции.

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
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Удаляет свойство с указанным именем из коллекции.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя свойства без учета регистра. |

### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Удаляет свойство по указанному индексу.

 **Remarks:** 

**Note:**  In Java this method is slow because iterates over all nodes.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| индекс | int | Нулевой индекс. |

### setAuthor(String value) {#setAuthor-java.lang.String}
```
public void setAuthor(String value)
```


Устанавливает имя автора документа.

 **Examples:** 

Показывает, как работать со встроенными свойствами документа в категории "Description".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя автора документа. |

### setBytes(int value) {#setBytes-int}
```
public void setBytes(int value)
```


Представляет оценку количества байтов в документе.

 **Remarks:** 

Microsoft Word не всегда устанавливает это свойство.

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Content".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

### setCategory(String value) {#setCategory-java.lang.String}
```
public void setCategory(String value)
```


Устанавливает категорию документа.

 **Examples:** 

Показывает, как работать со встроенными свойствами документа в категории "Description".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Категория документа. |

### setCharacters(int value) {#setCharacters-int}
```
public void setCharacters(int value)
```


Представляет оценку количества символов в документе.

 **Remarks:** 

Aspose.Words обновляет это свойство, когда вы вызываете [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Показывает, как обновить все метки списков в документе.

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

Показывает, как работать со свойствами документа в категории "Content".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

### setCharactersWithSpaces(int value) {#setCharactersWithSpaces-int}
```
public void setCharactersWithSpaces(int value)
```


Представляет оценку количества символов (включая пробелы) в документе.

 **Remarks:** 

Aspose.Words обновляет это свойство, когда вы вызываете [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Content".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

### setComments(String value) {#setComments-java.lang.String}
```
public void setComments(String value)
```


Устанавливает комментарии к документу.

 **Examples:** 

Показывает, как работать со встроенными свойствами документа в категории "Description".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Комментарии к документу. |

### setCompany(String value) {#setCompany-java.lang.String}
```
public void setCompany(String value)
```


Устанавливает свойство компании.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Свойство компании. |

### setContentStatus(String value) {#setContentStatus-java.lang.String}
```
public void setContentStatus(String value)
```


Устанавливает статус содержимого документа.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Content".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Статус содержимого документа. |

### setContentType(String value) {#setContentType-java.lang.String}
```
public void setContentType(String value)
```


Устанавливает тип содержимого документа.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Content".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Тип содержимого документа. |

### setCreatedTime(Date value) {#setCreatedTime-java.util.Date}
```
public void setCreatedTime(Date value)
```


Устанавливает дату создания документа в UTC.

 **Remarks:** 

Для документов, созданных из формата RTF, это свойство возвращает локальное время машины автора в момент создания документа.

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.util.Date | Дата создания документа в UTC. |

### setHeadingPairs(Object[] value) {#setHeadingPairs-java.lang.Object}
```
public void setHeadingPairs(Object[] value)
```


Указывает заголовки документа и их названия.

 **Remarks:** 

Каждая пара заголовков занимает два элемента в этом массиве.

Первый элемент пары — это java.lang.String, указывающий имя заголовка. Второй элемент пары — это int, указывающий количество частей документа для этого заголовка в свойстве [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String).

Общая сумма количеств для всех пар заголовков в этом свойстве должна быть равна количеству элементов в свойстве [getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties/\#getTitlesOfParts) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties/\#setTitlesOfParts-java.lang.String).

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает взаимосвязь между свойствами "HeadingPairs" и "TitlesOfParts".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.Object[] | Соответствующее значение java.lang.Object[]. |

### setHyperlinkBase(String value) {#setHyperlinkBase-java.lang.String}
```
public void setHyperlinkBase(String value)
```


Указывает базовую строку, используемую для оценки относительных гиперссылок в этом документе.

 **Remarks:** 

Aspose.Words не использует это свойство.

 **Examples:** 

Показывает, как сохранить базовую часть гиперссылки в свойствах документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setKeywords(String value) {#setKeywords-java.lang.String}
```
public void setKeywords(String value)
```


Устанавливает ключевые слова документа.

 **Examples:** 

Показывает, как работать со встроенными свойствами документа в категории "Description".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Ключевые слова документа. |

### setLastPrinted(Date value) {#setLastPrinted-java.util.Date}
```
public void setLastPrinted(Date value)
```


Устанавливает дату последней печати документа в UTC.

 **Remarks:** 

Для документов, созданных из формата RTF, это свойство возвращает локальное время последней операции печати.

Если документ никогда не печатался, это свойство вернёт DateTime.MinValue.

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.util.Date | Дата последней печати документа в UTC. |

### setLastSavedBy(String value) {#setLastSavedBy-java.lang.String}
```
public void setLastSavedBy(String value)
```


Устанавливает имя последнего автора.

 **Remarks:** 

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя последнего автора. |

### setLastSavedTime(Date value) {#setLastSavedTime-java.util.Date}
```
public void setLastSavedTime(Date value)
```


Устанавливает время последнего сохранения в UTC.

 **Remarks:** 

Для документов, созданных из формата RTF, это свойство возвращает локальное время последней операции сохранения.

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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

Показывает, как использовать поле SAVEDATE для отображения даты/времени последней операции сохранения документа, выполненной с помощью Microsoft Word.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.util.Date | Время последнего сохранения в UTC. |

### setLines(int value) {#setLines-int}
```
public void setLines(int value)
```


Представляет оценку количества строк в документе.

 **Remarks:** 

Aspose.Words обновляет это свойство, когда вы вызываете [Document.updateWordCount(boolean)](../../com.aspose.words/document/\#updateWordCount-boolean).

 **Examples:** 

Показывает, как обновить все метки списков в документе.

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

Показывает, как работать со свойствами документа в категории "Content".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

### setLinksUpToDate(boolean value) {#setLinksUpToDate-boolean}
```
public void setLinksUpToDate(boolean value)
```


Указывает, актуальны ли гиперссылки в документе.

 **Remarks:** 

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Content".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setManager(String value) {#setManager-java.lang.String}
```
public void setManager(String value)
```


Устанавливает свойство менеджера.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Свойство менеджера. |

### setNameOfApplication(String value) {#setNameOfApplication-java.lang.String}
```
public void setNameOfApplication(String value)
```


Устанавливает имя приложения.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя приложения. |

### setPages(int value) {#setPages-int}
```
public void setPages(int value)
```


Представляет оценку количества страниц в документе.

 **Remarks:** 

Aspose.Words обновляет это свойство, когда вы вызываете [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Content".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

### setParagraphs(int value) {#setParagraphs-int}
```
public void setParagraphs(int value)
```


Представляет оценку количества абзацев в документе.

 **Remarks:** 

Aspose.Words обновляет это свойство, когда вы вызываете [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Показывает, как обновить все метки списков в документе.

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

Показывает, как работать со свойствами документа в категории "Content".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

### setRevisionNumber(int value) {#setRevisionNumber-int}
```
public void setRevisionNumber(int value)
```


Устанавливает номер ревизии документа.

 **Remarks:** 

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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

Показывает, как работать с полями REVNUM.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Номер редакции документа. |

### setSecurity(int value) {#setSecurity-int}
```
public void setSecurity(int value)
```


Указывает уровень безопасности документа в виде числового значения.

 **Remarks:** 

Используйте это свойство только в информационных целях, поскольку Microsoft Word не всегда устанавливает его. Это свойство доступно только в документах DOC и OOXML.

Чтобы защитить или снять защиту с документа, используйте методы **M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** и [Document.unprotect()](../../com.aspose.words/document/\#unprotect).

Aspose.Words обновляет это свойство до правильного значения перед сохранением документа.

 **Examples:** 

Показывает, как использовать свойства документа для отображения уровня безопасности документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее значение  int . Значение должно быть побитовой комбинацией констант [DocumentSecurity](../../com.aspose.words/documentsecurity/). |

### setSubject(String value) {#setSubject-java.lang.String}
```
public void setSubject(String value)
```


Устанавливает тему документа.

 **Examples:** 

Показывает, как работать со встроенными свойствами документа в категории "Description".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Тема документа. |

### setTemplate(String value) {#setTemplate-java.lang.String}
```
public void setTemplate(String value)
```


Устанавливает информационное имя шаблона документа.

 **Remarks:** 

В Microsoft Word это свойство предназначено только для информационных целей и обычно содержит только имя файла шаблона без пути.

Пустая строка означает, что документ привязан к шаблону Normal.

Чтобы получить или установить фактическое имя прикреплённого шаблона, используйте свойство [Document.getAttachedTemplate()](../../com.aspose.words/document/\#getAttachedTemplate) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document/\#setAttachedTemplate-java.lang.String).

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Информационное имя шаблона документа. |

### setThumbnail(byte[] value) {#setThumbnail-byte}
```
public void setThumbnail(byte[] value)
```


Получает или задает миниатюру документа.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | byte[] | Соответствующее значение byte[]. |

### setTitle(String value) {#setTitle-java.lang.String}
```
public void setTitle(String value)
```


Устанавливает заголовок документа.

 **Examples:** 

Показывает, как работать со встроенными свойствами документа в категории "Description".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Заголовок документа. |

### setTitlesOfParts(String[] value) {#setTitlesOfParts-java.lang.String}
```
public void setTitlesOfParts(String[] value)
```


Каждая строка в массиве указывает имя части документа.

 **Remarks:** 

Aspose.Words не обновляет это свойство.

 **Examples:** 

Показывает взаимосвязь между свойствами "HeadingPairs" и "TitlesOfParts".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String[] | Соответствующее значение java.lang.String[]. |

### setTotalEditingTime(int value) {#setTotalEditingTime-int}
```
public void setTotalEditingTime(int value)
```


Устанавливает общее время редактирования в минутах.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Общее время редактирования в минутах. |

### setVersion(int value) {#setVersion-int}
```
public void setVersion(int value)
```


Представляет номер версии приложения, создавшего документ.

 **Remarks:** 

Когда документ создан в Microsoft Word, старшие 16 бит представляют основную версию, а младшие 16 бит — номер сборки.

 **Examples:** 

Показывает, как работать со свойствами документа в категории "Origin".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

### setWords(int value) {#setWords-int}
```
public void setWords(int value)
```


Представляет оценку количества слов в документе.

 **Remarks:** 

Aspose.Words обновляет это свойство, когда вы вызываете [Document.updateWordCount()](../../com.aspose.words/document/\#updateWordCount).

 **Examples:** 

Показывает, как обновить все метки списков в документе.

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

Показывает, как работать со свойствами документа в категории "Content".

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

