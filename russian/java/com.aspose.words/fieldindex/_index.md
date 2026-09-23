---
title: "FieldIndex"
linktitle: "FieldIndex"
second_title: "Aspose.Words для Java"
description: "Реализует поле INDEX на Java."
type: docs
weight: 249
url: /ru/java/com.aspose.words/fieldindex/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldIndex extends Field
```

Реализует поле INDEX.

Чтобы узнать больше, посетите статью документации [ Working with Fields ][Working with Fields].

 **Remarks:** 

Создаёт указатель, используя записи указателя, указанные полями XE, и вставляет этот указатель в данное место документа.

 **Examples:** 

Показывает, как создать поле INDEX, а затем использовать поля XE для заполнения его записями.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side
 // and the page containing the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // Configure the INDEX field only to display XE fields that are within the bounds
 // of a bookmark named "MainBookmark", and whose "EntryType" properties have a value of "A".
 // For both INDEX and XE fields, the "EntryType" property only uses the first character of its string value.
 index.setBookmarkName("MainBookmark");
 index.setEntryType("A");

 Assert.assertEquals(" INDEX  \\b MainBookmark \\f A", index.getFieldCode());

 // On a new page, start the bookmark with a name that matches the value
 // of the INDEX field's "BookmarkName" property.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("MainBookmark");

 // The INDEX field will pick up this entry because it is inside the bookmark,
 // and its entry type also matches the INDEX field's entry type.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 1");
 indexEntry.setEntryType("A");

 Assert.assertEquals(" XE  \"Index entry 1\" \\f A", indexEntry.getFieldCode());

 // Insert an XE field that will not appear in the INDEX because the entry types do not match.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 2");
 indexEntry.setEntryType("B");

 // End the bookmark and insert an XE field afterwards.
 // It is of the same type as the INDEX field, but will not appear
 // since it is outside the bookmark's boundaries.
 builder.endBookmark("MainBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 3");
 indexEntry.setEntryType("A");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Filtering.docx");
 
```

Показывает, как заполнить поле INDEX записями с помощью полей XE, а также изменить его внешний вид.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Методы

