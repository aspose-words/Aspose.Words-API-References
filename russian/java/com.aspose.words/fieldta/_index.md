---
title: "FieldTA"
linktitle: "FieldTA"
second_title: "Aspose.Words для Java"
description: "Реализует поле TA в Java."
type: docs
weight: 292
url: /ru/java/com.aspose.words/fieldta/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldTA extends Field
```

Реализует поле TA.

Чтобы узнать больше, посетите статью документации [ Working with Fields ][Working with Fields].

 **Remarks:** 

Определяет текст и номер страницы для записи в таблице авторитетов, которая используется полем TOA.

 **Examples:** 

Показывает, как создавать и настраивать таблицу указателей с использованием полей TOA и TA.

```

 public void fieldTOA() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOA field, which will create an entry for each TA field in the document,
     // displaying long citations and page numbers for each entry.
     FieldToa fieldToa = (FieldToa) builder.insertField(FieldType.FIELD_TOA, false);

     // Set the entry category for our table. This TOA will now only include TA fields
     // that have a matching value in their EntryCategory property.
     fieldToa.setEntryCategory("1");

     // Moreover, the Table of Authorities category at index 1 is "Cases",
     // which will show up as our table's title if we set this variable to true.
     fieldToa.setUseHeading(true);

     // We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
     fieldToa.setBookmarkName("MyBookmark");

     // By default, a dotted line page-wide tab appears between the TA field's citation
     // and its page number. We can replace it with any text we put on this property.
     // Inserting a tab character will preserve the original tab.
     fieldToa.setEntrySeparator(" \t p.");

     // If we have multiple TA entries that share the same long citation,
     // all their respective page numbers will show up on one row.
     // We can use this property to specify a string that will separate their page numbers.
     fieldToa.setPageNumberListSeparator(" & p. ");

     // We can set this to true to get our table to display the word "passim"
     // if there are five or more page numbers in one row.
     fieldToa.setUsePassim(true);

     // One TA field can refer to a range of pages.
     // We can specify a string here to appear between the start and end page numbers for such ranges.
     fieldToa.setPageRangeSeparator(" to ");

     // The format from the TA fields will carry over into our table.
     // We can disable this by setting the RemoveEntryFormatting flag.
     fieldToa.setRemoveEntryFormatting(true);
     builder.getFont().setColor(Color.GREEN);
     builder.getFont().setName("Arial Black");

     Assert.assertEquals(fieldToa.getFieldCode(), " TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f");

     builder.insertBreak(BreakType.PAGE_BREAK);

     // This TA field will not appear as an entry in the TOA since it is outside
     // the bookmark's bounds that the TOA's BookmarkName property specifies.
     FieldTA fieldTA = insertToaEntry(builder, "1", "Source 1");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 1\"");

     // This TA field is inside the bookmark,
     // but the entry category does not match that of the table, so the TA field will not include it.
     builder.startBookmark("MyBookmark");
     fieldTA = insertToaEntry(builder, "2", "Source 2");

     // This entry will appear in the table.
     fieldTA = insertToaEntry(builder, "1", "Source 3");

     // A TOA table does not display short citations,
     // but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
     fieldTA.setShortCitation("S.3");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\s S.3");

     // We can format the page number to make it bold/italic using the following properties.
     // We will still see these effects if we set our table to ignore formatting.
     fieldTA = insertToaEntry(builder, "1", "Source 2");
     fieldTA.isBold(true);
     fieldTA.isItalic(true);

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 2\" \\b \\i");

     // We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
     // Note that this entry refers to the same source as the one above to share one row in our table.
     // This row will have the page number of the entry above and the page range of this entry,
     // with the table's page list and page number range separators between page numbers.
     fieldTA = insertToaEntry(builder, "1", "Source 3");
     fieldTA.setPageRangeBookmarkName("MyMultiPageBookmark");

     builder.startBookmark("MyMultiPageBookmark");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.endBookmark("MyMultiPageBookmark");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark");

     // If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
     for (int i = 0; i < 5; i++) {
         insertToaEntry(builder, "1", "Source 4");
     }

     builder.endBookmark("MyBookmark");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOA.TA.docx");
 }

 private static FieldTA insertToaEntry(DocumentBuilder builder, String entryCategory, String longCitation) throws Exception {
     FieldTA field = (FieldTA) builder.insertField(FieldType.FIELD_TOA_ENTRY, false);
     field.setEntryCategory(entryCategory);
     field.setLongCitation(longCitation);

     builder.insertBreak(BreakType.PAGE_BREAK);

     return field;
 }
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Методы

