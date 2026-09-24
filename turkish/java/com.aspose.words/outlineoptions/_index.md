---
title: "OutlineOptions"
linktitle: "OutlineOptions"
second_title: "Aspose.Words Java için"
description: "Java'da anahat seçeneklerini belirtmeye izin verir."
type: docs
weight: 509
url: /tr/java/com.aspose.words/outlineoptions/
---

**Inheritance:**
java.lang.Object
```
public class OutlineOptions
```

Taslak seçeneklerini belirtmeye olanak tanır.

Daha fazla bilgi edinmek için [ Save a Document ][Save a Document] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

PDF'ye render ettiğimiz bir belgede üstbilgi/altbilgi yer imlerini nasıl işleyeceğimizi gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getBookmarksOutlineLevels()](#getBookmarksOutlineLevels) | Bireysel yer imleri anahat seviyesini belirtmeye izin verir. |
| [getCreateMissingOutlineLevels()](#getCreateMissingOutlineLevels) | Belge dışa aktarıldığında eksik anahat seviyelerinin oluşturulup oluşturulmayacağını belirleyen bir değeri alır veya ayarlar. |
| [getCreateOutlinesForHeadingsInTables()](#getCreateOutlinesForHeadingsInTables) | Tablolar içindeki başlıklar (Başlık stilleriyle biçimlendirilmiş paragraflar) için anahatların oluşturulup oluşturulmayacağını belirtir. |
| [getDefaultBookmarksOutlineLevel()](#getDefaultBookmarksOutlineLevel) | Word yer imlerinin gösterileceği belge anahattındaki varsayılan seviyeyi belirtir. |
| [getExpandedOutlineLevels()](#getExpandedOutlineLevels) | Dosya görüntülendiğinde belge anahattında kaç seviyenin genişletilmiş gösterileceğini belirtir. |
| [getHeadingsOutlineLevels()](#getHeadingsOutlineLevels) | Belge anahattına dahil edilecek başlık seviyelerinin (Başlık stilleriyle biçimlendirilmiş paragraflar) sayısını belirtir. |
| [setCreateMissingOutlineLevels(boolean value)](#setCreateMissingOutlineLevels-boolean) | Belge dışa aktarıldığında eksik anahat seviyelerinin oluşturulup oluşturulmayacağını belirleyen bir değeri alır veya ayarlar. |
| [setCreateOutlinesForHeadingsInTables(boolean value)](#setCreateOutlinesForHeadingsInTables-boolean) | Tablolar içindeki başlıklar (Başlık stilleriyle biçimlendirilmiş paragraflar) için anahatların oluşturulup oluşturulmayacağını belirtir. |
| [setDefaultBookmarksOutlineLevel(int value)](#setDefaultBookmarksOutlineLevel-int) | Word yer imlerinin gösterileceği belge anahattındaki varsayılan seviyeyi belirtir. |
| [setExpandedOutlineLevels(int value)](#setExpandedOutlineLevels-int) | Dosya görüntülendiğinde belge anahattında kaç seviyenin genişletilmiş gösterileceğini belirtir. |
| [setHeadingsOutlineLevels(int value)](#setHeadingsOutlineLevels-int) | Belge anahattına dahil edilecek başlık seviyelerinin (Başlık stilleriyle biçimlendirilmiş paragraflar) sayısını belirtir. |
### getBookmarksOutlineLevels() {#getBookmarksOutlineLevels}
```
public BookmarksOutlineLevelCollection getBookmarksOutlineLevels()
```


Bireysel yer imleri anahat seviyesini belirtmeye izin verir.

 **Remarks:** 

Bu koleksiyonda yer imi seviyesi belirtilmemişse, [getDefaultBookmarksOutlineLevel()](../../com.aspose.words/outlineoptions/\#getDefaultBookmarksOutlineLevel) / [setDefaultBookmarksOutlineLevel(int)](../../com.aspose.words/outlineoptions/\#setDefaultBookmarksOutlineLevel-int) değeri kullanılır.

 **Examples:** 

Yer imleri için taslak seviyelerinin nasıl ayarlanacağını gösterir.

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


Belge dışa aktarıldığında eksik anahat seviyelerinin oluşturulup oluşturulmayacağını belirleyen bir değeri alır veya ayarlar.

Bu özelliğin varsayılan değeri false'dur.

 **Examples:** 

PDF belgesi kaydedilirken karşılık gelen başlıkları olmayan anahat seviyeleriyle nasıl çalışılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getCreateOutlinesForHeadingsInTables() {#getCreateOutlinesForHeadingsInTables}
```
public boolean getCreateOutlinesForHeadingsInTables()
```


Tablolar içindeki başlıklar (Başlık stilleriyle biçimlendirilmiş paragraflar) için anahatların oluşturulup oluşturulmayacağını belirtir.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Tablolar içindeki başlıklar için PDF belge anahat girişlerinin nasıl oluşturulacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getDefaultBookmarksOutlineLevel() {#getDefaultBookmarksOutlineLevel}
```
public int getDefaultBookmarksOutlineLevel()
```


Word yer imlerinin gösterileceği belge anahattındaki varsayılan seviyeyi belirtir.

 **Remarks:** 

Bireysel yer imi seviyesi, [getBookmarksOutlineLevels()](../../com.aspose.words/outlineoptions/\#getBookmarksOutlineLevels) özelliği kullanılarak belirtilebilir.

0 belirtirseniz Word yer imleri belge anahattında gösterilmez. 1 belirtirseniz Word yer imleri anahattın 1. seviyesinde gösterilir; 2 için 2. seviye vb.

Varsayılan 0'dır. Geçerli aralık 0 ile 9 arasındadır.

 **Examples:** 

PDF'ye render ettiğimiz bir belgede üstbilgi/altbilgi yer imlerini nasıl işleyeceğimizi gösterir.

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
int - İlgili  int  değeri.
### getExpandedOutlineLevels() {#getExpandedOutlineLevels}
```
public int getExpandedOutlineLevels()
```


Dosya görüntülendiğinde belge anahattında kaç seviyenin genişletilmiş gösterileceğini belirtir.

 **Remarks:** 

Bu seçeneğin XPS olarak kaydedildiğinde çalışmayacağını unutmayın.

0'ı belirtin ve belge taslağı daraltılacaktır; 1'i belirtin ve taslaktaki birinci seviye öğeler genişletilecektir ve bu şekilde devam eder.

Varsayılan 0'dır. Geçerli aralık 0 ile 9 arasındadır.

 **Examples:** 

Belge taslağında üç seviye ile bir bütün belgeyi PDF'ye dönüştürmenin nasıl yapılacağını gösterir.

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
int - İlgili  int  değeri.
### getHeadingsOutlineLevels() {#getHeadingsOutlineLevels}
```
public int getHeadingsOutlineLevels()
```


Belge anahattına dahil edilecek başlık seviyelerinin (Başlık stilleriyle biçimlendirilmiş paragraflar) sayısını belirtir.

 **Remarks:** 

Taslakta başlık olmaması için 0'ı belirtin; taslakta bir seviye başlık için 1'i belirtin ve bu şekilde devam eder.

Varsayılan 0'dır. Geçerli aralık 0 ile 9 arasındadır.

 **Examples:** 

Belge taslağında üç seviye ile bir bütün belgeyi PDF'ye dönüştürmenin nasıl yapılacağını gösterir.

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
int - İlgili  int  değeri.
### setCreateMissingOutlineLevels(boolean value) {#setCreateMissingOutlineLevels-boolean}
```
public void setCreateMissingOutlineLevels(boolean value)
```


Belge dışa aktarıldığında eksik anahat seviyelerinin oluşturulup oluşturulmayacağını belirleyen bir değeri alır veya ayarlar.

Bu özelliğin varsayılan değeri false'dur.

 **Examples:** 

PDF belgesi kaydedilirken karşılık gelen başlıkları olmayan anahat seviyeleriyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setCreateOutlinesForHeadingsInTables(boolean value) {#setCreateOutlinesForHeadingsInTables-boolean}
```
public void setCreateOutlinesForHeadingsInTables(boolean value)
```


Tablolar içindeki başlıklar (Başlık stilleriyle biçimlendirilmiş paragraflar) için anahatların oluşturulup oluşturulmayacağını belirtir.

 **Remarks:** 

Varsayılan değer  false  dır.

 **Examples:** 

Tablolar içindeki başlıklar için PDF belge anahat girişlerinin nasıl oluşturulacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setDefaultBookmarksOutlineLevel(int value) {#setDefaultBookmarksOutlineLevel-int}
```
public void setDefaultBookmarksOutlineLevel(int value)
```


Word yer imlerinin gösterileceği belge anahattındaki varsayılan seviyeyi belirtir.

 **Remarks:** 

Bireysel yer imi seviyesi, [getBookmarksOutlineLevels()](../../com.aspose.words/outlineoptions/\#getBookmarksOutlineLevels) özelliği kullanılarak belirtilebilir.

0 belirtirseniz Word yer imleri belge anahattında gösterilmez. 1 belirtirseniz Word yer imleri anahattın 1. seviyesinde gösterilir; 2 için 2. seviye vb.

Varsayılan 0'dır. Geçerli aralık 0 ile 9 arasındadır.

 **Examples:** 

PDF'ye render ettiğimiz bir belgede üstbilgi/altbilgi yer imlerini nasıl işleyeceğimizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İlgili  int  değeri. |

### setExpandedOutlineLevels(int value) {#setExpandedOutlineLevels-int}
```
public void setExpandedOutlineLevels(int value)
```


Dosya görüntülendiğinde belge anahattında kaç seviyenin genişletilmiş gösterileceğini belirtir.

 **Remarks:** 

Bu seçeneğin XPS olarak kaydedildiğinde çalışmayacağını unutmayın.

0'ı belirtin ve belge taslağı daraltılacaktır; 1'i belirtin ve taslaktaki birinci seviye öğeler genişletilecektir ve bu şekilde devam eder.

Varsayılan 0'dır. Geçerli aralık 0 ile 9 arasındadır.

 **Examples:** 

Belge taslağında üç seviye ile bir bütün belgeyi PDF'ye dönüştürmenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İlgili  int  değeri. |

### setHeadingsOutlineLevels(int value) {#setHeadingsOutlineLevels-int}
```
public void setHeadingsOutlineLevels(int value)
```


Belge anahattına dahil edilecek başlık seviyelerinin (Başlık stilleriyle biçimlendirilmiş paragraflar) sayısını belirtir.

 **Remarks:** 

Taslakta başlık olmaması için 0'ı belirtin; taslakta bir seviye başlık için 1'i belirtin ve bu şekilde devam eder.

Varsayılan 0'dır. Geçerli aralık 0 ile 9 arasındadır.

 **Examples:** 

Belge taslağında üç seviye ile bir bütün belgeyi PDF'ye dönüştürmenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İlgili  int  değeri. |