| Метод | Описание |
| --- | --- |
| [getBookmarkName()](#getBookmarkName) | Получает имя закладки, отмечающей часть документа, используемую для построения указателя. |
| [getCrossReferenceSeparator()](#getCrossReferenceSeparator) | Получает последовательность символов, используемую для разделения перекрёстных ссылок и других записей. |
| [getDisplayResult()](#getDisplayResult) | Получает текст, представляющий отображаемый результат поля. |
| [getEnd()](#getEnd) | Получает узел, представляющий конец поля. |
| [getEntryType()](#getEntryType) | Получает тип записи указателя, используемый для построения указателя. |
| [getFieldCode()](#getFieldCode) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [getFormat()](#getFormat) | Получает объект [FieldFormat](../../com.aspose.words/fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [getHeading()](#getHeading) | Получает заголовок, который появляется в начале каждого набора записей для любой заданной буквы. |
| [getLanguageId()](#getLanguageId) | Получает идентификатор языка, используемый для создания указателя. |
| [getLetterRange()](#getLetterRange) | Получает диапазон букв, которым ограничивается указатель. |
| [getLocaleId()](#getLocaleId) | Получает LCID поля. |
| [getNumberOfColumns()](#getNumberOfColumns) | Получает количество столбцов на странице, используемых при построении указателя. |
| [getPageNumberListSeparator()](#getPageNumberListSeparator) | Получает последовательность символов, используемую для разделения двух номеров страниц в списке номеров страниц. |
| [getPageNumberSeparator()](#getPageNumberSeparator) | Получает последовательность символов, используемую для разделения записи указателя и её номера страницы. |
| [getPageRangeSeparator()](#getPageRangeSeparator) | Получает последовательность символов, используемую для разделения начала и конца диапазона страниц. |
| [getResult()](#getResult) | Получает текст, находящийся между разделителем поля и концом поля. |
| [getRunSubentriesOnSameLine()](#getRunSubentriesOnSameLine) | Получает, следует ли размещать подпункты в той же строке, что и основной пункт. |
| [getSeparator()](#getSeparator) | Получает узел, представляющий разделитель поля. |
| [getSequenceName()](#getSequenceName) | Получает имя последовательности, номер которой включён в номер страницы. |
| [getSequenceSeparator()](#getSequenceSeparator) | Получает последовательность символов, используемую для разделения номеров последовательностей и номеров страниц. |
| [getStart()](#getStart) | Получает узел, представляющий начало поля. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getType()](#getType) | Получает тип поля Microsoft Word. |
| [getUseYomi()](#getUseYomi) | Получает, следует ли включить использование йоми‑текста для записей указателя. |
| [hasPageNumberSeparator()](#hasPageNumberSeparator) | Получает значение, указывающее, переопределён ли разделитель номера страницы через код поля. |
| [hasSequenceName()](#hasSequenceName) | Получает значение, указывающее, следует ли использовать последовательность при построении результата поля. |
| [isDirty()](#isDirty) | Определяет, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [isDirty(boolean value)](#isDirty-boolean) | Устанавливает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [isLocked()](#isLocked) | Определяет, заблокировано ли поле (не должно пересчитывать свой результат). |
| [isLocked(boolean value)](#isLocked-boolean) | Устанавливает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [remove()](#remove) | Удаляет поле из документа. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String) | Устанавливает имя закладки, отмечающей часть документа, используемую для построения указателя. |
| [setCrossReferenceSeparator(String value)](#setCrossReferenceSeparator-java.lang.String) | Устанавливает последовательность символов, используемую для разделения перекрёстных ссылок и других записей. |
| [setEntryType(String value)](#setEntryType-java.lang.String) | Устанавливает тип записи указателя, используемый для построения указателя. |
| [setHeading(String value)](#setHeading-java.lang.String) | Устанавливает заголовок, который появляется в начале каждого набора записей для любой заданной буквы. |
| [setLanguageId(String value)](#setLanguageId-java.lang.String) | Устанавливает идентификатор языка, используемый для создания указателя. |
| [setLetterRange(String value)](#setLetterRange-java.lang.String) | Устанавливает диапазон букв, которым ограничивается указатель. |
| [setLocaleId(int value)](#setLocaleId-int) | Устанавливает LCID поля. |
| [setNumberOfColumns(String value)](#setNumberOfColumns-java.lang.String) | Устанавливает количество столбцов на странице, используемых при построении указателя. |
| [setPageNumberListSeparator(String value)](#setPageNumberListSeparator-java.lang.String) | Устанавливает последовательность символов, используемую для разделения двух номеров страниц в списке номеров страниц. |
| [setPageNumberSeparator(String value)](#setPageNumberSeparator-java.lang.String) | Устанавливает последовательность символов, используемую для разделения записи указателя и её номера страницы. |
| [setPageRangeSeparator(String value)](#setPageRangeSeparator-java.lang.String) | Устанавливает последовательность символов, используемую для разделения начала и конца диапазона страниц. |
| [setResult(String value)](#setResult-java.lang.String) | Устанавливает текст, находящийся между разделителем поля и его концом. |
| [setRunSubentriesOnSameLine(boolean value)](#setRunSubentriesOnSameLine-boolean) | Устанавливает, следует ли размещать подпункты в той же строке, что и основной пункт. |
| [setSequenceName(String value)](#setSequenceName-java.lang.String) | Устанавливает имя последовательности, номер которой включён в номер страницы. |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String) | Устанавливает последовательность символов, используемую для разделения номеров последовательностей и номеров страниц. |
| [setUseYomi(boolean value)](#setUseYomi-boolean) | Устанавливает, следует ли включить использование йоми‑текста для записей указателя. |
| [unlink()](#unlink) | Выполняет разъединение поля. |
| [update()](#update) | Выполняет обновление поля. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Выполняет обновление поля. |
### getBookmarkName() {#getBookmarkName}
```
public String getBookmarkName()
```


Получает имя закладки, отмечающей часть документа, используемую для построения указателя.

 **Examples:** 

Показывает, как создать поле INDEX, а затем использовать поля XE для заполнения его записями.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side
 // and the page containing the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // Configure the INDEX field only to display XE fields that are within the bounds
 // of a bookmark named "MainBookmark", and whose "EntryType" properties have a value of "A".
 // For both INDEX and XE fields, the "EntryType" property only uses the first character of its string value.
 index.setBookmarkName("MainBookmark");
 index.setEntryType("A");

 Assert.assertEquals(" INDEX  \\b MainBookmark \\f A", index.getFieldCode());

 // On a new page, start the bookmark with a name that matches the value
 // of the INDEX field's "BookmarkName" property.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("MainBookmark");

 // The INDEX field will pick up this entry because it is inside the bookmark,
 // and its entry type also matches the INDEX field's entry type.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 1");
 indexEntry.setEntryType("A");

 Assert.assertEquals(" XE  \"Index entry 1\" \\f A", indexEntry.getFieldCode());

 // Insert an XE field that will not appear in the INDEX because the entry types do not match.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 2");
 indexEntry.setEntryType("B");

 // End the bookmark and insert an XE field afterwards.
 // It is of the same type as the INDEX field, but will not appear
 // since it is outside the bookmark's boundaries.
 builder.endBookmark("MainBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 3");
 indexEntry.setEntryType("A");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Filtering.docx");
 
```

**Returns:**
java.lang.String - Имя закладки, отмечающей часть документа, используемую для построения указателя.
### getCrossReferenceSeparator() {#getCrossReferenceSeparator}
```
public String getCrossReferenceSeparator()
```


Получает последовательность символов, используемую для разделения перекрёстных ссылок и других записей.

 **Examples:** 

Показывает, как определить перекрестные ссылки в поле INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // We can configure an XE field to get its INDEX entry to display a string instead of a page number.
 // First, for entries that substitute a page number with a string,
 // specify a custom separator between the XE field's Text property value and the string.
 index.setCrossReferenceSeparator(", see: ");

 Assert.assertEquals(" INDEX  \\k \", see: \"", index.getFieldCode());

 // Insert an XE field, which creates a regular INDEX entry which displays this field's page number,
 // and does not invoke the CrossReferenceSeparator value.
 // The entry for this XE field will display "Apple, 2".
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");

 Assert.assertEquals(" XE  Apple", indexEntry.getFieldCode());

 // Insert another XE field on page 3 and set a value for the PageNumberReplacement property.
 // This value will show up instead of the number of the page that this field is on,
 // and the INDEX field's CrossReferenceSeparator value will appear in front of it.
 // The entry for this XE field will display "Banana, see: Tropical fruit".
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");
 indexEntry.setPageNumberReplacement("Tropical fruit");

 Assert.assertEquals(" XE  Banana \\t \"Tropical fruit\"", indexEntry.getFieldCode());

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.CrossReferenceSeparator.docx");
 
```

**Returns:**
java.lang.String - Последовательность символов, используемая для разделения перекрёстных ссылок и других записей.
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


Получает текст, представляющий отображаемый результат поля.

 **Remarks:** 

Метод [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) должен быть вызван для получения корректного значения полей [FieldListNum](../../com.aspose.words/fieldlistnum/), [FieldAutoNum](../../com.aspose.words/fieldautonum/), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout/) и [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl/).

 **Examples:** 

Показывает, как получить реальный текст, который поле отображает в документе.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("This document was written by ");
 FieldAuthor fieldAuthor = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);
 fieldAuthor.setAuthorName("John Doe");

 // We can use the DisplayResult property to verify what exact text
 // a field would display in its place in the document.
 Assert.assertEquals("", fieldAuthor.getDisplayResult());

 // Fields do not maintain accurate result values in real-time.
 // To make sure our fields display accurate results at any given time,
 // such as right before a save operation, we need to update them manually.
 fieldAuthor.update();

 Assert.assertEquals("John Doe", fieldAuthor.getDisplayResult());

 doc.save(getArtifactsDir() + "Field.DisplayResult.docx");
 
```

**Returns:**
java.lang.String — Текст, представляющий отображаемый результат поля.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Получает узел, представляющий конец поля.

 **Examples:** 

Показывает, как работать с коллекцией полей.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldEnd](../../com.aspose.words/fieldend/) - The node that represents the field end.
### getEntryType() {#getEntryType}
```
public String getEntryType()
```


Получает тип записи указателя, используемый для построения указателя.

 **Examples:** 

Показывает, как создать поле INDEX, а затем использовать поля XE для заполнения его записями.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side
 // and the page containing the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // Configure the INDEX field only to display XE fields that are within the bounds
 // of a bookmark named "MainBookmark", and whose "EntryType" properties have a value of "A".
 // For both INDEX and XE fields, the "EntryType" property only uses the first character of its string value.
 index.setBookmarkName("MainBookmark");
 index.setEntryType("A");

 Assert.assertEquals(" INDEX  \\b MainBookmark \\f A", index.getFieldCode());

 // On a new page, start the bookmark with a name that matches the value
 // of the INDEX field's "BookmarkName" property.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("MainBookmark");

 // The INDEX field will pick up this entry because it is inside the bookmark,
 // and its entry type also matches the INDEX field's entry type.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 1");
 indexEntry.setEntryType("A");

 Assert.assertEquals(" XE  \"Index entry 1\" \\f A", indexEntry.getFieldCode());

 // Insert an XE field that will not appear in the INDEX because the entry types do not match.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 2");
 indexEntry.setEntryType("B");

 // End the bookmark and insert an XE field afterwards.
 // It is of the same type as the INDEX field, but will not appear
 // since it is outside the bookmark's boundaries.
 builder.endBookmark("MainBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 3");
 indexEntry.setEntryType("A");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Filtering.docx");
 
```

**Returns:**
java.lang.String - Тип записи указателя, используемый для построения указателя.
### getFieldCode() {#getFieldCode}
```
public String getFieldCode()
```


Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат дочерних полей.

 **Examples:** 

Показывает, как вставить поле в документ, используя код поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Показывает, как получить код поля.

```

 // Open a document which contains a MERGEFIELD inside an IF field.
 Document doc = new Document(getMyDir() + "Nested fields.docx");
 FieldIf fieldIf = (FieldIf) doc.getRange().getFields().get(0);

 // There are two ways of getting a field's field code:
 // 1 -  Omit its inner fields:
 Assert.assertEquals(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.getFieldCode(false));

 // 2 -  Include its inner fields:
 Assert.assertEquals(" IF  MERGEFIELD NetIncome  > 0 \" (surplus of  MERGEFIELD  NetIncome \\f $ ) \" \"\" ",
         fieldIf.getFieldCode(true));

 // By default, the GetFieldCode method displays inner fields.
 Assert.assertEquals(fieldIf.getFieldCode(), fieldIf.getFieldCode(true));
 
```

**Returns:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует).

 **Examples:** 

Показывает, как получить код поля.

```

 // Open a document which contains a MERGEFIELD inside an IF field.
 Document doc = new Document(getMyDir() + "Nested fields.docx");
 FieldIf fieldIf = (FieldIf) doc.getRange().getFields().get(0);

 // There are two ways of getting a field's field code:
 // 1 -  Omit its inner fields:
 Assert.assertEquals(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.getFieldCode(false));

 // 2 -  Include its inner fields:
 Assert.assertEquals(" IF  MERGEFIELD NetIncome  > 0 \" (surplus of  MERGEFIELD  NetIncome \\f $ ) \" \"\" ",
         fieldIf.getFieldCode(true));

 // By default, the GetFieldCode method displays inner fields.
 Assert.assertEquals(fieldIf.getFieldCode(), fieldIf.getFieldCode(true));
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| includeChildFieldCodes | boolean | true, если коды дочерних полей должны быть включены. |

**Returns:**
java.lang.String
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Получает объект [FieldFormat](../../com.aspose.words/fieldformat/), который предоставляет типизированный доступ к форматированию поля.

 **Examples:** 

Показывает, как форматировать результаты полей.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a document builder to insert a field that displays a result with no format applied.
 Field field = builder.insertField("= 2 + 3");

 Assert.assertEquals("= 2 + 3", field.getFieldCode());
 Assert.assertEquals("5", field.getResult());

 // We can apply a format to a field's result using the field's properties.
 // Below are three types of formats that we can apply to a field's result.
 // 1 -  Numeric format:
 FieldFormat format = field.getFormat();
 format.setNumericFormat("$###.00");
 field.update();

 Assert.assertEquals("= 2 + 3 \\# $###.00", field.getFieldCode());
 Assert.assertEquals("$  5.00", field.getResult());

 // 2 -  Date/time format:
 field = builder.insertField("DATE");
 format = field.getFormat();
 format.setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 Assert.assertEquals("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());
 System.out.println("Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

 // 3 -  General format:
 field = builder.insertField("= 25 + 33");
 format = field.getFormat();
 format.getGeneralFormats().add(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().add(GeneralFormat.UPPER);
 field.update();

 int index = 0;
 Iterator generalFormatEnumerator = format.getGeneralFormats().iterator();
 while (generalFormatEnumerator.hasNext()) {
     int value = generalFormatEnumerator.next();
     System.out.println(MessageFormat.format("General format index {0}: {1}", index++, value));
 }

 Assert.assertEquals("= 25 + 33 \\* roman \\* Upper", field.getFieldCode());
 Assert.assertEquals("LVIII", field.getResult());
 Assert.assertEquals(2, format.getGeneralFormats().getCount());
 Assert.assertEquals(GeneralFormat.LOWERCASE_ROMAN, format.getGeneralFormats().get(0));

 // We can remove our formats to revert the field's result to its original form.
 format.getGeneralFormats().remove(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().removeAt(0);
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 field.update();

 Assert.assertEquals("= 25 + 33  ", field.getFieldCode());
 Assert.assertEquals("58", field.getResult());
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 
```

**Returns:**
[FieldFormat](../../com.aspose.words/fieldformat/) - A [FieldFormat](../../com.aspose.words/fieldformat/) object that provides typed access to field's formatting.
### getHeading() {#getHeading}
```
public String getHeading()
```


Получает заголовок, который появляется в начале каждого набора записей для любой заданной буквы.

 **Examples:** 

Показывает, как заполнить поле INDEX записями с помощью полей XE, а также изменить его внешний вид.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Returns:**
java.lang.String - Заголовок, который появляется в начале каждого набора записей для любой заданной буквы.
### getLanguageId() {#getLanguageId}
```
public String getLanguageId()
```


Получает идентификатор языка, используемый для создания указателя.

 **Examples:** 

Показывает, как заполнить поле INDEX записями с помощью полей XE, а также изменить его внешний вид.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Returns:**
java.lang.String - Идентификатор языка, используемый для создания указателя.
### getLetterRange() {#getLetterRange}
```
public String getLetterRange()
```


Получает диапазон букв, которым ограничивается указатель.

 **Examples:** 

Показывает, как заполнить поле INDEX записями с помощью полей XE, а также изменить его внешний вид.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Returns:**
java.lang.String - Диапазон букв, которым ограничивается указатель.
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Получает LCID поля.

 **Examples:** 

Показывает, как вставить поле и работать с его локалью.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a DATE field, and then print the date it will display.
 // Your thread's current culture determines the formatting of the date.
 Field field = builder.insertField("DATE");
 System.out.println(MessageFormat.format("Today''s date, as displayed in the \"{0}\" culture: {1}", Locale.getDefault().getDisplayLanguage(), field.getResult()));

 Assert.assertEquals(1033, field.getLocaleId());
 // Changing the culture of our thread will impact the result of the DATE field.
 // Another way to get the DATE field to display a date in a different culture is to use its LocaleId property.
 // This way allows us to avoid changing the thread's culture to get this effect.
 doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);
 CultureInfo de = new CultureInfo("de-DE");
 field.setLocaleId(1031);
 field.update();

 System.out.println(MessageFormat.format("Today''s date, as displayed according to the \"{0}\" culture: {1}", Locale.forLanguageTag(LocaleUtil.getLocaleFromLCID(field.getLocaleId())).getDisplayLanguage(), field.getResult()));
 
```

**Returns:**
int - LCID поля.
### getNumberOfColumns() {#getNumberOfColumns}
```
public String getNumberOfColumns()
```


Получает количество столбцов на странице, используемых при построении указателя.

 **Examples:** 

Показывает, как заполнить поле INDEX записями с помощью полей XE, а также изменить его внешний вид.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Returns:**
java.lang.String - Количество колонок на страницу, используемых при построении указателя.
### getPageNumberListSeparator() {#getPageNumberListSeparator}
```
public String getPageNumberListSeparator()
```


Получает последовательность символов, используемую для разделения двух номеров страниц в списке номеров страниц.

 **Examples:** 

Показывает, как изменить разделитель номеров страниц в поле INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // If our INDEX field has an entry for a group of XE fields,
 // this entry will display the number of each page that contains an XE field that belongs to this group.
 // We can set custom separators to customize the appearance of these page numbers.
 index.setPageNumberSeparator(", on page(s) ");
 index.setPageNumberListSeparator(" & ");

 Assert.assertEquals(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.getFieldCode());
 Assert.assertTrue(index.hasPageNumberSeparator());

 // After we insert these XE fields, the INDEX field will display "First entry, on page(s) 2 & 3 & 4".
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 Assert.assertEquals(" XE  \"First entry\"", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.PageNumberList.docx");
 
```

**Returns:**
java.lang.String - Последовательность символов, используемая для разделения двух номеров страниц в списке номеров страниц.
### getPageNumberSeparator() {#getPageNumberSeparator}
```
public String getPageNumberSeparator()
```


Получает последовательность символов, используемую для разделения записи указателя и её номера страницы.

 **Examples:** 

Показывает, как изменить разделитель номеров страниц в поле INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // If our INDEX field has an entry for a group of XE fields,
 // this entry will display the number of each page that contains an XE field that belongs to this group.
 // We can set custom separators to customize the appearance of these page numbers.
 index.setPageNumberSeparator(", on page(s) ");
 index.setPageNumberListSeparator(" & ");

 Assert.assertEquals(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.getFieldCode());
 Assert.assertTrue(index.hasPageNumberSeparator());

 // After we insert these XE fields, the INDEX field will display "First entry, on page(s) 2 & 3 & 4".
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 Assert.assertEquals(" XE  \"First entry\"", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.PageNumberList.docx");
 
```

**Returns:**
java.lang.String - Последовательность символов, используемая для разделения записи указателя и её номера страницы.
### getPageRangeSeparator() {#getPageRangeSeparator}
```
public String getPageRangeSeparator()
```


Получает последовательность символов, используемую для разделения начала и конца диапазона страниц.

 **Examples:** 

Показывает, как указать охваченные закладкой страницы в виде диапазона страниц для записи поля INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // For INDEX entries that display page ranges, we can specify a separator string
 // which will appear between the number of the first page, and the number of the last.
 index.setPageNumberSeparator(", on page(s) ");
 index.setPageRangeSeparator(" to ");

 Assert.assertEquals(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("My entry");

 // If an XE field names a bookmark using the PageRangeBookmarkName property,
 // its INDEX entry will show the range of pages that the bookmark spans
 // instead of the number of the page that contains the XE field.
 indexEntry.setPageRangeBookmarkName("MyBookmark");

 Assert.assertEquals(" XE  \"My entry\" \\r MyBookmark", indexEntry.getFieldCode());
 Assert.assertEquals(indexEntry.getPageRangeBookmarkName(), "MyBookmark");

 // Insert a bookmark that starts on page 3 and ends on page 5.
 // The INDEX entry for the XE field that references this bookmark will display this page range.
 // In our table, the INDEX entry will display "My entry, on page(s) 3 to 5".
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("MyBookmark");
 builder.write("Start of MyBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("End of MyBookmark");
 builder.endBookmark("MyBookmark");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.PageRangeBookmark.docx");
 
```

**Returns:**
java.lang.String - Последовательность символов, используемая для разделения начала и конца диапазона страниц.
### getResult() {#getResult}
```
public String getResult()
```


Получает текст, находящийся между разделителем поля и концом поля.

 **Examples:** 

Показывает, как вставить поле в документ, используя код поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
java.lang.String - Текст, который находится между разделителем поля и его концом.
### getRunSubentriesOnSameLine() {#getRunSubentriesOnSameLine}
```
public boolean getRunSubentriesOnSameLine()
```


Получает, следует ли размещать подпункты в той же строке, что и основной пункт.

 **Examples:** 

Показывает, как работать с подзаписями в поле INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setPageNumberSeparator(", see page ");
 index.setHeading("A");

 // XE fields that have a Text property whose value becomes the heading of the INDEX entry.
 // If this value contains two string segments split by a colon (the INDEX entry will treat :) delimiter,
 // the first segment is heading, and the second segment will become the subheading.
 // The INDEX field first groups entries alphabetically, then, if there are multiple XE fields with the same
 // headings, the INDEX field will further subgroup them by the values of these headings.
 // There can be multiple subgrouping layers, depending on how many times
 // the Text properties of XE fields get segmented like this.
 // By default, an INDEX field entry group will create a new line for every subheading within this group.
 // We can set the RunSubentriesOnSameLine flag to true to keep the heading,
 // and every subheading for the group on one line instead, which will make the INDEX field more compact.
 index.setRunSubentriesOnSameLine(runSubentriesOnTheSameLine);

 if (runSubentriesOnTheSameLine)
     Assert.assertEquals(" INDEX  \\e \", see page \" \\h A \\r", index.getFieldCode());
 else
     Assert.assertEquals(" INDEX  \\e \", see page \" \\h A", index.getFieldCode());

 // Insert two XE fields, each on a new page, and with the same heading named "Heading 1",
 // which the INDEX field will use to group them.
 // If RunSubentriesOnSameLine is false, then the INDEX table will create three lines:
 // one line for the grouping heading "Heading 1", and one more line for each subheading.
 // If RunSubentriesOnSameLine is true, then the INDEX table will create a one-line
 // entry that encompasses the heading and every subheading.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Heading 1:Subheading 1");

 Assert.assertEquals(" XE  \"Heading 1:Subheading 1\"", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Heading 1:Subheading 2");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Subheading.docx");
 
```

**Returns:**
boolean - Нужно ли размещать подзаписи в той же строке, что и основная запись.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Получает узел, представляющий разделитель поля. Может быть  null .

 **Examples:** 

Показывает, как работать с коллекцией полей.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldSeparator](../../com.aspose.words/fieldseparator/) - The node that represents the field separator.
### getSequenceName() {#getSequenceName}
```
public String getSequenceName()
```


Получает имя последовательности, номер которой включён в номер страницы.

 **Examples:** 

Показывает, как разделить документ на части, комбинируя поля INDEX и SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // In the SequenceName property, name a SEQ field sequence. Each entry of this INDEX field will now also display
 // the number that the sequence count is on at the XE field location that created this entry.
 index.setSequenceName("MySequence");

 // Set text that will around the sequence and page numbers to explain their meaning to the user.
 // An entry created with this configuration will display something like "MySequence at 1 on page 1" at its page number.
 // PageNumberSeparator and SequenceSeparator cannot be longer than 15 characters.
 index.setPageNumberSeparator("\tMySequence at ");
 index.setSequenceSeparator(" on page ");
 Assert.assertTrue(index.hasSequenceName());

 Assert.assertEquals(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field which moves the "MySequence" sequence to 1.
 // This field no different from normal document text. It will not appear on an INDEX field's table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldSeq sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", sequenceField.getFieldCode());

 // Insert an XE field which will create an entry in the INDEX field.
 // Since "MySequence" is at 1 and this XE field is on page 2, along with the custom separators we defined above,
 // this field's INDEX entry will display "Cat" on the left side, and "MySequence at 1 on page 2" on the right.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 Assert.assertEquals(" XE  Cat", indexEntry.getFieldCode());

 // Insert a page break, and use SEQ fields to advance "MySequence" to 3.
 builder.insertBreak(BreakType.PAGE_BREAK);
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 // Insert an XE field with the same Text property as the one above.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 // Since we are on page 2 with "MySequence" at 3, ", 3 on page 3" will be appended to the same INDEX entry as above.
 // The page number portion of that INDEX entry will now display "MySequence at 1 on page 2, 3 on page 3".
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 // Insert an XE field with a new and unique Text property value.
 // This will add a new entry, with MySequence at 3 on page 4.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Dog");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Sequence.docx");
 
```

**Returns:**
java.lang.String - Имя последовательности, номер которой включён в номер страницы.
### getSequenceSeparator() {#getSequenceSeparator}
```
public String getSequenceSeparator()
```


Получает последовательность символов, используемую для разделения номеров последовательностей и номеров страниц.

 **Examples:** 

Показывает, как разделить документ на части, комбинируя поля INDEX и SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // In the SequenceName property, name a SEQ field sequence. Each entry of this INDEX field will now also display
 // the number that the sequence count is on at the XE field location that created this entry.
 index.setSequenceName("MySequence");

 // Set text that will around the sequence and page numbers to explain their meaning to the user.
 // An entry created with this configuration will display something like "MySequence at 1 on page 1" at its page number.
 // PageNumberSeparator and SequenceSeparator cannot be longer than 15 characters.
 index.setPageNumberSeparator("\tMySequence at ");
 index.setSequenceSeparator(" on page ");
 Assert.assertTrue(index.hasSequenceName());

 Assert.assertEquals(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field which moves the "MySequence" sequence to 1.
 // This field no different from normal document text. It will not appear on an INDEX field's table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldSeq sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", sequenceField.getFieldCode());

 // Insert an XE field which will create an entry in the INDEX field.
 // Since "MySequence" is at 1 and this XE field is on page 2, along with the custom separators we defined above,
 // this field's INDEX entry will display "Cat" on the left side, and "MySequence at 1 on page 2" on the right.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 Assert.assertEquals(" XE  Cat", indexEntry.getFieldCode());

 // Insert a page break, and use SEQ fields to advance "MySequence" to 3.
 builder.insertBreak(BreakType.PAGE_BREAK);
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 // Insert an XE field with the same Text property as the one above.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 // Since we are on page 2 with "MySequence" at 3, ", 3 on page 3" will be appended to the same INDEX entry as above.
 // The page number portion of that INDEX entry will now display "MySequence at 1 on page 2, 3 on page 3".
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 // Insert an XE field with a new and unique Text property value.
 // This will add a new entry, with MySequence at 3 on page 4.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Dog");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Sequence.docx");
 
```

**Returns:**
java.lang.String - Последовательность символов, используемая для разделения номеров последовательностей и номеров страниц.
### getStart() {#getStart}
```
public FieldStart getStart()
```


Получает узел, представляющий начало поля.

 **Examples:** 

Показывает, как работать с коллекцией полей.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldStart](../../com.aspose.words/fieldstart/) - The node that represents the start of the field.
### getSwitchType(String switchName) {#getSwitchType-java.lang.String}
```
public int getSwitchType(String switchName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getType() {#getType}
```
public int getType()
```


Получает тип поля Microsoft Word.

 **Examples:** 

Показывает, как вставить поле в документ, используя код поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
int - Тип поля Microsoft Word. Возвращаемое значение является одной из констант [FieldType](../../com.aspose.words/fieldtype/).
### getUseYomi() {#getUseYomi}
```
public boolean getUseYomi()
```


Получает, следует ли включить использование йоми‑текста для записей указателя.

 **Examples:** 

Показывает, как сортировать записи поля INDEX фонетически.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // The INDEX table automatically sorts its entries by the values of their Text properties in alphabetic order.
 // Set the INDEX table to sort entries phonetically using Hiragana instead.
 index.setUseYomi(sortEntriesUsingYomi);

 if (sortEntriesUsingYomi)
     Assert.assertEquals(" INDEX  \\y", index.getFieldCode());
 else
     Assert.assertEquals(" INDEX ", index.getFieldCode());

 // Insert 4 XE fields, which would show up as entries in the INDEX field's table of contents.
 // The "Text" property may contain a word's spelling in Kanji, whose pronunciation may be ambiguous,
 // while the "Yomi" version of the word will spell exactly how it is pronounced using Hiragana.
 // If we set our INDEX field to use Yomi, it will sort these entries
 // by the value of their Yomi properties, instead of their Text values.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u611b\u5b50");
 indexEntry.setYomi("\u3042");

 Assert.assertEquals(" XE  \u611b\u5b50 \\y \u3042", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u660e\u7f8e");
 indexEntry.setYomi("\u3042");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u6075\u7f8e");
 indexEntry.setYomi("\u3048");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u611b\u7f8e");
 indexEntry.setYomi("\u3048");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Yomi.docx");
 
```

**Returns:**
boolean - Нужно ли включить использование йоми‑текста для записей указателя.
### hasPageNumberSeparator() {#hasPageNumberSeparator}
```
public boolean hasPageNumberSeparator()
```


Получает значение, указывающее, переопределён ли разделитель номера страницы через код поля.

 **Examples:** 

Показывает, как изменить разделитель номеров страниц в поле INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // If our INDEX field has an entry for a group of XE fields,
 // this entry will display the number of each page that contains an XE field that belongs to this group.
 // We can set custom separators to customize the appearance of these page numbers.
 index.setPageNumberSeparator(", on page(s) ");
 index.setPageNumberListSeparator(" & ");

 Assert.assertEquals(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.getFieldCode());
 Assert.assertTrue(index.hasPageNumberSeparator());

 // After we insert these XE fields, the INDEX field will display "First entry, on page(s) 2 & 3 & 4".
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 Assert.assertEquals(" XE  \"First entry\"", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.PageNumberList.docx");
 
```

**Returns:**
boolean - Значение, указывающее, переопределён ли разделитель номеров страниц через код поля.
### hasSequenceName() {#hasSequenceName}
```
public boolean hasSequenceName()
```


Получает значение, указывающее, следует ли использовать последовательность при построении результата поля.

 **Examples:** 

Показывает, как разделить документ на части, комбинируя поля INDEX и SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // In the SequenceName property, name a SEQ field sequence. Each entry of this INDEX field will now also display
 // the number that the sequence count is on at the XE field location that created this entry.
 index.setSequenceName("MySequence");

 // Set text that will around the sequence and page numbers to explain their meaning to the user.
 // An entry created with this configuration will display something like "MySequence at 1 on page 1" at its page number.
 // PageNumberSeparator and SequenceSeparator cannot be longer than 15 characters.
 index.setPageNumberSeparator("\tMySequence at ");
 index.setSequenceSeparator(" on page ");
 Assert.assertTrue(index.hasSequenceName());

 Assert.assertEquals(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field which moves the "MySequence" sequence to 1.
 // This field no different from normal document text. It will not appear on an INDEX field's table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldSeq sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", sequenceField.getFieldCode());

 // Insert an XE field which will create an entry in the INDEX field.
 // Since "MySequence" is at 1 and this XE field is on page 2, along with the custom separators we defined above,
 // this field's INDEX entry will display "Cat" on the left side, and "MySequence at 1 on page 2" on the right.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 Assert.assertEquals(" XE  Cat", indexEntry.getFieldCode());

 // Insert a page break, and use SEQ fields to advance "MySequence" to 3.
 builder.insertBreak(BreakType.PAGE_BREAK);
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 // Insert an XE field with the same Text property as the one above.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 // Since we are on page 2 with "MySequence" at 3, ", 3 on page 3" will be appended to the same INDEX entry as above.
 // The page number portion of that INDEX entry will now display "MySequence at 1 on page 2, 3 on page 3".
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 // Insert an XE field with a new and unique Text property value.
 // This will add a new entry, with MySequence at 3 on page 4.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Dog");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Sequence.docx");
 
```

**Returns:**
boolean - Значение, указывающее, следует ли использовать последовательность при построении результата поля.
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Определяет, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ.

 **Examples:** 

Показывает, как использовать специальное свойство для обновления результата поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Returns:**
boolean - Является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Устанавливает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ.

 **Examples:** 

Показывает, как использовать специальное свойство для обновления результата поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |

### isLocked() {#isLocked}
```
public boolean isLocked()
```


Определяет, заблокировано ли поле (не должно пересчитывать свой результат).

 **Examples:** 

Показывает, как работать с узлом FieldStart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Returns:**
boolean - Является ли поле заблокированным (не должно пересчитывать свой результат).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Устанавливает, заблокировано ли поле (не должно пересчитывать свой результат).

 **Examples:** 

Показывает, как работать с узлом FieldStart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Является ли поле заблокированным (не должно пересчитывать свой результат). |

### remove() {#remove}
```
public Node remove()
```


Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает  null .

 **Examples:** 

Показывает, как удалять поля из коллекции полей.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
 builder.insertField(" TIME ");
 builder.insertField(" REVNUM ");
 builder.insertField(" AUTHOR  \"John Doe\" ");
 builder.insertField(" SUBJECT \"My Subject\" ");
 builder.insertField(" QUOTE \"Hello world!\" ");
 doc.updateFields();

 FieldCollection fields = doc.getRange().getFields();

 Assert.assertEquals(6, fields.getCount());

 // Below are four ways of removing fields from a field collection.
 // 1 -  Get a field to remove itself:
 fields.get(0).remove();
 Assert.assertEquals(5, fields.getCount());

 // 2 -  Get the collection to remove a field that we pass to its removal method:
 Field lastField = fields.get(3);
 fields.remove(lastField);
 Assert.assertEquals(4, fields.getCount());

 // 3 -  Remove a field from a collection at an index:
 fields.removeAt(2);
 Assert.assertEquals(3, fields.getCount());

 // 4 -  Remove all the fields from the collection at once:
 fields.clear();
 Assert.assertEquals(0, fields.getCount());
 
```

Показывает, как обрабатывать поля PRIVATE.

```

 public void fieldPrivate() throws Exception {
     // Open a Corel WordPerfect document which we have converted to .docx format.
     Document doc = new Document(getMyDir() + "Field sample - PRIVATE.docx");

     // WordPerfect 5.x/6.x documents like the one we have loaded may contain PRIVATE fields.
     // Microsoft Word preserves PRIVATE fields during load/save operations,
     // but provides no functionality for them.
     FieldPrivate field = (FieldPrivate) doc.getRange().getFields().get(0);

     Assert.assertEquals(" PRIVATE \"My value\" ", field.getFieldCode());
     Assert.assertEquals(FieldType.FIELD_PRIVATE, field.getType());

     // We can also insert PRIVATE fields using a document builder.
     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.insertField(FieldType.FIELD_PRIVATE, true);

     // These fields are not a viable way of protecting sensitive information.
     // Unless backward compatibility with older versions of WordPerfect is essential,
     // we can safely remove these fields. We can do this using a DocumentVisiitor implementation.
     Assert.assertEquals(2, doc.getRange().getFields().getCount());

     FieldPrivateRemover remover = new FieldPrivateRemover();
     doc.accept(remover);

     Assert.assertEquals(remover.getFieldsRemovedCount(), 2);
     Assert.assertEquals(doc.getRange().getFields().getCount(), 0);
 }

 /// 
 /// Removes all encountered PRIVATE fields.
 /// 
 public static class FieldPrivateRemover extends DocumentVisitor {
     public FieldPrivateRemover() {
         mFieldsRemovedCount = 0;
     }

     public int getFieldsRemovedCount() {
         return mFieldsRemovedCount;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// If the node belongs to a PRIVATE field, the entire field is removed.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) throws Exception {
         if (fieldEnd.getFieldType() == FieldType.FIELD_PRIVATE) {
             fieldEnd.getField().remove();
             mFieldsRemovedCount++;
         }

         return VisitorAction.CONTINUE;
     }

     private int mFieldsRemovedCount;
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/)
### setBookmarkName(String value) {#setBookmarkName-java.lang.String}
```
public void setBookmarkName(String value)
```


Устанавливает имя закладки, отмечающей часть документа, используемую для построения указателя.

 **Examples:** 

Показывает, как создать поле INDEX, а затем использовать поля XE для заполнения его записями.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side
 // and the page containing the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // Configure the INDEX field only to display XE fields that are within the bounds
 // of a bookmark named "MainBookmark", and whose "EntryType" properties have a value of "A".
 // For both INDEX and XE fields, the "EntryType" property only uses the first character of its string value.
 index.setBookmarkName("MainBookmark");
 index.setEntryType("A");

 Assert.assertEquals(" INDEX  \\b MainBookmark \\f A", index.getFieldCode());

 // On a new page, start the bookmark with a name that matches the value
 // of the INDEX field's "BookmarkName" property.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("MainBookmark");

 // The INDEX field will pick up this entry because it is inside the bookmark,
 // and its entry type also matches the INDEX field's entry type.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 1");
 indexEntry.setEntryType("A");

 Assert.assertEquals(" XE  \"Index entry 1\" \\f A", indexEntry.getFieldCode());

 // Insert an XE field that will not appear in the INDEX because the entry types do not match.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 2");
 indexEntry.setEntryType("B");

 // End the bookmark and insert an XE field afterwards.
 // It is of the same type as the INDEX field, but will not appear
 // since it is outside the bookmark's boundaries.
 builder.endBookmark("MainBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 3");
 indexEntry.setEntryType("A");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Filtering.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя закладки, отмечающей часть документа, используемую для построения указателя. |

### setCrossReferenceSeparator(String value) {#setCrossReferenceSeparator-java.lang.String}
```
public void setCrossReferenceSeparator(String value)
```


Устанавливает последовательность символов, используемую для разделения перекрёстных ссылок и других записей.

 **Examples:** 

Показывает, как определить перекрестные ссылки в поле INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // We can configure an XE field to get its INDEX entry to display a string instead of a page number.
 // First, for entries that substitute a page number with a string,
 // specify a custom separator between the XE field's Text property value and the string.
 index.setCrossReferenceSeparator(", see: ");

 Assert.assertEquals(" INDEX  \\k \", see: \"", index.getFieldCode());

 // Insert an XE field, which creates a regular INDEX entry which displays this field's page number,
 // and does not invoke the CrossReferenceSeparator value.
 // The entry for this XE field will display "Apple, 2".
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");

 Assert.assertEquals(" XE  Apple", indexEntry.getFieldCode());

 // Insert another XE field on page 3 and set a value for the PageNumberReplacement property.
 // This value will show up instead of the number of the page that this field is on,
 // and the INDEX field's CrossReferenceSeparator value will appear in front of it.
 // The entry for this XE field will display "Banana, see: Tropical fruit".
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");
 indexEntry.setPageNumberReplacement("Tropical fruit");

 Assert.assertEquals(" XE  Banana \\t \"Tropical fruit\"", indexEntry.getFieldCode());

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.CrossReferenceSeparator.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Последовательность символов, используемая для разделения перекрёстных ссылок и других записей. |

### setEntryType(String value) {#setEntryType-java.lang.String}
```
public void setEntryType(String value)
```


Устанавливает тип записи указателя, используемый для построения указателя.

 **Examples:** 

Показывает, как создать поле INDEX, а затем использовать поля XE для заполнения его записями.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side
 // and the page containing the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // Configure the INDEX field only to display XE fields that are within the bounds
 // of a bookmark named "MainBookmark", and whose "EntryType" properties have a value of "A".
 // For both INDEX and XE fields, the "EntryType" property only uses the first character of its string value.
 index.setBookmarkName("MainBookmark");
 index.setEntryType("A");

 Assert.assertEquals(" INDEX  \\b MainBookmark \\f A", index.getFieldCode());

 // On a new page, start the bookmark with a name that matches the value
 // of the INDEX field's "BookmarkName" property.
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("MainBookmark");

 // The INDEX field will pick up this entry because it is inside the bookmark,
 // and its entry type also matches the INDEX field's entry type.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 1");
 indexEntry.setEntryType("A");

 Assert.assertEquals(" XE  \"Index entry 1\" \\f A", indexEntry.getFieldCode());

 // Insert an XE field that will not appear in the INDEX because the entry types do not match.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 2");
 indexEntry.setEntryType("B");

 // End the bookmark and insert an XE field afterwards.
 // It is of the same type as the INDEX field, but will not appear
 // since it is outside the bookmark's boundaries.
 builder.endBookmark("MainBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Index entry 3");
 indexEntry.setEntryType("A");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Filtering.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Тип записи указателя, используемый для построения указателя. |

### setHeading(String value) {#setHeading-java.lang.String}
```
public void setHeading(String value)
```


Устанавливает заголовок, который появляется в начале каждого набора записей для любой заданной буквы.

 **Examples:** 

Показывает, как заполнить поле INDEX записями с помощью полей XE, а также изменить его внешний вид.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Заголовок, который появляется в начале каждого набора записей для конкретной буквы. |

### setLanguageId(String value) {#setLanguageId-java.lang.String}
```
public void setLanguageId(String value)
```


Устанавливает идентификатор языка, используемый для создания указателя.

 **Examples:** 

Показывает, как заполнить поле INDEX записями с помощью полей XE, а также изменить его внешний вид.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Идентификатор языка, используемый для генерации указателя. |

### setLetterRange(String value) {#setLetterRange-java.lang.String}
```
public void setLetterRange(String value)
```


Устанавливает диапазон букв, которым ограничивается указатель.

 **Examples:** 

Показывает, как заполнить поле INDEX записями с помощью полей XE, а также изменить его внешний вид.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Диапазон букв, к которому ограничивается указатель. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Устанавливает LCID поля.

 **Examples:** 

Показывает, как вставить поле и работать с его локалью.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a DATE field, and then print the date it will display.
 // Your thread's current culture determines the formatting of the date.
 Field field = builder.insertField("DATE");
 System.out.println(MessageFormat.format("Today''s date, as displayed in the \"{0}\" culture: {1}", Locale.getDefault().getDisplayLanguage(), field.getResult()));

 Assert.assertEquals(1033, field.getLocaleId());
 // Changing the culture of our thread will impact the result of the DATE field.
 // Another way to get the DATE field to display a date in a different culture is to use its LocaleId property.
 // This way allows us to avoid changing the thread's culture to get this effect.
 doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);
 CultureInfo de = new CultureInfo("de-DE");
 field.setLocaleId(1031);
 field.update();

 System.out.println(MessageFormat.format("Today''s date, as displayed according to the \"{0}\" culture: {1}", Locale.forLanguageTag(LocaleUtil.getLocaleFromLCID(field.getLocaleId())).getDisplayLanguage(), field.getResult()));
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | LCID поля. |

### setNumberOfColumns(String value) {#setNumberOfColumns-java.lang.String}
```
public void setNumberOfColumns(String value)
```


Устанавливает количество столбцов на странице, используемых при построении указателя.

 **Examples:** 

Показывает, как заполнить поле INDEX записями с помощью полей XE, а также изменить его внешний вид.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setLanguageId("1033");

 // Setting this property's value to "A" will group all the entries by their first letter,
 // and place that letter in uppercase above each group.
 index.setHeading("A");

 // Set the table created by the INDEX field to span over 2 columns.
 index.setNumberOfColumns("2");

 // Set any entries with starting letters outside the "a-c" character range to be omitted.
 index.setLetterRange("a-c");

 Assert.assertEquals(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.getFieldCode());

 // These next two XE fields will show up under the "A" heading,
 // with their respective text stylings also applied to their page numbers.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apple");
 indexEntry.isItalic(true);

 Assert.assertEquals(" XE  Apple \\i", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Apricot");
 indexEntry.isBold(true);

 Assert.assertEquals(" XE  Apricot \\b", indexEntry.getFieldCode());

 // Both the next two XE fields will be under a "B" and "C" heading in the INDEX fields table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Banana");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cherry");

 // INDEX fields sort all entries alphabetically, so this entry will show up under "A" with the other two.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Avocado");

 // This entry will not appear because it starts with the letter "D",
 // which is outside the "a-c" character range that the INDEX field's LetterRange property defines.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Durian");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Formatting.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Количество колонок на страницу, используемых при построении указателя. |

### setPageNumberListSeparator(String value) {#setPageNumberListSeparator-java.lang.String}
```
public void setPageNumberListSeparator(String value)
```


Устанавливает последовательность символов, используемую для разделения двух номеров страниц в списке номеров страниц.

 **Examples:** 

Показывает, как изменить разделитель номеров страниц в поле INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // If our INDEX field has an entry for a group of XE fields,
 // this entry will display the number of each page that contains an XE field that belongs to this group.
 // We can set custom separators to customize the appearance of these page numbers.
 index.setPageNumberSeparator(", on page(s) ");
 index.setPageNumberListSeparator(" & ");

 Assert.assertEquals(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.getFieldCode());
 Assert.assertTrue(index.hasPageNumberSeparator());

 // After we insert these XE fields, the INDEX field will display "First entry, on page(s) 2 & 3 & 4".
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 Assert.assertEquals(" XE  \"First entry\"", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.PageNumberList.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Последовательность символов, используемая для разделения двух номеров страниц в списке номеров страниц. |

### setPageNumberSeparator(String value) {#setPageNumberSeparator-java.lang.String}
```
public void setPageNumberSeparator(String value)
```


Устанавливает последовательность символов, используемую для разделения записи указателя и её номера страницы.

 **Examples:** 

Показывает, как изменить разделитель номеров страниц в поле INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // If our INDEX field has an entry for a group of XE fields,
 // this entry will display the number of each page that contains an XE field that belongs to this group.
 // We can set custom separators to customize the appearance of these page numbers.
 index.setPageNumberSeparator(", on page(s) ");
 index.setPageNumberListSeparator(" & ");

 Assert.assertEquals(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.getFieldCode());
 Assert.assertTrue(index.hasPageNumberSeparator());

 // After we insert these XE fields, the INDEX field will display "First entry, on page(s) 2 & 3 & 4".
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 Assert.assertEquals(" XE  \"First entry\"", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("First entry");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.PageNumberList.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Последовательность символов, используемая для разделения записи указателя и её номера страницы. |

### setPageRangeSeparator(String value) {#setPageRangeSeparator-java.lang.String}
```
public void setPageRangeSeparator(String value)
```


Устанавливает последовательность символов, используемую для разделения начала и конца диапазона страниц.

 **Examples:** 

Показывает, как указать охваченные закладкой страницы в виде диапазона страниц для записи поля INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // For INDEX entries that display page ranges, we can specify a separator string
 // which will appear between the number of the first page, and the number of the last.
 index.setPageNumberSeparator(", on page(s) ");
 index.setPageRangeSeparator(" to ");

 Assert.assertEquals(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("My entry");

 // If an XE field names a bookmark using the PageRangeBookmarkName property,
 // its INDEX entry will show the range of pages that the bookmark spans
 // instead of the number of the page that contains the XE field.
 indexEntry.setPageRangeBookmarkName("MyBookmark");

 Assert.assertEquals(" XE  \"My entry\" \\r MyBookmark", indexEntry.getFieldCode());
 Assert.assertEquals(indexEntry.getPageRangeBookmarkName(), "MyBookmark");

 // Insert a bookmark that starts on page 3 and ends on page 5.
 // The INDEX entry for the XE field that references this bookmark will display this page range.
 // In our table, the INDEX entry will display "My entry, on page(s) 3 to 5".
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.startBookmark("MyBookmark");
 builder.write("Start of MyBookmark");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("End of MyBookmark");
 builder.endBookmark("MyBookmark");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.PageRangeBookmark.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Последовательность символов, используемая для разделения начала и конца диапазона страниц. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Устанавливает текст, находящийся между разделителем поля и его концом.

 **Examples:** 

Показывает, как вставить поле в документ, используя код поля.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Текст, который находится между разделителем поля и его концом. |

### setRunSubentriesOnSameLine(boolean value) {#setRunSubentriesOnSameLine-boolean}
```
public void setRunSubentriesOnSameLine(boolean value)
```


Устанавливает, следует ли размещать подпункты в той же строке, что и основной пункт.

 **Examples:** 

Показывает, как работать с подзаписями в поле INDEX.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);
 index.setPageNumberSeparator(", see page ");
 index.setHeading("A");

 // XE fields that have a Text property whose value becomes the heading of the INDEX entry.
 // If this value contains two string segments split by a colon (the INDEX entry will treat :) delimiter,
 // the first segment is heading, and the second segment will become the subheading.
 // The INDEX field first groups entries alphabetically, then, if there are multiple XE fields with the same
 // headings, the INDEX field will further subgroup them by the values of these headings.
 // There can be multiple subgrouping layers, depending on how many times
 // the Text properties of XE fields get segmented like this.
 // By default, an INDEX field entry group will create a new line for every subheading within this group.
 // We can set the RunSubentriesOnSameLine flag to true to keep the heading,
 // and every subheading for the group on one line instead, which will make the INDEX field more compact.
 index.setRunSubentriesOnSameLine(runSubentriesOnTheSameLine);

 if (runSubentriesOnTheSameLine)
     Assert.assertEquals(" INDEX  \\e \", see page \" \\h A \\r", index.getFieldCode());
 else
     Assert.assertEquals(" INDEX  \\e \", see page \" \\h A", index.getFieldCode());

 // Insert two XE fields, each on a new page, and with the same heading named "Heading 1",
 // which the INDEX field will use to group them.
 // If RunSubentriesOnSameLine is false, then the INDEX table will create three lines:
 // one line for the grouping heading "Heading 1", and one more line for each subheading.
 // If RunSubentriesOnSameLine is true, then the INDEX table will create a one-line
 // entry that encompasses the heading and every subheading.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Heading 1:Subheading 1");

 Assert.assertEquals(" XE  \"Heading 1:Subheading 1\"", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Heading 1:Subheading 2");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Subheading.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Нужно ли размещать подзаписи в той же строке, что и основная запись. |

### setSequenceName(String value) {#setSequenceName-java.lang.String}
```
public void setSequenceName(String value)
```


Устанавливает имя последовательности, номер которой включён в номер страницы.

 **Examples:** 

Показывает, как разделить документ на части, комбинируя поля INDEX и SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // In the SequenceName property, name a SEQ field sequence. Each entry of this INDEX field will now also display
 // the number that the sequence count is on at the XE field location that created this entry.
 index.setSequenceName("MySequence");

 // Set text that will around the sequence and page numbers to explain their meaning to the user.
 // An entry created with this configuration will display something like "MySequence at 1 on page 1" at its page number.
 // PageNumberSeparator and SequenceSeparator cannot be longer than 15 characters.
 index.setPageNumberSeparator("\tMySequence at ");
 index.setSequenceSeparator(" on page ");
 Assert.assertTrue(index.hasSequenceName());

 Assert.assertEquals(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field which moves the "MySequence" sequence to 1.
 // This field no different from normal document text. It will not appear on an INDEX field's table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldSeq sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", sequenceField.getFieldCode());

 // Insert an XE field which will create an entry in the INDEX field.
 // Since "MySequence" is at 1 and this XE field is on page 2, along with the custom separators we defined above,
 // this field's INDEX entry will display "Cat" on the left side, and "MySequence at 1 on page 2" on the right.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 Assert.assertEquals(" XE  Cat", indexEntry.getFieldCode());

 // Insert a page break, and use SEQ fields to advance "MySequence" to 3.
 builder.insertBreak(BreakType.PAGE_BREAK);
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 // Insert an XE field with the same Text property as the one above.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 // Since we are on page 2 with "MySequence" at 3, ", 3 on page 3" will be appended to the same INDEX entry as above.
 // The page number portion of that INDEX entry will now display "MySequence at 1 on page 2, 3 on page 3".
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 // Insert an XE field with a new and unique Text property value.
 // This will add a new entry, with MySequence at 3 on page 4.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Dog");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Sequence.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя последовательности, номер которой включён в номер страницы. |

### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String}
```
public void setSequenceSeparator(String value)
```


Устанавливает последовательность символов, используемую для разделения номеров последовательностей и номеров страниц.

 **Examples:** 

Показывает, как разделить документ на части, комбинируя поля INDEX и SEQ.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // If the XE fields have the same value in their "Text" property,
 // the INDEX field will group them into one entry.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // In the SequenceName property, name a SEQ field sequence. Each entry of this INDEX field will now also display
 // the number that the sequence count is on at the XE field location that created this entry.
 index.setSequenceName("MySequence");

 // Set text that will around the sequence and page numbers to explain their meaning to the user.
 // An entry created with this configuration will display something like "MySequence at 1 on page 1" at its page number.
 // PageNumberSeparator and SequenceSeparator cannot be longer than 15 characters.
 index.setPageNumberSeparator("\tMySequence at ");
 index.setSequenceSeparator(" on page ");
 Assert.assertTrue(index.hasSequenceName());

 Assert.assertEquals(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.getFieldCode());

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Insert a SEQ field which moves the "MySequence" sequence to 1.
 // This field no different from normal document text. It will not appear on an INDEX field's table of contents.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldSeq sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", sequenceField.getFieldCode());

 // Insert an XE field which will create an entry in the INDEX field.
 // Since "MySequence" is at 1 and this XE field is on page 2, along with the custom separators we defined above,
 // this field's INDEX entry will display "Cat" on the left side, and "MySequence at 1 on page 2" on the right.
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 Assert.assertEquals(" XE  Cat", indexEntry.getFieldCode());

 // Insert a page break, and use SEQ fields to advance "MySequence" to 3.
 builder.insertBreak(BreakType.PAGE_BREAK);
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");
 sequenceField = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 sequenceField.setSequenceIdentifier("MySequence");

 // Insert an XE field with the same Text property as the one above.
 // The INDEX entry will group XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 // Since we are on page 2 with "MySequence" at 3, ", 3 on page 3" will be appended to the same INDEX entry as above.
 // The page number portion of that INDEX entry will now display "MySequence at 1 on page 2, 3 on page 3".
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Cat");

 // Insert an XE field with a new and unique Text property value.
 // This will add a new entry, with MySequence at 3 on page 4.
 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("Dog");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Sequence.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Последовательность символов, используемая для разделения номеров последовательностей и номеров страниц. |

### setUseYomi(boolean value) {#setUseYomi-boolean}
```
public void setUseYomi(boolean value)
```


Устанавливает, следует ли включить использование йоми‑текста для записей указателя.

 **Examples:** 

Показывает, как сортировать записи поля INDEX фонетически.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an INDEX field which will display an entry for each XE field found in the document.
 // Each entry will display the XE field's Text property value on the left side,
 // and the number of the page that contains the XE field on the right.
 // The INDEX entry will collect all XE fields with matching values in the "Text" property
 // into one entry as opposed to making an entry for each XE field.
 FieldIndex index = (FieldIndex) builder.insertField(FieldType.FIELD_INDEX, true);

 // The INDEX table automatically sorts its entries by the values of their Text properties in alphabetic order.
 // Set the INDEX table to sort entries phonetically using Hiragana instead.
 index.setUseYomi(sortEntriesUsingYomi);

 if (sortEntriesUsingYomi)
     Assert.assertEquals(" INDEX  \\y", index.getFieldCode());
 else
     Assert.assertEquals(" INDEX ", index.getFieldCode());

 // Insert 4 XE fields, which would show up as entries in the INDEX field's table of contents.
 // The "Text" property may contain a word's spelling in Kanji, whose pronunciation may be ambiguous,
 // while the "Yomi" version of the word will spell exactly how it is pronounced using Hiragana.
 // If we set our INDEX field to use Yomi, it will sort these entries
 // by the value of their Yomi properties, instead of their Text values.
 builder.insertBreak(BreakType.PAGE_BREAK);
 FieldXE indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u611b\u5b50");
 indexEntry.setYomi("\u3042");

 Assert.assertEquals(" XE  \u611b\u5b50 \\y \u3042", indexEntry.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u660e\u7f8e");
 indexEntry.setYomi("\u3042");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u6075\u7f8e");
 indexEntry.setYomi("\u3048");

 builder.insertBreak(BreakType.PAGE_BREAK);
 indexEntry = (FieldXE) builder.insertField(FieldType.FIELD_INDEX_ENTRY, true);
 indexEntry.setText("\u611b\u7f8e");
 indexEntry.setYomi("\u3048");

 doc.updatePageLayout();
 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.INDEX.XE.Yomi.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Нужно ли включить использование йоми‑текста для записей указателя. |

### unlink() {#unlink}
```
public boolean unlink()
```


Выполняет разъединение поля.

 **Remarks:** 

Заменяет поле его самым последним результатом.

Некоторые поля, такие как поля XE (Index Entry) и SEQ (Sequence), нельзя разъединять.

 **Examples:** 

Показывает, как разъединить поле.

```

 Document doc = new Document(getMyDir() + "Linked fields.docx");
 doc.getRange().getFields().get(1).unlink();
 
```

**Returns:**
boolean -  true  если поле было разъединено, иначе  false .
### update() {#update}
```
public void update()
```


Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется.

 **Examples:** 

Показывает, как вставить поле в документ, используя FieldType.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert two fields while passing a flag which determines whether to update them as the builder inserts them.
 // In some cases, updating fields could be computationally expensive, and it may be a good idea to defer the update.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 builder.write("This document was written by ");
 builder.insertField(FieldType.FIELD_AUTHOR, updateInsertedFieldsImmediately);

 builder.insertParagraph();
 builder.write("\nThis is page ");
 builder.insertField(FieldType.FIELD_PAGE, updateInsertedFieldsImmediately);

 Assert.assertEquals(" AUTHOR ", doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(" PAGE ", doc.getRange().getFields().get(1).getFieldCode());

 if (updateInsertedFieldsImmediately) {
     Assert.assertEquals("John Doe", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals("1", doc.getRange().getFields().get(1).getResult());
 } else {
     Assert.assertEquals("", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals("", doc.getRange().getFields().get(1).getResult());

     // We will need to update these fields using the update methods manually.
     doc.getRange().getFields().get(0).update();

     Assert.assertEquals("John Doe", doc.getRange().getFields().get(0).getResult());

     doc.updateFields();

     Assert.assertEquals("1", doc.getRange().getFields().get(1).getResult());
 }
 
```

Показывает, как форматировать результаты полей.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a document builder to insert a field that displays a result with no format applied.
 Field field = builder.insertField("= 2 + 3");

 Assert.assertEquals("= 2 + 3", field.getFieldCode());
 Assert.assertEquals("5", field.getResult());

 // We can apply a format to a field's result using the field's properties.
 // Below are three types of formats that we can apply to a field's result.
 // 1 -  Numeric format:
 FieldFormat format = field.getFormat();
 format.setNumericFormat("$###.00");
 field.update();

 Assert.assertEquals("= 2 + 3 \\# $###.00", field.getFieldCode());
 Assert.assertEquals("$  5.00", field.getResult());

 // 2 -  Date/time format:
 field = builder.insertField("DATE");
 format = field.getFormat();
 format.setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 Assert.assertEquals("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());
 System.out.println("Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

 // 3 -  General format:
 field = builder.insertField("= 25 + 33");
 format = field.getFormat();
 format.getGeneralFormats().add(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().add(GeneralFormat.UPPER);
 field.update();

 int index = 0;
 Iterator generalFormatEnumerator = format.getGeneralFormats().iterator();
 while (generalFormatEnumerator.hasNext()) {
     int value = generalFormatEnumerator.next();
     System.out.println(MessageFormat.format("General format index {0}: {1}", index++, value));
 }

 Assert.assertEquals("= 25 + 33 \\* roman \\* Upper", field.getFieldCode());
 Assert.assertEquals("LVIII", field.getResult());
 Assert.assertEquals(2, format.getGeneralFormats().getCount());
 Assert.assertEquals(GeneralFormat.LOWERCASE_ROMAN, format.getGeneralFormats().get(0));

 // We can remove our formats to revert the field's result to its original form.
 format.getGeneralFormats().remove(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().removeAt(0);
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 field.update();

 Assert.assertEquals("= 25 + 33  ", field.getFieldCode());
 Assert.assertEquals("58", field.getResult());
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 
```

### update(boolean ignoreMergeFormat) {#update-boolean}
```
public void update(boolean ignoreMergeFormat)
```


Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется.

 **Examples:** 

Показывает, как сохранять или отбрасывать поля INCLUDEPICTURE при загрузке документа.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldIncludePicture includePicture = (FieldIncludePicture) builder.insertField(FieldType.FIELD_INCLUDE_PICTURE, true);
 includePicture.setSourceFullName(getImageDir() + "Transparent background logo.png");
 includePicture.update(true);

 try (ByteArrayOutputStream docStream = new ByteArrayOutputStream()) {
     doc.save(docStream, new OoxmlSaveOptions(SaveFormat.DOCX));

     // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
     // into image shapes when loading a document that contains them.
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setPreserveIncludePictureField(preserveIncludePictureField);
     }

     doc = new Document(new ByteArrayInputStream(docStream.toByteArray()), loadOptions);
     FieldCollection fieldCollection = doc.getRange().getFields();

     if (preserveIncludePictureField) {
         Assert.assertTrue(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));

         doc.updateFields();
         doc.save(getArtifactsDir() + "Field.PreserveIncludePicture.docx");
     } else {
         Assert.assertFalse(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));
     }
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ignoreMergeFormat | boolean | Если  true  то прямое форматирование результата поля отменяется, независимо от переключателя MERGEFORMAT, иначе выполняется обычное обновление. |