| Метод | Описание |
| --- | --- |
| [getDisplayResult()](#getDisplayResult) | Получает текст, представляющий отображаемый результат поля. |
| [getEnd()](#getEnd) | Получает узел, представляющий конец поля. |
| [getEntryCategory()](#getEntryCategory) | Получает целую категорию записи, которая представляет собой число, соответствующее порядку категорий. |
| [getFieldCode()](#getFieldCode) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [getFormat()](#getFormat) | Получает объект [FieldFormat](../../com.aspose.words/fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [getLocaleId()](#getLocaleId) | Получает LCID поля. |
| [getLongCitation()](#getLongCitation) | Получает полную ссылку для записи. |
| [getPageRangeBookmarkName()](#getPageRangeBookmarkName) | Получает имя закладки, отмечающей диапазон страниц, который вставляется как номер страницы записи. |
| [getResult()](#getResult) | Получает текст, находящийся между разделителем поля и концом поля. |
| [getSeparator()](#getSeparator) | Получает узел, представляющий разделитель поля. |
| [getShortCitation()](#getShortCitation) | Получает краткую ссылку для записи. |
| [getStart()](#getStart) | Получает узел, представляющий начало поля. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getType()](#getType) | Получает тип поля Microsoft Word. |
| [isBold()](#isBold) | Получает, следует ли применять полужирное форматирование к номеру страницы записи. |
| [isBold(boolean value)](#isBold-boolean) | Устанавливает, следует ли применять полужирное форматирование к номеру страницы записи. |
| [isDirty()](#isDirty) | Определяет, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [isDirty(boolean value)](#isDirty-boolean) | Устанавливает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [isItalic()](#isItalic) | Получает, следует ли применять курсивное форматирование к номеру страницы записи. |
| [isItalic(boolean value)](#isItalic-boolean) | Устанавливает, следует ли применять курсивное форматирование к номеру страницы записи. |
| [isLocked()](#isLocked) | Определяет, заблокировано ли поле (не должно пересчитывать свой результат). |
| [isLocked(boolean value)](#isLocked-boolean) | Устанавливает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [remove()](#remove) | Удаляет поле из документа. |
| [setEntryCategory(String value)](#setEntryCategory-java.lang.String) | Устанавливает целую категорию записи, которая представляет собой число, соответствующее порядку категорий. |
| [setLocaleId(int value)](#setLocaleId-int) | Устанавливает LCID поля. |
| [setLongCitation(String value)](#setLongCitation-java.lang.String) | Устанавливает полную ссылку для записи. |
| [setPageRangeBookmarkName(String value)](#setPageRangeBookmarkName-java.lang.String) | Устанавливает имя закладки, отмечающей диапазон страниц, который вставляется как номер страницы записи. |
| [setResult(String value)](#setResult-java.lang.String) | Устанавливает текст, находящийся между разделителем поля и его концом. |
| [setShortCitation(String value)](#setShortCitation-java.lang.String) | Устанавливает краткую ссылку для записи. |
| [unlink()](#unlink) | Выполняет разъединение поля. |
| [update()](#update) | Выполняет обновление поля. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Выполняет обновление поля. |
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
### getEntryCategory() {#getEntryCategory}
```
public String getEntryCategory()
```


Получает целую категорию записи, которая представляет собой число, соответствующее порядку категорий.

 **Examples:** 

Показывает, как создавать и настраивать таблицу указателей с использованием полей TOA и TA.

```

 public void fieldTOA() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOA field, which will create an entry for each TA field in the document,
     // displaying long citations and page numbers for each entry.
     FieldToa fieldToa = (FieldToa) builder.insertField(FieldType.FIELD_TOA, false);

     // Set the entry category for our table. This TOA will now only include TA fields
     // that have a matching value in their EntryCategory property.
     fieldToa.setEntryCategory("1");

     // Moreover, the Table of Authorities category at index 1 is "Cases",
     // which will show up as our table's title if we set this variable to true.
     fieldToa.setUseHeading(true);

     // We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
     fieldToa.setBookmarkName("MyBookmark");

     // By default, a dotted line page-wide tab appears between the TA field's citation
     // and its page number. We can replace it with any text we put on this property.
     // Inserting a tab character will preserve the original tab.
     fieldToa.setEntrySeparator(" \t p.");

     // If we have multiple TA entries that share the same long citation,
     // all their respective page numbers will show up on one row.
     // We can use this property to specify a string that will separate their page numbers.
     fieldToa.setPageNumberListSeparator(" & p. ");

     // We can set this to true to get our table to display the word "passim"
     // if there are five or more page numbers in one row.
     fieldToa.setUsePassim(true);

     // One TA field can refer to a range of pages.
     // We can specify a string here to appear between the start and end page numbers for such ranges.
     fieldToa.setPageRangeSeparator(" to ");

     // The format from the TA fields will carry over into our table.
     // We can disable this by setting the RemoveEntryFormatting flag.
     fieldToa.setRemoveEntryFormatting(true);
     builder.getFont().setColor(Color.GREEN);
     builder.getFont().setName("Arial Black");

     Assert.assertEquals(fieldToa.getFieldCode(), " TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f");

     builder.insertBreak(BreakType.PAGE_BREAK);

     // This TA field will not appear as an entry in the TOA since it is outside
     // the bookmark's bounds that the TOA's BookmarkName property specifies.
     FieldTA fieldTA = insertToaEntry(builder, "1", "Source 1");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 1\"");

     // This TA field is inside the bookmark,
     // but the entry category does not match that of the table, so the TA field will not include it.
     builder.startBookmark("MyBookmark");
     fieldTA = insertToaEntry(builder, "2", "Source 2");

     // This entry will appear in the table.
     fieldTA = insertToaEntry(builder, "1", "Source 3");

     // A TOA table does not display short citations,
     // but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
     fieldTA.setShortCitation("S.3");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\s S.3");

     // We can format the page number to make it bold/italic using the following properties.
     // We will still see these effects if we set our table to ignore formatting.
     fieldTA = insertToaEntry(builder, "1", "Source 2");
     fieldTA.isBold(true);
     fieldTA.isItalic(true);

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 2\" \\b \\i");

     // We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
     // Note that this entry refers to the same source as the one above to share one row in our table.
     // This row will have the page number of the entry above and the page range of this entry,
     // with the table's page list and page number range separators between page numbers.
     fieldTA = insertToaEntry(builder, "1", "Source 3");
     fieldTA.setPageRangeBookmarkName("MyMultiPageBookmark");

     builder.startBookmark("MyMultiPageBookmark");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.endBookmark("MyMultiPageBookmark");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark");

     // If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
     for (int i = 0; i < 5; i++) {
         insertToaEntry(builder, "1", "Source 4");
     }

     builder.endBookmark("MyBookmark");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOA.TA.docx");
 }

 private static FieldTA insertToaEntry(DocumentBuilder builder, String entryCategory, String longCitation) throws Exception {
     FieldTA field = (FieldTA) builder.insertField(FieldType.FIELD_TOA_ENTRY, false);
     field.setEntryCategory(entryCategory);
     field.setLongCitation(longCitation);

     builder.insertBreak(BreakType.PAGE_BREAK);

     return field;
 }
 
```

**Returns:**
java.lang.String — целая категория записи, которая представляет собой число, соответствующее порядку категорий.
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
### getLongCitation() {#getLongCitation}
```
public String getLongCitation()
```


Получает полную ссылку для записи.

 **Examples:** 

Показывает, как создавать и настраивать таблицу указателей с использованием полей TOA и TA.

```

 public void fieldTOA() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOA field, which will create an entry for each TA field in the document,
     // displaying long citations and page numbers for each entry.
     FieldToa fieldToa = (FieldToa) builder.insertField(FieldType.FIELD_TOA, false);

     // Set the entry category for our table. This TOA will now only include TA fields
     // that have a matching value in their EntryCategory property.
     fieldToa.setEntryCategory("1");

     // Moreover, the Table of Authorities category at index 1 is "Cases",
     // which will show up as our table's title if we set this variable to true.
     fieldToa.setUseHeading(true);

     // We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
     fieldToa.setBookmarkName("MyBookmark");

     // By default, a dotted line page-wide tab appears between the TA field's citation
     // and its page number. We can replace it with any text we put on this property.
     // Inserting a tab character will preserve the original tab.
     fieldToa.setEntrySeparator(" \t p.");

     // If we have multiple TA entries that share the same long citation,
     // all their respective page numbers will show up on one row.
     // We can use this property to specify a string that will separate their page numbers.
     fieldToa.setPageNumberListSeparator(" & p. ");

     // We can set this to true to get our table to display the word "passim"
     // if there are five or more page numbers in one row.
     fieldToa.setUsePassim(true);

     // One TA field can refer to a range of pages.
     // We can specify a string here to appear between the start and end page numbers for such ranges.
     fieldToa.setPageRangeSeparator(" to ");

     // The format from the TA fields will carry over into our table.
     // We can disable this by setting the RemoveEntryFormatting flag.
     fieldToa.setRemoveEntryFormatting(true);
     builder.getFont().setColor(Color.GREEN);
     builder.getFont().setName("Arial Black");

     Assert.assertEquals(fieldToa.getFieldCode(), " TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f");

     builder.insertBreak(BreakType.PAGE_BREAK);

     // This TA field will not appear as an entry in the TOA since it is outside
     // the bookmark's bounds that the TOA's BookmarkName property specifies.
     FieldTA fieldTA = insertToaEntry(builder, "1", "Source 1");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 1\"");

     // This TA field is inside the bookmark,
     // but the entry category does not match that of the table, so the TA field will not include it.
     builder.startBookmark("MyBookmark");
     fieldTA = insertToaEntry(builder, "2", "Source 2");

     // This entry will appear in the table.
     fieldTA = insertToaEntry(builder, "1", "Source 3");

     // A TOA table does not display short citations,
     // but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
     fieldTA.setShortCitation("S.3");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\s S.3");

     // We can format the page number to make it bold/italic using the following properties.
     // We will still see these effects if we set our table to ignore formatting.
     fieldTA = insertToaEntry(builder, "1", "Source 2");
     fieldTA.isBold(true);
     fieldTA.isItalic(true);

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 2\" \\b \\i");

     // We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
     // Note that this entry refers to the same source as the one above to share one row in our table.
     // This row will have the page number of the entry above and the page range of this entry,
     // with the table's page list and page number range separators between page numbers.
     fieldTA = insertToaEntry(builder, "1", "Source 3");
     fieldTA.setPageRangeBookmarkName("MyMultiPageBookmark");

     builder.startBookmark("MyMultiPageBookmark");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.endBookmark("MyMultiPageBookmark");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark");

     // If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
     for (int i = 0; i < 5; i++) {
         insertToaEntry(builder, "1", "Source 4");
     }

     builder.endBookmark("MyBookmark");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOA.TA.docx");
 }

 private static FieldTA insertToaEntry(DocumentBuilder builder, String entryCategory, String longCitation) throws Exception {
     FieldTA field = (FieldTA) builder.insertField(FieldType.FIELD_TOA_ENTRY, false);
     field.setEntryCategory(entryCategory);
     field.setLongCitation(longCitation);

     builder.insertBreak(BreakType.PAGE_BREAK);

     return field;
 }
 
```

**Returns:**
java.lang.String — полная ссылка для записи.
### getPageRangeBookmarkName() {#getPageRangeBookmarkName}
```
public String getPageRangeBookmarkName()
```


Получает имя закладки, отмечающей диапазон страниц, который вставляется как номер страницы записи.

 **Examples:** 

Показывает, как создавать и настраивать таблицу указателей с использованием полей TOA и TA.

```

 public void fieldTOA() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOA field, which will create an entry for each TA field in the document,
     // displaying long citations and page numbers for each entry.
     FieldToa fieldToa = (FieldToa) builder.insertField(FieldType.FIELD_TOA, false);

     // Set the entry category for our table. This TOA will now only include TA fields
     // that have a matching value in their EntryCategory property.
     fieldToa.setEntryCategory("1");

     // Moreover, the Table of Authorities category at index 1 is "Cases",
     // which will show up as our table's title if we set this variable to true.
     fieldToa.setUseHeading(true);

     // We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
     fieldToa.setBookmarkName("MyBookmark");

     // By default, a dotted line page-wide tab appears between the TA field's citation
     // and its page number. We can replace it with any text we put on this property.
     // Inserting a tab character will preserve the original tab.
     fieldToa.setEntrySeparator(" \t p.");

     // If we have multiple TA entries that share the same long citation,
     // all their respective page numbers will show up on one row.
     // We can use this property to specify a string that will separate their page numbers.
     fieldToa.setPageNumberListSeparator(" & p. ");

     // We can set this to true to get our table to display the word "passim"
     // if there are five or more page numbers in one row.
     fieldToa.setUsePassim(true);

     // One TA field can refer to a range of pages.
     // We can specify a string here to appear between the start and end page numbers for such ranges.
     fieldToa.setPageRangeSeparator(" to ");

     // The format from the TA fields will carry over into our table.
     // We can disable this by setting the RemoveEntryFormatting flag.
     fieldToa.setRemoveEntryFormatting(true);
     builder.getFont().setColor(Color.GREEN);
     builder.getFont().setName("Arial Black");

     Assert.assertEquals(fieldToa.getFieldCode(), " TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f");

     builder.insertBreak(BreakType.PAGE_BREAK);

     // This TA field will not appear as an entry in the TOA since it is outside
     // the bookmark's bounds that the TOA's BookmarkName property specifies.
     FieldTA fieldTA = insertToaEntry(builder, "1", "Source 1");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 1\"");

     // This TA field is inside the bookmark,
     // but the entry category does not match that of the table, so the TA field will not include it.
     builder.startBookmark("MyBookmark");
     fieldTA = insertToaEntry(builder, "2", "Source 2");

     // This entry will appear in the table.
     fieldTA = insertToaEntry(builder, "1", "Source 3");

     // A TOA table does not display short citations,
     // but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
     fieldTA.setShortCitation("S.3");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\s S.3");

     // We can format the page number to make it bold/italic using the following properties.
     // We will still see these effects if we set our table to ignore formatting.
     fieldTA = insertToaEntry(builder, "1", "Source 2");
     fieldTA.isBold(true);
     fieldTA.isItalic(true);

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 2\" \\b \\i");

     // We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
     // Note that this entry refers to the same source as the one above to share one row in our table.
     // This row will have the page number of the entry above and the page range of this entry,
     // with the table's page list and page number range separators between page numbers.
     fieldTA = insertToaEntry(builder, "1", "Source 3");
     fieldTA.setPageRangeBookmarkName("MyMultiPageBookmark");

     builder.startBookmark("MyMultiPageBookmark");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.endBookmark("MyMultiPageBookmark");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark");

     // If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
     for (int i = 0; i < 5; i++) {
         insertToaEntry(builder, "1", "Source 4");
     }

     builder.endBookmark("MyBookmark");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOA.TA.docx");
 }

 private static FieldTA insertToaEntry(DocumentBuilder builder, String entryCategory, String longCitation) throws Exception {
     FieldTA field = (FieldTA) builder.insertField(FieldType.FIELD_TOA_ENTRY, false);
     field.setEntryCategory(entryCategory);
     field.setLongCitation(longCitation);

     builder.insertBreak(BreakType.PAGE_BREAK);

     return field;
 }
 
```

**Returns:**
java.lang.String - Имя закладки, которое отмечает диапазон страниц, вставляемый как номер страницы записи.
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
### getShortCitation() {#getShortCitation}
```
public String getShortCitation()
```


Получает краткую ссылку для записи.

 **Examples:** 

Показывает, как создавать и настраивать таблицу указателей с использованием полей TOA и TA.

```

 public void fieldTOA() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOA field, which will create an entry for each TA field in the document,
     // displaying long citations and page numbers for each entry.
     FieldToa fieldToa = (FieldToa) builder.insertField(FieldType.FIELD_TOA, false);

     // Set the entry category for our table. This TOA will now only include TA fields
     // that have a matching value in their EntryCategory property.
     fieldToa.setEntryCategory("1");

     // Moreover, the Table of Authorities category at index 1 is "Cases",
     // which will show up as our table's title if we set this variable to true.
     fieldToa.setUseHeading(true);

     // We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
     fieldToa.setBookmarkName("MyBookmark");

     // By default, a dotted line page-wide tab appears between the TA field's citation
     // and its page number. We can replace it with any text we put on this property.
     // Inserting a tab character will preserve the original tab.
     fieldToa.setEntrySeparator(" \t p.");

     // If we have multiple TA entries that share the same long citation,
     // all their respective page numbers will show up on one row.
     // We can use this property to specify a string that will separate their page numbers.
     fieldToa.setPageNumberListSeparator(" & p. ");

     // We can set this to true to get our table to display the word "passim"
     // if there are five or more page numbers in one row.
     fieldToa.setUsePassim(true);

     // One TA field can refer to a range of pages.
     // We can specify a string here to appear between the start and end page numbers for such ranges.
     fieldToa.setPageRangeSeparator(" to ");

     // The format from the TA fields will carry over into our table.
     // We can disable this by setting the RemoveEntryFormatting flag.
     fieldToa.setRemoveEntryFormatting(true);
     builder.getFont().setColor(Color.GREEN);
     builder.getFont().setName("Arial Black");

     Assert.assertEquals(fieldToa.getFieldCode(), " TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f");

     builder.insertBreak(BreakType.PAGE_BREAK);

     // This TA field will not appear as an entry in the TOA since it is outside
     // the bookmark's bounds that the TOA's BookmarkName property specifies.
     FieldTA fieldTA = insertToaEntry(builder, "1", "Source 1");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 1\"");

     // This TA field is inside the bookmark,
     // but the entry category does not match that of the table, so the TA field will not include it.
     builder.startBookmark("MyBookmark");
     fieldTA = insertToaEntry(builder, "2", "Source 2");

     // This entry will appear in the table.
     fieldTA = insertToaEntry(builder, "1", "Source 3");

     // A TOA table does not display short citations,
     // but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
     fieldTA.setShortCitation("S.3");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\s S.3");

     // We can format the page number to make it bold/italic using the following properties.
     // We will still see these effects if we set our table to ignore formatting.
     fieldTA = insertToaEntry(builder, "1", "Source 2");
     fieldTA.isBold(true);
     fieldTA.isItalic(true);

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 2\" \\b \\i");

     // We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
     // Note that this entry refers to the same source as the one above to share one row in our table.
     // This row will have the page number of the entry above and the page range of this entry,
     // with the table's page list and page number range separators between page numbers.
     fieldTA = insertToaEntry(builder, "1", "Source 3");
     fieldTA.setPageRangeBookmarkName("MyMultiPageBookmark");

     builder.startBookmark("MyMultiPageBookmark");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.endBookmark("MyMultiPageBookmark");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark");

     // If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
     for (int i = 0; i < 5; i++) {
         insertToaEntry(builder, "1", "Source 4");
     }

     builder.endBookmark("MyBookmark");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOA.TA.docx");
 }

 private static FieldTA insertToaEntry(DocumentBuilder builder, String entryCategory, String longCitation) throws Exception {
     FieldTA field = (FieldTA) builder.insertField(FieldType.FIELD_TOA_ENTRY, false);
     field.setEntryCategory(entryCategory);
     field.setLongCitation(longCitation);

     builder.insertBreak(BreakType.PAGE_BREAK);

     return field;
 }
 
```

**Returns:**
java.lang.String — краткая ссылка для записи.
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
### isBold() {#isBold}
```
public boolean isBold()
```


Получает, следует ли применять полужирное форматирование к номеру страницы записи.

 **Examples:** 

Показывает, как создавать и настраивать таблицу указателей с использованием полей TOA и TA.

```

 public void fieldTOA() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOA field, which will create an entry for each TA field in the document,
     // displaying long citations and page numbers for each entry.
     FieldToa fieldToa = (FieldToa) builder.insertField(FieldType.FIELD_TOA, false);

     // Set the entry category for our table. This TOA will now only include TA fields
     // that have a matching value in their EntryCategory property.
     fieldToa.setEntryCategory("1");

     // Moreover, the Table of Authorities category at index 1 is "Cases",
     // which will show up as our table's title if we set this variable to true.
     fieldToa.setUseHeading(true);

     // We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
     fieldToa.setBookmarkName("MyBookmark");

     // By default, a dotted line page-wide tab appears between the TA field's citation
     // and its page number. We can replace it with any text we put on this property.
     // Inserting a tab character will preserve the original tab.
     fieldToa.setEntrySeparator(" \t p.");

     // If we have multiple TA entries that share the same long citation,
     // all their respective page numbers will show up on one row.
     // We can use this property to specify a string that will separate their page numbers.
     fieldToa.setPageNumberListSeparator(" & p. ");

     // We can set this to true to get our table to display the word "passim"
     // if there are five or more page numbers in one row.
     fieldToa.setUsePassim(true);

     // One TA field can refer to a range of pages.
     // We can specify a string here to appear between the start and end page numbers for such ranges.
     fieldToa.setPageRangeSeparator(" to ");

     // The format from the TA fields will carry over into our table.
     // We can disable this by setting the RemoveEntryFormatting flag.
     fieldToa.setRemoveEntryFormatting(true);
     builder.getFont().setColor(Color.GREEN);
     builder.getFont().setName("Arial Black");

     Assert.assertEquals(fieldToa.getFieldCode(), " TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f");

     builder.insertBreak(BreakType.PAGE_BREAK);

     // This TA field will not appear as an entry in the TOA since it is outside
     // the bookmark's bounds that the TOA's BookmarkName property specifies.
     FieldTA fieldTA = insertToaEntry(builder, "1", "Source 1");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 1\"");

     // This TA field is inside the bookmark,
     // but the entry category does not match that of the table, so the TA field will not include it.
     builder.startBookmark("MyBookmark");
     fieldTA = insertToaEntry(builder, "2", "Source 2");

     // This entry will appear in the table.
     fieldTA = insertToaEntry(builder, "1", "Source 3");

     // A TOA table does not display short citations,
     // but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
     fieldTA.setShortCitation("S.3");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\s S.3");

     // We can format the page number to make it bold/italic using the following properties.
     // We will still see these effects if we set our table to ignore formatting.
     fieldTA = insertToaEntry(builder, "1", "Source 2");
     fieldTA.isBold(true);
     fieldTA.isItalic(true);

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 2\" \\b \\i");

     // We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
     // Note that this entry refers to the same source as the one above to share one row in our table.
     // This row will have the page number of the entry above and the page range of this entry,
     // with the table's page list and page number range separators between page numbers.
     fieldTA = insertToaEntry(builder, "1", "Source 3");
     fieldTA.setPageRangeBookmarkName("MyMultiPageBookmark");

     builder.startBookmark("MyMultiPageBookmark");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.endBookmark("MyMultiPageBookmark");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark");

     // If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
     for (int i = 0; i < 5; i++) {
         insertToaEntry(builder, "1", "Source 4");
     }

     builder.endBookmark("MyBookmark");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOA.TA.docx");
 }

 private static FieldTA insertToaEntry(DocumentBuilder builder, String entryCategory, String longCitation) throws Exception {
     FieldTA field = (FieldTA) builder.insertField(FieldType.FIELD_TOA_ENTRY, false);
     field.setEntryCategory(entryCategory);
     field.setLongCitation(longCitation);

     builder.insertBreak(BreakType.PAGE_BREAK);

     return field;
 }
 
```

**Returns:**
boolean — следует ли применять полужирное форматирование к номеру страницы записи.
### isBold(boolean value) {#isBold-boolean}
```
public void isBold(boolean value)
```


Устанавливает, следует ли применять полужирное форматирование к номеру страницы записи.

 **Examples:** 

Показывает, как создавать и настраивать таблицу указателей с использованием полей TOA и TA.

```

 public void fieldTOA() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOA field, which will create an entry for each TA field in the document,
     // displaying long citations and page numbers for each entry.
     FieldToa fieldToa = (FieldToa) builder.insertField(FieldType.FIELD_TOA, false);

     // Set the entry category for our table. This TOA will now only include TA fields
     // that have a matching value in their EntryCategory property.
     fieldToa.setEntryCategory("1");

     // Moreover, the Table of Authorities category at index 1 is "Cases",
     // which will show up as our table's title if we set this variable to true.
     fieldToa.setUseHeading(true);

     // We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
     fieldToa.setBookmarkName("MyBookmark");

     // By default, a dotted line page-wide tab appears between the TA field's citation
     // and its page number. We can replace it with any text we put on this property.
     // Inserting a tab character will preserve the original tab.
     fieldToa.setEntrySeparator(" \t p.");

     // If we have multiple TA entries that share the same long citation,
     // all their respective page numbers will show up on one row.
     // We can use this property to specify a string that will separate their page numbers.
     fieldToa.setPageNumberListSeparator(" & p. ");

     // We can set this to true to get our table to display the word "passim"
     // if there are five or more page numbers in one row.
     fieldToa.setUsePassim(true);

     // One TA field can refer to a range of pages.
     // We can specify a string here to appear between the start and end page numbers for such ranges.
     fieldToa.setPageRangeSeparator(" to ");

     // The format from the TA fields will carry over into our table.
     // We can disable this by setting the RemoveEntryFormatting flag.
     fieldToa.setRemoveEntryFormatting(true);
     builder.getFont().setColor(Color.GREEN);
     builder.getFont().setName("Arial Black");

     Assert.assertEquals(fieldToa.getFieldCode(), " TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f");

     builder.insertBreak(BreakType.PAGE_BREAK);

     // This TA field will not appear as an entry in the TOA since it is outside
     // the bookmark's bounds that the TOA's BookmarkName property specifies.
     FieldTA fieldTA = insertToaEntry(builder, "1", "Source 1");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 1\"");

     // This TA field is inside the bookmark,
     // but the entry category does not match that of the table, so the TA field will not include it.
     builder.startBookmark("MyBookmark");
     fieldTA = insertToaEntry(builder, "2", "Source 2");

     // This entry will appear in the table.
     fieldTA = insertToaEntry(builder, "1", "Source 3");

     // A TOA table does not display short citations,
     // but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
     fieldTA.setShortCitation("S.3");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\s S.3");

     // We can format the page number to make it bold/italic using the following properties.
     // We will still see these effects if we set our table to ignore formatting.
     fieldTA = insertToaEntry(builder, "1", "Source 2");
     fieldTA.isBold(true);
     fieldTA.isItalic(true);

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 2\" \\b \\i");

     // We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
     // Note that this entry refers to the same source as the one above to share one row in our table.
     // This row will have the page number of the entry above and the page range of this entry,
     // with the table's page list and page number range separators between page numbers.
     fieldTA = insertToaEntry(builder, "1", "Source 3");
     fieldTA.setPageRangeBookmarkName("MyMultiPageBookmark");

     builder.startBookmark("MyMultiPageBookmark");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.endBookmark("MyMultiPageBookmark");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark");

     // If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
     for (int i = 0; i < 5; i++) {
         insertToaEntry(builder, "1", "Source 4");
     }

     builder.endBookmark("MyBookmark");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOA.TA.docx");
 }

 private static FieldTA insertToaEntry(DocumentBuilder builder, String entryCategory, String longCitation) throws Exception {
     FieldTA field = (FieldTA) builder.insertField(FieldType.FIELD_TOA_ENTRY, false);
     field.setEntryCategory(entryCategory);
     field.setLongCitation(longCitation);

     builder.insertBreak(BreakType.PAGE_BREAK);

     return field;
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Следует ли применять полужирное форматирование к номеру страницы записи. |

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

### isItalic() {#isItalic}
```
public boolean isItalic()
```


Получает, следует ли применять курсивное форматирование к номеру страницы записи.

 **Examples:** 

Показывает, как создавать и настраивать таблицу указателей с использованием полей TOA и TA.

```

 public void fieldTOA() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOA field, which will create an entry for each TA field in the document,
     // displaying long citations and page numbers for each entry.
     FieldToa fieldToa = (FieldToa) builder.insertField(FieldType.FIELD_TOA, false);

     // Set the entry category for our table. This TOA will now only include TA fields
     // that have a matching value in their EntryCategory property.
     fieldToa.setEntryCategory("1");

     // Moreover, the Table of Authorities category at index 1 is "Cases",
     // which will show up as our table's title if we set this variable to true.
     fieldToa.setUseHeading(true);

     // We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
     fieldToa.setBookmarkName("MyBookmark");

     // By default, a dotted line page-wide tab appears between the TA field's citation
     // and its page number. We can replace it with any text we put on this property.
     // Inserting a tab character will preserve the original tab.
     fieldToa.setEntrySeparator(" \t p.");

     // If we have multiple TA entries that share the same long citation,
     // all their respective page numbers will show up on one row.
     // We can use this property to specify a string that will separate their page numbers.
     fieldToa.setPageNumberListSeparator(" & p. ");

     // We can set this to true to get our table to display the word "passim"
     // if there are five or more page numbers in one row.
     fieldToa.setUsePassim(true);

     // One TA field can refer to a range of pages.
     // We can specify a string here to appear between the start and end page numbers for such ranges.
     fieldToa.setPageRangeSeparator(" to ");

     // The format from the TA fields will carry over into our table.
     // We can disable this by setting the RemoveEntryFormatting flag.
     fieldToa.setRemoveEntryFormatting(true);
     builder.getFont().setColor(Color.GREEN);
     builder.getFont().setName("Arial Black");

     Assert.assertEquals(fieldToa.getFieldCode(), " TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f");

     builder.insertBreak(BreakType.PAGE_BREAK);

     // This TA field will not appear as an entry in the TOA since it is outside
     // the bookmark's bounds that the TOA's BookmarkName property specifies.
     FieldTA fieldTA = insertToaEntry(builder, "1", "Source 1");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 1\"");

     // This TA field is inside the bookmark,
     // but the entry category does not match that of the table, so the TA field will not include it.
     builder.startBookmark("MyBookmark");
     fieldTA = insertToaEntry(builder, "2", "Source 2");

     // This entry will appear in the table.
     fieldTA = insertToaEntry(builder, "1", "Source 3");

     // A TOA table does not display short citations,
     // but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
     fieldTA.setShortCitation("S.3");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\s S.3");

     // We can format the page number to make it bold/italic using the following properties.
     // We will still see these effects if we set our table to ignore formatting.
     fieldTA = insertToaEntry(builder, "1", "Source 2");
     fieldTA.isBold(true);
     fieldTA.isItalic(true);

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 2\" \\b \\i");

     // We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
     // Note that this entry refers to the same source as the one above to share one row in our table.
     // This row will have the page number of the entry above and the page range of this entry,
     // with the table's page list and page number range separators between page numbers.
     fieldTA = insertToaEntry(builder, "1", "Source 3");
     fieldTA.setPageRangeBookmarkName("MyMultiPageBookmark");

     builder.startBookmark("MyMultiPageBookmark");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.endBookmark("MyMultiPageBookmark");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark");

     // If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
     for (int i = 0; i < 5; i++) {
         insertToaEntry(builder, "1", "Source 4");
     }

     builder.endBookmark("MyBookmark");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOA.TA.docx");
 }

 private static FieldTA insertToaEntry(DocumentBuilder builder, String entryCategory, String longCitation) throws Exception {
     FieldTA field = (FieldTA) builder.insertField(FieldType.FIELD_TOA_ENTRY, false);
     field.setEntryCategory(entryCategory);
     field.setLongCitation(longCitation);

     builder.insertBreak(BreakType.PAGE_BREAK);

     return field;
 }
 
```

**Returns:**
boolean — следует ли применять курсивное форматирование к номеру страницы записи.
### isItalic(boolean value) {#isItalic-boolean}
```
public void isItalic(boolean value)
```


Устанавливает, следует ли применять курсивное форматирование к номеру страницы записи.

 **Examples:** 

Показывает, как создавать и настраивать таблицу указателей с использованием полей TOA и TA.

```

 public void fieldTOA() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOA field, which will create an entry for each TA field in the document,
     // displaying long citations and page numbers for each entry.
     FieldToa fieldToa = (FieldToa) builder.insertField(FieldType.FIELD_TOA, false);

     // Set the entry category for our table. This TOA will now only include TA fields
     // that have a matching value in their EntryCategory property.
     fieldToa.setEntryCategory("1");

     // Moreover, the Table of Authorities category at index 1 is "Cases",
     // which will show up as our table's title if we set this variable to true.
     fieldToa.setUseHeading(true);

     // We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
     fieldToa.setBookmarkName("MyBookmark");

     // By default, a dotted line page-wide tab appears between the TA field's citation
     // and its page number. We can replace it with any text we put on this property.
     // Inserting a tab character will preserve the original tab.
     fieldToa.setEntrySeparator(" \t p.");

     // If we have multiple TA entries that share the same long citation,
     // all their respective page numbers will show up on one row.
     // We can use this property to specify a string that will separate their page numbers.
     fieldToa.setPageNumberListSeparator(" & p. ");

     // We can set this to true to get our table to display the word "passim"
     // if there are five or more page numbers in one row.
     fieldToa.setUsePassim(true);

     // One TA field can refer to a range of pages.
     // We can specify a string here to appear between the start and end page numbers for such ranges.
     fieldToa.setPageRangeSeparator(" to ");

     // The format from the TA fields will carry over into our table.
     // We can disable this by setting the RemoveEntryFormatting flag.
     fieldToa.setRemoveEntryFormatting(true);
     builder.getFont().setColor(Color.GREEN);
     builder.getFont().setName("Arial Black");

     Assert.assertEquals(fieldToa.getFieldCode(), " TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f");

     builder.insertBreak(BreakType.PAGE_BREAK);

     // This TA field will not appear as an entry in the TOA since it is outside
     // the bookmark's bounds that the TOA's BookmarkName property specifies.
     FieldTA fieldTA = insertToaEntry(builder, "1", "Source 1");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 1\"");

     // This TA field is inside the bookmark,
     // but the entry category does not match that of the table, so the TA field will not include it.
     builder.startBookmark("MyBookmark");
     fieldTA = insertToaEntry(builder, "2", "Source 2");

     // This entry will appear in the table.
     fieldTA = insertToaEntry(builder, "1", "Source 3");

     // A TOA table does not display short citations,
     // but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
     fieldTA.setShortCitation("S.3");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\s S.3");

     // We can format the page number to make it bold/italic using the following properties.
     // We will still see these effects if we set our table to ignore formatting.
     fieldTA = insertToaEntry(builder, "1", "Source 2");
     fieldTA.isBold(true);
     fieldTA.isItalic(true);

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 2\" \\b \\i");

     // We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
     // Note that this entry refers to the same source as the one above to share one row in our table.
     // This row will have the page number of the entry above and the page range of this entry,
     // with the table's page list and page number range separators between page numbers.
     fieldTA = insertToaEntry(builder, "1", "Source 3");
     fieldTA.setPageRangeBookmarkName("MyMultiPageBookmark");

     builder.startBookmark("MyMultiPageBookmark");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.endBookmark("MyMultiPageBookmark");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark");

     // If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
     for (int i = 0; i < 5; i++) {
         insertToaEntry(builder, "1", "Source 4");
     }

     builder.endBookmark("MyBookmark");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOA.TA.docx");
 }

 private static FieldTA insertToaEntry(DocumentBuilder builder, String entryCategory, String longCitation) throws Exception {
     FieldTA field = (FieldTA) builder.insertField(FieldType.FIELD_TOA_ENTRY, false);
     field.setEntryCategory(entryCategory);
     field.setLongCitation(longCitation);

     builder.insertBreak(BreakType.PAGE_BREAK);

     return field;
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Следует ли применять курсивное форматирование к номеру страницы записи. |

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
### setEntryCategory(String value) {#setEntryCategory-java.lang.String}
```
public void setEntryCategory(String value)
```


Устанавливает целую категорию записи, которая представляет собой число, соответствующее порядку категорий.

 **Examples:** 

Показывает, как создавать и настраивать таблицу указателей с использованием полей TOA и TA.

```

 public void fieldTOA() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOA field, which will create an entry for each TA field in the document,
     // displaying long citations and page numbers for each entry.
     FieldToa fieldToa = (FieldToa) builder.insertField(FieldType.FIELD_TOA, false);

     // Set the entry category for our table. This TOA will now only include TA fields
     // that have a matching value in their EntryCategory property.
     fieldToa.setEntryCategory("1");

     // Moreover, the Table of Authorities category at index 1 is "Cases",
     // which will show up as our table's title if we set this variable to true.
     fieldToa.setUseHeading(true);

     // We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
     fieldToa.setBookmarkName("MyBookmark");

     // By default, a dotted line page-wide tab appears between the TA field's citation
     // and its page number. We can replace it with any text we put on this property.
     // Inserting a tab character will preserve the original tab.
     fieldToa.setEntrySeparator(" \t p.");

     // If we have multiple TA entries that share the same long citation,
     // all their respective page numbers will show up on one row.
     // We can use this property to specify a string that will separate their page numbers.
     fieldToa.setPageNumberListSeparator(" & p. ");

     // We can set this to true to get our table to display the word "passim"
     // if there are five or more page numbers in one row.
     fieldToa.setUsePassim(true);

     // One TA field can refer to a range of pages.
     // We can specify a string here to appear between the start and end page numbers for such ranges.
     fieldToa.setPageRangeSeparator(" to ");

     // The format from the TA fields will carry over into our table.
     // We can disable this by setting the RemoveEntryFormatting flag.
     fieldToa.setRemoveEntryFormatting(true);
     builder.getFont().setColor(Color.GREEN);
     builder.getFont().setName("Arial Black");

     Assert.assertEquals(fieldToa.getFieldCode(), " TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f");

     builder.insertBreak(BreakType.PAGE_BREAK);

     // This TA field will not appear as an entry in the TOA since it is outside
     // the bookmark's bounds that the TOA's BookmarkName property specifies.
     FieldTA fieldTA = insertToaEntry(builder, "1", "Source 1");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 1\"");

     // This TA field is inside the bookmark,
     // but the entry category does not match that of the table, so the TA field will not include it.
     builder.startBookmark("MyBookmark");
     fieldTA = insertToaEntry(builder, "2", "Source 2");

     // This entry will appear in the table.
     fieldTA = insertToaEntry(builder, "1", "Source 3");

     // A TOA table does not display short citations,
     // but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
     fieldTA.setShortCitation("S.3");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\s S.3");

     // We can format the page number to make it bold/italic using the following properties.
     // We will still see these effects if we set our table to ignore formatting.
     fieldTA = insertToaEntry(builder, "1", "Source 2");
     fieldTA.isBold(true);
     fieldTA.isItalic(true);

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 2\" \\b \\i");

     // We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
     // Note that this entry refers to the same source as the one above to share one row in our table.
     // This row will have the page number of the entry above and the page range of this entry,
     // with the table's page list and page number range separators between page numbers.
     fieldTA = insertToaEntry(builder, "1", "Source 3");
     fieldTA.setPageRangeBookmarkName("MyMultiPageBookmark");

     builder.startBookmark("MyMultiPageBookmark");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.endBookmark("MyMultiPageBookmark");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark");

     // If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
     for (int i = 0; i < 5; i++) {
         insertToaEntry(builder, "1", "Source 4");
     }

     builder.endBookmark("MyBookmark");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOA.TA.docx");
 }

 private static FieldTA insertToaEntry(DocumentBuilder builder, String entryCategory, String longCitation) throws Exception {
     FieldTA field = (FieldTA) builder.insertField(FieldType.FIELD_TOA_ENTRY, false);
     field.setEntryCategory(entryCategory);
     field.setLongCitation(longCitation);

     builder.insertBreak(BreakType.PAGE_BREAK);

     return field;
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Целая категория записи, которая представляет собой число, соответствующее порядку категорий. |

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

### setLongCitation(String value) {#setLongCitation-java.lang.String}
```
public void setLongCitation(String value)
```


Устанавливает полную ссылку для записи.

 **Examples:** 

Показывает, как создавать и настраивать таблицу указателей с использованием полей TOA и TA.

```

 public void fieldTOA() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOA field, which will create an entry for each TA field in the document,
     // displaying long citations and page numbers for each entry.
     FieldToa fieldToa = (FieldToa) builder.insertField(FieldType.FIELD_TOA, false);

     // Set the entry category for our table. This TOA will now only include TA fields
     // that have a matching value in their EntryCategory property.
     fieldToa.setEntryCategory("1");

     // Moreover, the Table of Authorities category at index 1 is "Cases",
     // which will show up as our table's title if we set this variable to true.
     fieldToa.setUseHeading(true);

     // We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
     fieldToa.setBookmarkName("MyBookmark");

     // By default, a dotted line page-wide tab appears between the TA field's citation
     // and its page number. We can replace it with any text we put on this property.
     // Inserting a tab character will preserve the original tab.
     fieldToa.setEntrySeparator(" \t p.");

     // If we have multiple TA entries that share the same long citation,
     // all their respective page numbers will show up on one row.
     // We can use this property to specify a string that will separate their page numbers.
     fieldToa.setPageNumberListSeparator(" & p. ");

     // We can set this to true to get our table to display the word "passim"
     // if there are five or more page numbers in one row.
     fieldToa.setUsePassim(true);

     // One TA field can refer to a range of pages.
     // We can specify a string here to appear between the start and end page numbers for such ranges.
     fieldToa.setPageRangeSeparator(" to ");

     // The format from the TA fields will carry over into our table.
     // We can disable this by setting the RemoveEntryFormatting flag.
     fieldToa.setRemoveEntryFormatting(true);
     builder.getFont().setColor(Color.GREEN);
     builder.getFont().setName("Arial Black");

     Assert.assertEquals(fieldToa.getFieldCode(), " TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f");

     builder.insertBreak(BreakType.PAGE_BREAK);

     // This TA field will not appear as an entry in the TOA since it is outside
     // the bookmark's bounds that the TOA's BookmarkName property specifies.
     FieldTA fieldTA = insertToaEntry(builder, "1", "Source 1");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 1\"");

     // This TA field is inside the bookmark,
     // but the entry category does not match that of the table, so the TA field will not include it.
     builder.startBookmark("MyBookmark");
     fieldTA = insertToaEntry(builder, "2", "Source 2");

     // This entry will appear in the table.
     fieldTA = insertToaEntry(builder, "1", "Source 3");

     // A TOA table does not display short citations,
     // but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
     fieldTA.setShortCitation("S.3");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\s S.3");

     // We can format the page number to make it bold/italic using the following properties.
     // We will still see these effects if we set our table to ignore formatting.
     fieldTA = insertToaEntry(builder, "1", "Source 2");
     fieldTA.isBold(true);
     fieldTA.isItalic(true);

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 2\" \\b \\i");

     // We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
     // Note that this entry refers to the same source as the one above to share one row in our table.
     // This row will have the page number of the entry above and the page range of this entry,
     // with the table's page list and page number range separators between page numbers.
     fieldTA = insertToaEntry(builder, "1", "Source 3");
     fieldTA.setPageRangeBookmarkName("MyMultiPageBookmark");

     builder.startBookmark("MyMultiPageBookmark");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.endBookmark("MyMultiPageBookmark");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark");

     // If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
     for (int i = 0; i < 5; i++) {
         insertToaEntry(builder, "1", "Source 4");
     }

     builder.endBookmark("MyBookmark");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOA.TA.docx");
 }

 private static FieldTA insertToaEntry(DocumentBuilder builder, String entryCategory, String longCitation) throws Exception {
     FieldTA field = (FieldTA) builder.insertField(FieldType.FIELD_TOA_ENTRY, false);
     field.setEntryCategory(entryCategory);
     field.setLongCitation(longCitation);

     builder.insertBreak(BreakType.PAGE_BREAK);

     return field;
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Полная ссылка для записи. |

### setPageRangeBookmarkName(String value) {#setPageRangeBookmarkName-java.lang.String}
```
public void setPageRangeBookmarkName(String value)
```


Устанавливает имя закладки, отмечающей диапазон страниц, который вставляется как номер страницы записи.

 **Examples:** 

Показывает, как создавать и настраивать таблицу указателей с использованием полей TOA и TA.

```

 public void fieldTOA() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOA field, which will create an entry for each TA field in the document,
     // displaying long citations and page numbers for each entry.
     FieldToa fieldToa = (FieldToa) builder.insertField(FieldType.FIELD_TOA, false);

     // Set the entry category for our table. This TOA will now only include TA fields
     // that have a matching value in their EntryCategory property.
     fieldToa.setEntryCategory("1");

     // Moreover, the Table of Authorities category at index 1 is "Cases",
     // which will show up as our table's title if we set this variable to true.
     fieldToa.setUseHeading(true);

     // We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
     fieldToa.setBookmarkName("MyBookmark");

     // By default, a dotted line page-wide tab appears between the TA field's citation
     // and its page number. We can replace it with any text we put on this property.
     // Inserting a tab character will preserve the original tab.
     fieldToa.setEntrySeparator(" \t p.");

     // If we have multiple TA entries that share the same long citation,
     // all their respective page numbers will show up on one row.
     // We can use this property to specify a string that will separate their page numbers.
     fieldToa.setPageNumberListSeparator(" & p. ");

     // We can set this to true to get our table to display the word "passim"
     // if there are five or more page numbers in one row.
     fieldToa.setUsePassim(true);

     // One TA field can refer to a range of pages.
     // We can specify a string here to appear between the start and end page numbers for such ranges.
     fieldToa.setPageRangeSeparator(" to ");

     // The format from the TA fields will carry over into our table.
     // We can disable this by setting the RemoveEntryFormatting flag.
     fieldToa.setRemoveEntryFormatting(true);
     builder.getFont().setColor(Color.GREEN);
     builder.getFont().setName("Arial Black");

     Assert.assertEquals(fieldToa.getFieldCode(), " TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f");

     builder.insertBreak(BreakType.PAGE_BREAK);

     // This TA field will not appear as an entry in the TOA since it is outside
     // the bookmark's bounds that the TOA's BookmarkName property specifies.
     FieldTA fieldTA = insertToaEntry(builder, "1", "Source 1");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 1\"");

     // This TA field is inside the bookmark,
     // but the entry category does not match that of the table, so the TA field will not include it.
     builder.startBookmark("MyBookmark");
     fieldTA = insertToaEntry(builder, "2", "Source 2");

     // This entry will appear in the table.
     fieldTA = insertToaEntry(builder, "1", "Source 3");

     // A TOA table does not display short citations,
     // but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
     fieldTA.setShortCitation("S.3");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\s S.3");

     // We can format the page number to make it bold/italic using the following properties.
     // We will still see these effects if we set our table to ignore formatting.
     fieldTA = insertToaEntry(builder, "1", "Source 2");
     fieldTA.isBold(true);
     fieldTA.isItalic(true);

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 2\" \\b \\i");

     // We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
     // Note that this entry refers to the same source as the one above to share one row in our table.
     // This row will have the page number of the entry above and the page range of this entry,
     // with the table's page list and page number range separators between page numbers.
     fieldTA = insertToaEntry(builder, "1", "Source 3");
     fieldTA.setPageRangeBookmarkName("MyMultiPageBookmark");

     builder.startBookmark("MyMultiPageBookmark");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.endBookmark("MyMultiPageBookmark");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark");

     // If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
     for (int i = 0; i < 5; i++) {
         insertToaEntry(builder, "1", "Source 4");
     }

     builder.endBookmark("MyBookmark");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOA.TA.docx");
 }

 private static FieldTA insertToaEntry(DocumentBuilder builder, String entryCategory, String longCitation) throws Exception {
     FieldTA field = (FieldTA) builder.insertField(FieldType.FIELD_TOA_ENTRY, false);
     field.setEntryCategory(entryCategory);
     field.setLongCitation(longCitation);

     builder.insertBreak(BreakType.PAGE_BREAK);

     return field;
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Имя закладки, которое отмечает диапазон страниц, вставляемый как номер страницы записи. |

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

### setShortCitation(String value) {#setShortCitation-java.lang.String}
```
public void setShortCitation(String value)
```


Устанавливает краткую ссылку для записи.

 **Examples:** 

Показывает, как создавать и настраивать таблицу указателей с использованием полей TOA и TA.

```

 public void fieldTOA() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOA field, which will create an entry for each TA field in the document,
     // displaying long citations and page numbers for each entry.
     FieldToa fieldToa = (FieldToa) builder.insertField(FieldType.FIELD_TOA, false);

     // Set the entry category for our table. This TOA will now only include TA fields
     // that have a matching value in their EntryCategory property.
     fieldToa.setEntryCategory("1");

     // Moreover, the Table of Authorities category at index 1 is "Cases",
     // which will show up as our table's title if we set this variable to true.
     fieldToa.setUseHeading(true);

     // We can further filter TA fields by naming a bookmark that they will need to be within the TOA bounds.
     fieldToa.setBookmarkName("MyBookmark");

     // By default, a dotted line page-wide tab appears between the TA field's citation
     // and its page number. We can replace it with any text we put on this property.
     // Inserting a tab character will preserve the original tab.
     fieldToa.setEntrySeparator(" \t p.");

     // If we have multiple TA entries that share the same long citation,
     // all their respective page numbers will show up on one row.
     // We can use this property to specify a string that will separate their page numbers.
     fieldToa.setPageNumberListSeparator(" & p. ");

     // We can set this to true to get our table to display the word "passim"
     // if there are five or more page numbers in one row.
     fieldToa.setUsePassim(true);

     // One TA field can refer to a range of pages.
     // We can specify a string here to appear between the start and end page numbers for such ranges.
     fieldToa.setPageRangeSeparator(" to ");

     // The format from the TA fields will carry over into our table.
     // We can disable this by setting the RemoveEntryFormatting flag.
     fieldToa.setRemoveEntryFormatting(true);
     builder.getFont().setColor(Color.GREEN);
     builder.getFont().setName("Arial Black");

     Assert.assertEquals(fieldToa.getFieldCode(), " TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f");

     builder.insertBreak(BreakType.PAGE_BREAK);

     // This TA field will not appear as an entry in the TOA since it is outside
     // the bookmark's bounds that the TOA's BookmarkName property specifies.
     FieldTA fieldTA = insertToaEntry(builder, "1", "Source 1");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 1\"");

     // This TA field is inside the bookmark,
     // but the entry category does not match that of the table, so the TA field will not include it.
     builder.startBookmark("MyBookmark");
     fieldTA = insertToaEntry(builder, "2", "Source 2");

     // This entry will appear in the table.
     fieldTA = insertToaEntry(builder, "1", "Source 3");

     // A TOA table does not display short citations,
     // but we can use them as a shorthand to refer to bulky source names that multiple TA fields reference.
     fieldTA.setShortCitation("S.3");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\s S.3");

     // We can format the page number to make it bold/italic using the following properties.
     // We will still see these effects if we set our table to ignore formatting.
     fieldTA = insertToaEntry(builder, "1", "Source 2");
     fieldTA.isBold(true);
     fieldTA.isItalic(true);

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 2\" \\b \\i");

     // We can configure TA fields to get their TOA entries to refer to a range of pages that a bookmark spans across.
     // Note that this entry refers to the same source as the one above to share one row in our table.
     // This row will have the page number of the entry above and the page range of this entry,
     // with the table's page list and page number range separators between page numbers.
     fieldTA = insertToaEntry(builder, "1", "Source 3");
     fieldTA.setPageRangeBookmarkName("MyMultiPageBookmark");

     builder.startBookmark("MyMultiPageBookmark");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.endBookmark("MyMultiPageBookmark");

     Assert.assertEquals(fieldTA.getFieldCode(), " TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark");

     // If we have enabled the "Passim" feature of our table, having 5 or more TA entries with the same source will invoke it.
     for (int i = 0; i < 5; i++) {
         insertToaEntry(builder, "1", "Source 4");
     }

     builder.endBookmark("MyBookmark");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOA.TA.docx");
 }

 private static FieldTA insertToaEntry(DocumentBuilder builder, String entryCategory, String longCitation) throws Exception {
     FieldTA field = (FieldTA) builder.insertField(FieldType.FIELD_TOA_ENTRY, false);
     field.setEntryCategory(entryCategory);
     field.setLongCitation(longCitation);

     builder.insertBreak(BreakType.PAGE_BREAK);

     return field;
 }
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Краткая ссылка для записи. |

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

