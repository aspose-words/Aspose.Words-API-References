---
title: FieldToa
linktitle: FieldToa
second_title: Aspose.Words for Java
description: Implements the TOA field in Java.
type: docs
weight: 266
url: /java/com.aspose.words/fieldtoa/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldToa extends Field
```

Implements the TOA field.

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.

 **Remarks:** 

Builds a table of authorities (that is, a list of the references in a legal document, such as references to cases, statutes, and rules, along with the numbers of the pages on which the references appear) using the entries specified by TA fields.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
## Methods

| Method | Description |
| --- | --- |
| [getBookmarkName()](#getBookmarkName) | Gets the name of the bookmark that marks the portion of the document used to build the table. |
| [getDisplayResult()](#getDisplayResult) | Gets the text that represents the displayed field result. |
| [getEnd()](#getEnd) | Gets the node that represents the field end. |
| [getEntryCategory()](#getEntryCategory) | Gets the integral category for entries included in the table. |
| [getEntrySeparator()](#getEntrySeparator) | Gets the character sequence that is used to separate a table of authorities entry and its page number. |
| [getFieldCode()](#getFieldCode) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Returns text between field start and field separator (or field end if there is no separator). |
| [getFormat()](#getFormat) | Gets a [FieldFormat](../../com.aspose.words/fieldformat/) object that provides typed access to field's formatting. |
| [getLocaleId()](#getLocaleId) | Gets the LCID of the field. |
| [getPageNumberListSeparator()](#getPageNumberListSeparator) | Gets the character sequence that is used to separate two page numbers in a page number list. |
| [getPageRangeSeparator()](#getPageRangeSeparator) | Gets the character sequence that is used to separate the start and end of a page range. |
| [getRemoveEntryFormatting()](#getRemoveEntryFormatting) | Gets whether to remove the formatting of the entry text in the document from the entry in the table of authorities. |
| [getResult()](#getResult) | Gets text that is between the field separator and field end. |
| [getSeparator()](#getSeparator) | Gets the node that represents the field separator. |
| [getSequenceName()](#getSequenceName) | Gets the name of a sequence whose number is included with the page number. |
| [getSequenceSeparator()](#getSequenceSeparator) | Gets the character sequence that is used to separate sequence numbers and page numbers. |
| [getStart()](#getStart) | Gets the node that represents the start of the field. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getType()](#getType) | Gets the Microsoft Word field type. |
| [getUseHeading()](#getUseHeading) | Gets whether to include the category heading for the entries in a table of authorities. |
| [getUsePassim()](#getUsePassim) | Gets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited. |
| [isDirty()](#isDirty) | Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isDirty(boolean value)](#isDirty-boolean) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [isLocked()](#isLocked) | Gets whether the field is locked (should not recalculate its result). |
| [isLocked(boolean value)](#isLocked-boolean) | Sets whether the field is locked (should not recalculate its result). |
| [remove()](#remove) | Removes the field from the document. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String) | Sets the name of the bookmark that marks the portion of the document used to build the table. |
| [setEntryCategory(String value)](#setEntryCategory-java.lang.String) | Sets the integral category for entries included in the table. |
| [setEntrySeparator(String value)](#setEntrySeparator-java.lang.String) | Sets the character sequence that is used to separate a table of authorities entry and its page number. |
| [setLocaleId(int value)](#setLocaleId-int) | Sets the LCID of the field. |
| [setPageNumberListSeparator(String value)](#setPageNumberListSeparator-java.lang.String) | Sets the character sequence that is used to separate two page numbers in a page number list. |
| [setPageRangeSeparator(String value)](#setPageRangeSeparator-java.lang.String) | Sets the character sequence that is used to separate the start and end of a page range. |
| [setRemoveEntryFormatting(boolean value)](#setRemoveEntryFormatting-boolean) | Sets whether to remove the formatting of the entry text in the document from the entry in the table of authorities. |
| [setResult(String value)](#setResult-java.lang.String) | Sets text that is between the field separator and field end. |
| [setSequenceName(String value)](#setSequenceName-java.lang.String) | Sets the name of a sequence whose number is included with the page number. |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String) | Sets the character sequence that is used to separate sequence numbers and page numbers. |
| [setUseHeading(boolean value)](#setUseHeading-boolean) | Sets whether to include the category heading for the entries in a table of authorities. |
| [setUsePassim(boolean value)](#setUsePassim-boolean) | Sets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited. |
| [unlink()](#unlink) | Performs the field unlink. |
| [update()](#update) | Performs the field update. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Performs a field update. |
### getBookmarkName() {#getBookmarkName}
```
public String getBookmarkName()
```


Gets the name of the bookmark that marks the portion of the document used to build the table.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
java.lang.String - The name of the bookmark that marks the portion of the document used to build the table.
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


Gets the text that represents the displayed field result.

 **Remarks:** 

The [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) method must be called to obtain correct value for the [FieldListNum](../../com.aspose.words/fieldlistnum/), [FieldAutoNum](../../com.aspose.words/fieldautonum/), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout/) and [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl/) fields.

 **Examples:** 

Shows how to get the real text that a field displays in the document.

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
java.lang.String - The text that represents the displayed field result.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Gets the node that represents the field end.

 **Examples:** 

Shows how to work with a collection of fields.

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


Gets the integral category for entries included in the table.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
java.lang.String - The integral category for entries included in the table.
### getEntrySeparator() {#getEntrySeparator}
```
public String getEntrySeparator()
```


Gets the character sequence that is used to separate a table of authorities entry and its page number.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
java.lang.String - The character sequence that is used to separate a table of authorities entry and its page number.
### getFieldCode() {#getFieldCode}
```
public String getFieldCode()
```


Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.

 **Examples:** 

Shows how to insert a field into a document using a field code.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Shows how to get a field's field code.

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


Returns text between field start and field separator (or field end if there is no separator).

 **Examples:** 

Shows how to get a field's field code.

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
| Parameter | Type | Description |
| --- | --- | --- |
| includeChildFieldCodes | boolean |  true  if child field codes should be included. |

**Returns:**
java.lang.String
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Gets a [FieldFormat](../../com.aspose.words/fieldformat/) object that provides typed access to field's formatting.

 **Examples:** 

Shows how to format field results.

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


Gets the LCID of the field.

 **Examples:** 

Shows how to insert a field and work with its locale.

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
int - The LCID of the field.
### getPageNumberListSeparator() {#getPageNumberListSeparator}
```
public String getPageNumberListSeparator()
```


Gets the character sequence that is used to separate two page numbers in a page number list.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
java.lang.String - The character sequence that is used to separate two page numbers in a page number list.
### getPageRangeSeparator() {#getPageRangeSeparator}
```
public String getPageRangeSeparator()
```


Gets the character sequence that is used to separate the start and end of a page range.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
java.lang.String - The character sequence that is used to separate the start and end of a page range.
### getRemoveEntryFormatting() {#getRemoveEntryFormatting}
```
public boolean getRemoveEntryFormatting()
```


Gets whether to remove the formatting of the entry text in the document from the entry in the table of authorities.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
boolean - Whether to remove the formatting of the entry text in the document from the entry in the table of authorities.
### getResult() {#getResult}
```
public String getResult()
```


Gets text that is between the field separator and field end.

 **Examples:** 

Shows how to insert a field into a document using a field code.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
java.lang.String - Text that is between the field separator and field end.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Gets the node that represents the field separator. Can be  null .

 **Examples:** 

Shows how to work with a collection of fields.

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


Gets the name of a sequence whose number is included with the page number.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
java.lang.String - The name of a sequence whose number is included with the page number.
### getSequenceSeparator() {#getSequenceSeparator}
```
public String getSequenceSeparator()
```


Gets the character sequence that is used to separate sequence numbers and page numbers.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
java.lang.String - The character sequence that is used to separate sequence numbers and page numbers.
### getStart() {#getStart}
```
public FieldStart getStart()
```


Gets the node that represents the start of the field.

 **Examples:** 

Shows how to work with a collection of fields.

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
| Parameter | Type | Description |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getType() {#getType}
```
public int getType()
```


Gets the Microsoft Word field type.

 **Examples:** 

Shows how to insert a field into a document using a field code.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
int - The Microsoft Word field type. The returned value is one of [FieldType](../../com.aspose.words/fieldtype/) constants.
### getUseHeading() {#getUseHeading}
```
public boolean getUseHeading()
```


Gets whether to include the category heading for the entries in a table of authorities.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
boolean - Whether to include the category heading for the entries in a table of authorities.
### getUsePassim() {#getUsePassim}
```
public boolean getUsePassim()
```


Gets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
boolean - Whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited.
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Gets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

 **Examples:** 

Shows how to use special property for updating field result.

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
boolean - Whether the current result of the field is no longer correct (stale) due to other modifications made to the document.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

 **Examples:** 

Shows how to use special property for updating field result.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |

### isLocked() {#isLocked}
```
public boolean isLocked()
```


Gets whether the field is locked (should not recalculate its result).

 **Examples:** 

Shows how to work with a FieldStart node.

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
boolean - Whether the field is locked (should not recalculate its result).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Sets whether the field is locked (should not recalculate its result).

 **Examples:** 

Shows how to work with a FieldStart node.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether the field is locked (should not recalculate its result). |

### remove() {#remove}
```
public Node remove()
```


Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns  null .

 **Examples:** 

Shows how to remove fields from a field collection.

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

Shows how to process PRIVATE fields.

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


Sets the name of the bookmark that marks the portion of the document used to build the table.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the bookmark that marks the portion of the document used to build the table. |

### setEntryCategory(String value) {#setEntryCategory-java.lang.String}
```
public void setEntryCategory(String value)
```


Sets the integral category for entries included in the table.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The integral category for entries included in the table. |

### setEntrySeparator(String value) {#setEntrySeparator-java.lang.String}
```
public void setEntrySeparator(String value)
```


Sets the character sequence that is used to separate a table of authorities entry and its page number.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate a table of authorities entry and its page number. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Sets the LCID of the field.

 **Examples:** 

Shows how to insert a field and work with its locale.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The LCID of the field. |

### setPageNumberListSeparator(String value) {#setPageNumberListSeparator-java.lang.String}
```
public void setPageNumberListSeparator(String value)
```


Sets the character sequence that is used to separate two page numbers in a page number list.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate two page numbers in a page number list. |

### setPageRangeSeparator(String value) {#setPageRangeSeparator-java.lang.String}
```
public void setPageRangeSeparator(String value)
```


Sets the character sequence that is used to separate the start and end of a page range.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate the start and end of a page range. |

### setRemoveEntryFormatting(boolean value) {#setRemoveEntryFormatting-boolean}
```
public void setRemoveEntryFormatting(boolean value)
```


Sets whether to remove the formatting of the entry text in the document from the entry in the table of authorities.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to remove the formatting of the entry text in the document from the entry in the table of authorities. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Sets text that is between the field separator and field end.

 **Examples:** 

Shows how to insert a field into a document using a field code.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Text that is between the field separator and field end. |

### setSequenceName(String value) {#setSequenceName-java.lang.String}
```
public void setSequenceName(String value)
```


Sets the name of a sequence whose number is included with the page number.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of a sequence whose number is included with the page number. |

### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String}
```
public void setSequenceSeparator(String value)
```


Sets the character sequence that is used to separate sequence numbers and page numbers.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The character sequence that is used to separate sequence numbers and page numbers. |

### setUseHeading(boolean value) {#setUseHeading-boolean}
```
public void setUseHeading(boolean value)
```


Sets whether to include the category heading for the entries in a table of authorities.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to include the category heading for the entries in a table of authorities. |

### setUsePassim(boolean value) {#setUsePassim-boolean}
```
public void setUsePassim(boolean value)
```


Sets whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited.

 **Examples:** 

Shows how to build and customize a table of authorities using TOA and TA fields.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to replace five or more different page references to the same authority with "passim", which is used to indicate that a word or passage occurs frequently in the work cited. |

### unlink() {#unlink}
```
public boolean unlink()
```


Performs the field unlink.

 **Remarks:** 

Replaces the field with its most recent result.

Some fields, such as XE (Index Entry) fields and SEQ (Sequence) fields, cannot be unlinked.

 **Examples:** 

Shows how to unlink a field.

```

 Document doc = new Document(getMyDir() + "Linked fields.docx");
 doc.getRange().getFields().get(1).unlink();
 
```

**Returns:**
boolean -  true  if the field has been unlinked, otherwise  false .
### update() {#update}
```
public void update()
```


Performs the field update. Throws if the field is being updated already.

 **Examples:** 

Shows how to insert a field into a document using FieldType.

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

Shows how to format field results.

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


Performs a field update. Throws if the field is being updated already.

 **Examples:** 

Shows how to preserve or discard INCLUDEPICTURE fields when loading a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| ignoreMergeFormat | boolean | If  true  then direct field result formatting is abandoned, regardless of the MERGEFORMAT switch, otherwise normal update is performed. |

