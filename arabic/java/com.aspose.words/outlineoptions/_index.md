---
title: "OutlineOptions"
linktitle: "OutlineOptions"
second_title: "Aspose.Words لـ Java"
description: "يسمح بتحديد خيارات المخطط في Java."
type: docs
weight: 509
url: /ar/java/com.aspose.words/outlineoptions/
---

**Inheritance:**
java.lang.Object
```
public class OutlineOptions
```

يسمح بتحديد خيارات المخطط.

للتعرف على المزيد، زر [ Save a Document ][Save a Document] مقالة الوثائق.

 **Examples:** 

يوضح كيفية معالجة العلامات المرجعية في رؤوس/تذييلات الصفحات في مستند نقوم بتحويله إلى PDF.

```

 Document doc = new Document(getMyDir() + "Bookmarks in headers and footers.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "PageMode" property to "PdfPageMode.UseOutlines" to display the outline navigation pane in the output PDF.
 saveOptions.setPageMode(PdfPageMode.USE_OUTLINES);

 // Set the "DefaultBookmarksOutlineLevel" property to "1" to display all
 // bookmarks at the first level of the outline in the output PDF.
 saveOptions.getOutlineOptions().setDefaultBookmarksOutlineLevel(1);

 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.None" to
 // not export any bookmarks that are inside headers/footers.
 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.First" to
 // only export bookmarks in the first section's header/footers.
 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.All" to
 // export bookmarks that are in all headers/footers.
 saveOptions.setHeaderFooterBookmarksExportMode(headerFooterBookmarksExportMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
 
```


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getBookmarksOutlineLevels()](#getBookmarksOutlineLevels) | يسمح بتحديد مستوى مخطط العلامات المرجعية الفردية. |
| [getCreateMissingOutlineLevels()](#getCreateMissingOutlineLevels) | يحصل أو يعيّن قيمة تحدد ما إذا كان سيتم إنشاء مستويات مخطط مفقودة عند تصدير المستند أم لا. |
| [getCreateOutlinesForHeadingsInTables()](#getCreateOutlinesForHeadingsInTables) | يحدد ما إذا كان سيتم إنشاء مخططات للعناوين (الفقرات المنسقة بأنماط Heading) داخل الجداول أم لا. |
| [getDefaultBookmarksOutlineLevel()](#getDefaultBookmarksOutlineLevel) | يحدد المستوى الافتراضي في مخطط المستند الذي يتم فيه عرض علامات Word المرجعية. |
| [getExpandedOutlineLevels()](#getExpandedOutlineLevels) | يحدد عدد المستويات في مخطط المستند التي يتم توسيعها عند عرض الملف. |
| [getHeadingsOutlineLevels()](#getHeadingsOutlineLevels) | يحدد عدد مستويات العناوين (الفقرات المنسقة بأنماط Heading) التي تُدرج في مخطط المستند. |
| [setCreateMissingOutlineLevels(boolean value)](#setCreateMissingOutlineLevels-boolean) | يحصل أو يعيّن قيمة تحدد ما إذا كان سيتم إنشاء مستويات مخطط مفقودة عند تصدير المستند أم لا. |
| [setCreateOutlinesForHeadingsInTables(boolean value)](#setCreateOutlinesForHeadingsInTables-boolean) | يحدد ما إذا كان سيتم إنشاء مخططات للعناوين (الفقرات المنسقة بأنماط Heading) داخل الجداول أم لا. |
| [setDefaultBookmarksOutlineLevel(int value)](#setDefaultBookmarksOutlineLevel-int) | يحدد المستوى الافتراضي في مخطط المستند الذي يتم فيه عرض علامات Word المرجعية. |
| [setExpandedOutlineLevels(int value)](#setExpandedOutlineLevels-int) | يحدد عدد المستويات في مخطط المستند التي يتم توسيعها عند عرض الملف. |
| [setHeadingsOutlineLevels(int value)](#setHeadingsOutlineLevels-int) | يحدد عدد مستويات العناوين (الفقرات المنسقة بأنماط Heading) التي تُدرج في مخطط المستند. |
### getBookmarksOutlineLevels() {#getBookmarksOutlineLevels}
```
public BookmarksOutlineLevelCollection getBookmarksOutlineLevels()
```


يسمح بتحديد مستوى مخطط العلامات المرجعية الفردية.

 **Remarks:** 

إذا لم يتم تحديد مستوى العلامة المرجعية في هذه المجموعة، فسيتم استخدام قيمة [getDefaultBookmarksOutlineLevel()](../../com.aspose.words/outlineoptions/\#getDefaultBookmarksOutlineLevel) / [setDefaultBookmarksOutlineLevel(int)](../../com.aspose.words/outlineoptions/\#setDefaultBookmarksOutlineLevel-int).

 **Examples:** 

يوضح كيفية تعيين مستويات المخطط للإشارات المرجعية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bookmark with another bookmark nested inside it.
 builder.startBookmark("Bookmark 1");
 builder.writeln("Text inside Bookmark 1.");

 builder.startBookmark("Bookmark 2");
 builder.writeln("Text inside Bookmark 1 and 2.");
 builder.endBookmark("Bookmark 2");

 builder.writeln("Text inside Bookmark 1.");
 builder.endBookmark("Bookmark 1");

 // Insert another bookmark.
 builder.startBookmark("Bookmark 3");
 builder.writeln("Text inside Bookmark 3.");
 builder.endBookmark("Bookmark 3");

 // When saving to .pdf, bookmarks can be accessed via a drop-down menu and used as anchors by most readers.
 // Bookmarks can also have numeric values for outline levels,
 // enabling lower level outline entries to hide higher-level child entries when collapsed in the reader.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 BookmarksOutlineLevelCollection outlineLevels = pdfSaveOptions.getOutlineOptions().getBookmarksOutlineLevels();

 outlineLevels.add("Bookmark 1", 1);
 outlineLevels.add("Bookmark 2", 2);
 outlineLevels.add("Bookmark 3", 3);

 Assert.assertEquals(outlineLevels.getCount(), 3);
 Assert.assertTrue(outlineLevels.contains("Bookmark 1"));
 Assert.assertEquals(outlineLevels.get(0), 1);
 Assert.assertEquals(outlineLevels.get("Bookmark 2"), 2);
 Assert.assertEquals(outlineLevels.indexOfKey("Bookmark 3"), 2);

 // We can remove two elements so that only the outline level designation for "Bookmark 1" is left.
 outlineLevels.removeAt(2);
 outlineLevels.remove("Bookmark 2");

 // There are nine outline levels. Their numbering will be optimized during the save operation.
 // In this case, levels "5" and "9" will become "2" and "3".
 outlineLevels.add("Bookmark 2", 5);
 outlineLevels.add("Bookmark 3", 9);

 doc.save(getArtifactsDir() + "BookmarksOutlineLevelCollection.BookmarkLevels.pdf", pdfSaveOptions);

 // Emptying this collection will preserve the bookmarks and put them all on the same outline level.
 outlineLevels.clear();
 
```

**Returns:**
[BookmarksOutlineLevelCollection](../../com.aspose.words/bookmarksoutlinelevelcollection/) - The corresponding [BookmarksOutlineLevelCollection](../../com.aspose.words/bookmarksoutlinelevelcollection/) value.
### getCreateMissingOutlineLevels() {#getCreateMissingOutlineLevels}
```
public boolean getCreateMissingOutlineLevels()
```


يحصل أو يعيّن قيمة تحدد ما إذا كان سيتم إنشاء مستويات مخطط مفقودة عند تصدير المستند أم لا.

القيمة الافتراضية لهذه الخاصية هي false .

 **Examples:** 

يوضح كيفية التعامل مع مستويات المخطط التي لا تحتوي على أي عناوين مطابقة عند حفظ مستند PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings that can serve as TOC entries of levels 1 and 5.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_5);

 builder.writeln("Heading 1.1.1.1.1");
 builder.writeln("Heading 1.1.1.1.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "5" to include all headings of levels 5 and below in the outline.
 saveOptions.getOutlineOptions().setHeadingsOutlineLevels(5);

 // This document contains headings of levels 1 and 5, and no headings with levels of 2, 3, and 4.
 // The output PDF document will treat outline levels 2, 3, and 4 as "missing".
 // Set the "CreateMissingOutlineLevels" property to "true" to include all missing levels in the outline,
 // leaving blank outline entries since there are no usable headings.
 // Set the "CreateMissingOutlineLevels" property to "false" to ignore missing outline levels,
 // and treat the outline level 5 headings as level 2.
 saveOptions.getOutlineOptions().setCreateMissingOutlineLevels(createMissingOutlineLevels);

 doc.save(getArtifactsDir() + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getCreateOutlinesForHeadingsInTables() {#getCreateOutlinesForHeadingsInTables}
```
public boolean getCreateOutlinesForHeadingsInTables()
```


يحدد ما إذا كان سيتم إنشاء مخططات للعناوين (الفقرات المنسقة بأنماط Heading) داخل الجداول أم لا.

 **Remarks:** 

القيمة الافتراضية هي false .

 **Examples:** 

يوضح كيفية إنشاء إدخالات مخطط مستند PDF للعناوين داخل الجداول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a table with three rows. The first row,
 // whose text we will format in a heading-type style, will serve as the column header.
 builder.startTable();
 builder.insertCell();
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.write("Customers");
 builder.endRow();
 builder.insertCell();
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.write("John Doe");
 builder.endRow();
 builder.insertCell();
 builder.write("Jane Doe");
 builder.endTable();

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "1" to get the outline
 // to only register headings with heading levels that are no larger than 1.
 pdfSaveOptions.getOutlineOptions().setHeadingsOutlineLevels(1);

 // Set the "CreateOutlinesForHeadingsInTables" property to "false" to exclude all headings within tables,
 // such as the one we have created above from the outline.
 // Set the "CreateOutlinesForHeadingsInTables" property to "true" to include all headings within tables
 // in the outline, provided that they have a heading level that is no larger than the value of the "HeadingsOutlineLevels" property.
 pdfSaveOptions.getOutlineOptions().setCreateOutlinesForHeadingsInTables(createOutlinesForHeadingsInTables);

 doc.save(getArtifactsDir() + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getDefaultBookmarksOutlineLevel() {#getDefaultBookmarksOutlineLevel}
```
public int getDefaultBookmarksOutlineLevel()
```


يحدد المستوى الافتراضي في مخطط المستند الذي يتم فيه عرض علامات Word المرجعية.

 **Remarks:** 

يمكن تحديد مستوى العلامات المرجعية الفردية باستخدام خاصية [getBookmarksOutlineLevels()](../../com.aspose.words/outlineoptions/\#getBookmarksOutlineLevels).

حدد 0 ولن يتم عرض علامات Word المرجعية في مخطط المستند. حدد 1 وستُعرض علامات Word المرجعية في مخطط المستند عند المستوى 1؛ 2 للمستوى 2 وهكذا.

الافتراضي هو 0. النطاق الصالح هو من 0 إلى 9.

 **Examples:** 

يوضح كيفية معالجة العلامات المرجعية في رؤوس/تذييلات الصفحات في مستند نقوم بتحويله إلى PDF.

```

 Document doc = new Document(getMyDir() + "Bookmarks in headers and footers.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "PageMode" property to "PdfPageMode.UseOutlines" to display the outline navigation pane in the output PDF.
 saveOptions.setPageMode(PdfPageMode.USE_OUTLINES);

 // Set the "DefaultBookmarksOutlineLevel" property to "1" to display all
 // bookmarks at the first level of the outline in the output PDF.
 saveOptions.getOutlineOptions().setDefaultBookmarksOutlineLevel(1);

 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.None" to
 // not export any bookmarks that are inside headers/footers.
 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.First" to
 // only export bookmarks in the first section's header/footers.
 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.All" to
 // export bookmarks that are in all headers/footers.
 saveOptions.setHeaderFooterBookmarksExportMode(headerFooterBookmarksExportMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
 
```

**Returns:**
int - القيمة المقابلة  int .
### getExpandedOutlineLevels() {#getExpandedOutlineLevels}
```
public int getExpandedOutlineLevels()
```


يحدد عدد المستويات في مخطط المستند التي يتم توسيعها عند عرض الملف.

 **Remarks:** 

لاحظ أن هذه الخيارات لن تعمل عند الحفظ إلى XPS.

حدد 0 وسيتم طي مخطط المستند؛ حدد 1 وسيتم توسيع عناصر المستوى الأول في المخطط وهكذا.

الافتراضي هو 0. النطاق الصالح هو من 0 إلى 9.

 **Examples:** 

يوضح كيفية تحويل مستند كامل إلى PDF مع ثلاثة مستويات في مخطط المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings of levels 1 to 5.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);

 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);

 builder.writeln("Heading 1.2.1");
 builder.writeln("Heading 1.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);

 builder.writeln("Heading 1.2.2.1");
 builder.writeln("Heading 1.2.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_5);

 builder.writeln("Heading 1.2.2.2.1");
 builder.writeln("Heading 1.2.2.2.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
 options.getOutlineOptions().setHeadingsOutlineLevels(4);

 // If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
 // an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
 // In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
 // the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
 // In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
 // Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
 // and collapse all level and 3 and higher entries when we open the document.
 options.getOutlineOptions().setExpandedOutlineLevels(2);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
 
```

**Returns:**
int - القيمة المقابلة  int .
### getHeadingsOutlineLevels() {#getHeadingsOutlineLevels}
```
public int getHeadingsOutlineLevels()
```


يحدد عدد مستويات العناوين (الفقرات المنسقة بأنماط Heading) التي تُدرج في مخطط المستند.

 **Remarks:** 

حدد 0 لعدم وجود عناوين في المخطط؛ حدد 1 لمستوى واحد من العناوين في المخطط وهكذا.

الافتراضي هو 0. النطاق الصالح هو من 0 إلى 9.

 **Examples:** 

يوضح كيفية تحويل مستند كامل إلى PDF مع ثلاثة مستويات في مخطط المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings of levels 1 to 5.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);

 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);

 builder.writeln("Heading 1.2.1");
 builder.writeln("Heading 1.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);

 builder.writeln("Heading 1.2.2.1");
 builder.writeln("Heading 1.2.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_5);

 builder.writeln("Heading 1.2.2.2.1");
 builder.writeln("Heading 1.2.2.2.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
 options.getOutlineOptions().setHeadingsOutlineLevels(4);

 // If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
 // an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
 // In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
 // the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
 // In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
 // Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
 // and collapse all level and 3 and higher entries when we open the document.
 options.getOutlineOptions().setExpandedOutlineLevels(2);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
 
```

**Returns:**
int - القيمة المقابلة  int .
### setCreateMissingOutlineLevels(boolean value) {#setCreateMissingOutlineLevels-boolean}
```
public void setCreateMissingOutlineLevels(boolean value)
```


يحصل أو يعيّن قيمة تحدد ما إذا كان سيتم إنشاء مستويات مخطط مفقودة عند تصدير المستند أم لا.

القيمة الافتراضية لهذه الخاصية هي false .

 **Examples:** 

يوضح كيفية التعامل مع مستويات المخطط التي لا تحتوي على أي عناوين مطابقة عند حفظ مستند PDF.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings that can serve as TOC entries of levels 1 and 5.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_5);

 builder.writeln("Heading 1.1.1.1.1");
 builder.writeln("Heading 1.1.1.1.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "5" to include all headings of levels 5 and below in the outline.
 saveOptions.getOutlineOptions().setHeadingsOutlineLevels(5);

 // This document contains headings of levels 1 and 5, and no headings with levels of 2, 3, and 4.
 // The output PDF document will treat outline levels 2, 3, and 4 as "missing".
 // Set the "CreateMissingOutlineLevels" property to "true" to include all missing levels in the outline,
 // leaving blank outline entries since there are no usable headings.
 // Set the "CreateMissingOutlineLevels" property to "false" to ignore missing outline levels,
 // and treat the outline level 5 headings as level 2.
 saveOptions.getOutlineOptions().setCreateMissingOutlineLevels(createMissingOutlineLevels);

 doc.save(getArtifactsDir() + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setCreateOutlinesForHeadingsInTables(boolean value) {#setCreateOutlinesForHeadingsInTables-boolean}
```
public void setCreateOutlinesForHeadingsInTables(boolean value)
```


يحدد ما إذا كان سيتم إنشاء مخططات للعناوين (الفقرات المنسقة بأنماط Heading) داخل الجداول أم لا.

 **Remarks:** 

القيمة الافتراضية هي false .

 **Examples:** 

يوضح كيفية إنشاء إدخالات مخطط مستند PDF للعناوين داخل الجداول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a table with three rows. The first row,
 // whose text we will format in a heading-type style, will serve as the column header.
 builder.startTable();
 builder.insertCell();
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.write("Customers");
 builder.endRow();
 builder.insertCell();
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.NORMAL);
 builder.write("John Doe");
 builder.endRow();
 builder.insertCell();
 builder.write("Jane Doe");
 builder.endTable();

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "1" to get the outline
 // to only register headings with heading levels that are no larger than 1.
 pdfSaveOptions.getOutlineOptions().setHeadingsOutlineLevels(1);

 // Set the "CreateOutlinesForHeadingsInTables" property to "false" to exclude all headings within tables,
 // such as the one we have created above from the outline.
 // Set the "CreateOutlinesForHeadingsInTables" property to "true" to include all headings within tables
 // in the outline, provided that they have a heading level that is no larger than the value of the "HeadingsOutlineLevels" property.
 pdfSaveOptions.getOutlineOptions().setCreateOutlinesForHeadingsInTables(createOutlinesForHeadingsInTables);

 doc.save(getArtifactsDir() + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setDefaultBookmarksOutlineLevel(int value) {#setDefaultBookmarksOutlineLevel-int}
```
public void setDefaultBookmarksOutlineLevel(int value)
```


يحدد المستوى الافتراضي في مخطط المستند الذي يتم فيه عرض علامات Word المرجعية.

 **Remarks:** 

يمكن تحديد مستوى العلامات المرجعية الفردية باستخدام خاصية [getBookmarksOutlineLevels()](../../com.aspose.words/outlineoptions/\#getBookmarksOutlineLevels).

حدد 0 ولن يتم عرض علامات Word المرجعية في مخطط المستند. حدد 1 وستُعرض علامات Word المرجعية في مخطط المستند عند المستوى 1؛ 2 للمستوى 2 وهكذا.

الافتراضي هو 0. النطاق الصالح هو من 0 إلى 9.

 **Examples:** 

يوضح كيفية معالجة العلامات المرجعية في رؤوس/تذييلات الصفحات في مستند نقوم بتحويله إلى PDF.

```

 Document doc = new Document(getMyDir() + "Bookmarks in headers and footers.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "PageMode" property to "PdfPageMode.UseOutlines" to display the outline navigation pane in the output PDF.
 saveOptions.setPageMode(PdfPageMode.USE_OUTLINES);

 // Set the "DefaultBookmarksOutlineLevel" property to "1" to display all
 // bookmarks at the first level of the outline in the output PDF.
 saveOptions.getOutlineOptions().setDefaultBookmarksOutlineLevel(1);

 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.None" to
 // not export any bookmarks that are inside headers/footers.
 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.First" to
 // only export bookmarks in the first section's header/footers.
 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.All" to
 // export bookmarks that are in all headers/footers.
 saveOptions.setHeaderFooterBookmarksExportMode(headerFooterBookmarksExportMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | القيمة  int  المقابلة. |

### setExpandedOutlineLevels(int value) {#setExpandedOutlineLevels-int}
```
public void setExpandedOutlineLevels(int value)
```


يحدد عدد المستويات في مخطط المستند التي يتم توسيعها عند عرض الملف.

 **Remarks:** 

لاحظ أن هذه الخيارات لن تعمل عند الحفظ إلى XPS.

حدد 0 وسيتم طي مخطط المستند؛ حدد 1 وسيتم توسيع عناصر المستوى الأول في المخطط وهكذا.

الافتراضي هو 0. النطاق الصالح هو من 0 إلى 9.

 **Examples:** 

يوضح كيفية تحويل مستند كامل إلى PDF مع ثلاثة مستويات في مخطط المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings of levels 1 to 5.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);

 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);

 builder.writeln("Heading 1.2.1");
 builder.writeln("Heading 1.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);

 builder.writeln("Heading 1.2.2.1");
 builder.writeln("Heading 1.2.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_5);

 builder.writeln("Heading 1.2.2.2.1");
 builder.writeln("Heading 1.2.2.2.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
 options.getOutlineOptions().setHeadingsOutlineLevels(4);

 // If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
 // an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
 // In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
 // the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
 // In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
 // Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
 // and collapse all level and 3 and higher entries when we open the document.
 options.getOutlineOptions().setExpandedOutlineLevels(2);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | القيمة  int  المقابلة. |

### setHeadingsOutlineLevels(int value) {#setHeadingsOutlineLevels-int}
```
public void setHeadingsOutlineLevels(int value)
```


يحدد عدد مستويات العناوين (الفقرات المنسقة بأنماط Heading) التي تُدرج في مخطط المستند.

 **Remarks:** 

حدد 0 لعدم وجود عناوين في المخطط؛ حدد 1 لمستوى واحد من العناوين في المخطط وهكذا.

الافتراضي هو 0. النطاق الصالح هو من 0 إلى 9.

 **Examples:** 

يوضح كيفية تحويل مستند كامل إلى PDF مع ثلاثة مستويات في مخطط المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings of levels 1 to 5.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);

 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);

 builder.writeln("Heading 1.2.1");
 builder.writeln("Heading 1.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);

 builder.writeln("Heading 1.2.2.1");
 builder.writeln("Heading 1.2.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_5);

 builder.writeln("Heading 1.2.2.2.1");
 builder.writeln("Heading 1.2.2.2.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
 options.getOutlineOptions().setHeadingsOutlineLevels(4);

 // If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
 // an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
 // In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
 // the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
 // In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
 // Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
 // and collapse all level and 3 and higher entries when we open the document.
 options.getOutlineOptions().setExpandedOutlineLevels(2);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | القيمة  int  المقابلة. |

