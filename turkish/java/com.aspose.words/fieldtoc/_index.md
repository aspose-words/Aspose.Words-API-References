---
title: "FieldToc"
linktitle: "FieldToc"
second_title: "Aspose.Words Java için"
description: "Java'da TOC alanını uygular."
type: docs
weight: 298
url: /tr/java/com.aspose.words/fieldtoc/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldToc extends Field
```

TOC alanını uygular.

Daha fazla bilgi için, [ Working with Fields ][Working with Fields] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

TC alanları tarafından belirtilen girişleri, başlık seviyelerini ve belirtilen stilleri kullanarak bir içindekiler tablosu (aynı zamanda şekil tablosu da olabilir) oluşturur ve bu tabloyu belgenin bu konumuna ekler.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

SEQ alanlarını kullanarak bir TOC alanını girişlerle doldurmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getBookmarkName()](#getBookmarkName) | Tabloyu oluşturmak için kullanılan belgenin bölümünü işaretleyen yer iminin adını alır. |
| [getCaptionlessTableOfFiguresLabel()](#getCaptionlessTableOfFiguresLabel) | Altyazının etiketi ve numarası dahil olmayan bir şekil tablosu oluştururken kullanılan sıra tanımlayıcısının adını alır. |
| [getCustomStyles()](#getCustomStyles) | İçindekiler tablosuna dahil edilecek, yerleşik başlık stilleri dışındaki stillerin bir listesini alır. |
| [getDisplayResult()](#getDisplayResult) | Görüntülenen alan sonucunu temsil eden metni alır. |
| [getEnd()](#getEnd) | Alan sonunu temsil eden düğümü alır. |
| [getEntryIdentifier()](#getEntryIdentifier) | Dahil edilen TC alanlarının tip tanımlayıcılarıyla eşleşmesi gereken bir dize alır. |
| [getEntryLevelRange()](#getEntryLevelRange) | İçindekiler tablosu girişlerinin dahil edilecek seviye aralığını alır. |
| [getEntrySeparator()](#getEntrySeparator) | Bir giriş ile sayfa numarasını ayıran karakter dizisini alır. |
| [getFieldCode()](#getFieldCode) | Alan başlangıcı ile alan ayırıcı arasındaki metni (veya ayırıcı yoksa alan sonunu) döndürür. |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Alan başlangıcı ile alan ayırıcı arasındaki metni (veya ayırıcı yoksa alan sonunu) döndürür. |
| [getFormat()](#getFormat) | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../../com.aspose.words/fieldformat/) nesnesi alır. |
| [getHeadingLevelRange()](#getHeadingLevelRange) | Dahil edilecek başlık seviyelerinin aralığını alır. |
| [getHideInWebLayout()](#getHideInWebLayout) | Web düzeni görünümünde sekme lideri ve sayfa numaralarının gizlenip gizlenmeyeceğini alır. |
| [getInsertHyperlinks()](#getInsertHyperlinks) | İçindekiler tablosu girişlerinin hiperlink olup olmayacağını alır. |
| [getLocaleId()](#getLocaleId) | Alanının LCID'sini alır. |
| [getPageNumberOmittingLevelRange()](#getPageNumberOmittingLevelRange) | Sayfa numaralarının atlanacağı içindekiler tablosu girişlerinin seviye aralığını alır. |
| [getPrefixedSequenceIdentifier()](#getPrefixedSequenceIdentifier) | Girişin sayfa numarasına bir önek eklenmesi gereken dizinin tanımlayıcısını alır. |
| [getPreserveLineBreaks()](#getPreserveLineBreaks) | Tablo girişleri içinde yeni satır karakterlerinin korunup korunmayacağını alır. |
| [getPreserveTabs()](#getPreserveTabs) | Tablo girişleri içinde sekme girişlerinin korunup korunmayacağını alır. |
| [getResult()](#getResult) | Alan ayırıcı ile alan sonu arasındaki metni alır. |
| [getSeparator()](#getSeparator) | Alan ayırıcıyı temsil eden düğümü alır. |
| [getSequenceSeparator()](#getSequenceSeparator) | Dizi numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter dizisini alır. |
| [getStart()](#getStart) | Alan başlangıcını temsil eden düğümü alır. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getTableOfFiguresLabel()](#getTableOfFiguresLabel) | Şekil tablosu oluşturulurken kullanılan dizi tanımlayıcısının adını alır. |
| [getType()](#getType) | Microsoft Word alan türünü alır. |
| [getUseParagraphOutlineLevel()](#getUseParagraphOutlineLevel) | Uygulanan paragraf taslak seviyesinin kullanılıp kullanılmayacağını alır. |
| [isDirty()](#isDirty) | Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını alır. |
| [isDirty(boolean value)](#isDirty-boolean) | Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını ayarlar. |
| [isLocked()](#isLocked) | Alan kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır. |
| [isLocked(boolean value)](#isLocked-boolean) | Alan kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) ayarlar. |
| [remove()](#remove) | Alanı belgeden kaldırır. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String) | Tabloyu oluşturmak için kullanılan belgenin bölümünü işaretleyen yer iminin adını ayarlar. |
| [setCaptionlessTableOfFiguresLabel(String value)](#setCaptionlessTableOfFiguresLabel-java.lang.String) | Altyazının etiketi ve numarasını içermeyen bir şekil tablosu oluşturulurken kullanılan dizi tanımlayıcısının adını ayarlar. |
| [setCustomStyles(String value)](#setCustomStyles-java.lang.String) | İçindekiler tablosuna dahil edilecek, yerleşik başlık stilleri dışındaki stillerin bir listesini ayarlar. |
| [setEntryIdentifier(String value)](#setEntryIdentifier-java.lang.String) | Dahil edilen TC alanlarının tip tanımlayıcılarıyla eşleşmesi gereken bir dizeyi ayarlar. |
| [setEntryLevelRange(String value)](#setEntryLevelRange-java.lang.String) | İçindekiler tablosu girişlerinin dahil edilecek seviye aralığını ayarlar. |
| [setEntrySeparator(String value)](#setEntrySeparator-java.lang.String) | Bir giriş ile sayfa numarasını ayıran karakter dizisini ayarlar. |
| [setHeadingLevelRange(String value)](#setHeadingLevelRange-java.lang.String) | Dahil edilecek başlık seviyelerinin aralığını ayarlar. |
| [setHideInWebLayout(boolean value)](#setHideInWebLayout-boolean) | Web düzeni görünümünde sekme lideri ve sayfa numaralarının gizlenip gizlenmeyeceğini ayarlar. |
| [setInsertHyperlinks(boolean value)](#setInsertHyperlinks-boolean) | İçindekiler tablosu girişlerinin hiperlink olup olmayacağını ayarlar. |
| [setLocaleId(int value)](#setLocaleId-int) | Alanının LCID'sini ayarlar. |
| [setPageNumberOmittingLevelRange(String value)](#setPageNumberOmittingLevelRange-java.lang.String) | Sayfa numaralarının atlanacağı içindekiler tablosu girişlerinin seviye aralığını ayarlar. |
| [setPrefixedSequenceIdentifier(String value)](#setPrefixedSequenceIdentifier-java.lang.String) | Girişin sayfa numarasına bir önek eklenmesi gereken dizinin tanımlayıcısını ayarlar. |
| [setPreserveLineBreaks(boolean value)](#setPreserveLineBreaks-boolean) | Tablo girişleri içinde yeni satır karakterlerinin korunup korunmayacağını ayarlar. |
| [setPreserveTabs(boolean value)](#setPreserveTabs-boolean) | Tablo girişleri içinde sekme girişlerinin korunup korunmayacağını ayarlar. |
| [setResult(String value)](#setResult-java.lang.String) | Alan ayırıcı ile alan sonu arasındaki metni ayarlar. |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String) | Dizi numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter dizisini ayarlar. |
| [setTableOfFiguresLabel(String value)](#setTableOfFiguresLabel-java.lang.String) | Şekil tablosu oluşturulurken kullanılan dizi tanımlayıcısının adını ayarlar. |
| [setUseParagraphOutlineLevel(boolean value)](#setUseParagraphOutlineLevel-boolean) | Uygulanan paragraf taslak seviyesinin kullanılıp kullanılmayacağını ayarlar. |
| [unlink()](#unlink) | Alan bağlantısını kaldırır. |
| [update()](#update) | Alan güncellemesini gerçekleştirir. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Bir alan güncellemesi gerçekleştirir. |
| [updatePageNumbers()](#updatePageNumbers) | Bu içindekiler tablosundaki öğeler için sayfa numaralarını günceller. |
### getBookmarkName() {#getBookmarkName}
```
public String getBookmarkName()
```


Tabloyu oluşturmak için kullanılan belgenin bölümünü işaretleyen yer iminin adını alır.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
java.lang.String - Tabloyu oluşturmak için kullanılan belgenin bölümünü işaretleyen yer iminin adı.
### getCaptionlessTableOfFiguresLabel() {#getCaptionlessTableOfFiguresLabel}
```
public String getCaptionlessTableOfFiguresLabel()
```


Altyazının etiketi ve numarası dahil olmayan bir şekil tablosu oluştururken kullanılan sıra tanımlayıcısının adını alır.

 **Examples:** 

Dizi tanımlayıcısının adının nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldToc fieldToc = (FieldToc)builder.insertField(FieldType.FIELD_TOC, true);
 fieldToc.setCaptionlessTableOfFiguresLabel("Test");

 Assert.assertEquals(" TOC  \\a Test", fieldToc.getFieldCode());
 
```

**Returns:**
java.lang.String - Başlık etiketini ve numarasını içermeyen bir şekil tablosu oluşturulurken kullanılan dizi tanımlayıcısının adı.
### getCustomStyles() {#getCustomStyles}
```
public String getCustomStyles()
```


İçindekiler tablosuna dahil edilecek, yerleşik başlık stilleri dışındaki stillerin bir listesini alır.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
java.lang.String - İçindekiler tablosuna dahil edilecek yerleşik başlık stilleri dışındaki stil listesi.
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


Görüntülenen alan sonucunu temsil eden metni alır.

 **Remarks:** 

Doğru değer elde etmek için [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) yöntemi, [FieldListNum](../../com.aspose.words/fieldlistnum/), [FieldAutoNum](../../com.aspose.words/fieldautonum/), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout/) ve [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl/) alanları için çağrılmalıdır.

 **Examples:** 

Bir alanın belgede gösterdiği gerçek metni nasıl alacağınızı gösterir.

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
java.lang.String - Görüntülenen alan sonucunu temsil eden metin.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Alan sonunu temsil eden düğümü alır.

 **Examples:** 

Alan koleksiyonu ile nasıl çalışılacağını gösterir.

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
### getEntryIdentifier() {#getEntryIdentifier}
```
public String getEntryIdentifier()
```


Dahil edilen TC alanlarının tip tanımlayıcılarıyla eşleşmesi gereken bir dize alır.

 **Examples:** 

Bir TOC alanı eklemenin ve hangi TC alanlarının giriş olarak sonlanacağını filtrelemenin nasıl yapılacağını gösterir.

```

 public void fieldTocEntryIdentifier() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOC field, which will compile all TC fields into a table of contents.
     FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Configure the field only to pick up TC entries of the "A" type, and an entry-level between 1 and 3.
     fieldToc.setEntryIdentifier("A");
     fieldToc.setEntryLevelRange("1-3");

     Assert.assertEquals(" TOC  \\f A \\l 1-3", fieldToc.getFieldCode());

     // These two entries will appear in the table.
     builder.insertBreak(BreakType.PAGE_BREAK);
     insertTocEntry(builder, "TC field 1", "A", "1");
     insertTocEntry(builder, "TC field 2", "A", "2");

     Assert.assertEquals(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.getRange().getFields().get(1).getFieldCode());

     // This entry will be omitted from the table because it has a different type from "A".
     insertTocEntry(builder, "TC field 3", "B", "1");

     // This entry will be omitted from the table because it has an entry-level outside of the 1-3 range.
     insertTocEntry(builder, "TC field 4", "A", "5");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TC.docx");
 }

 /// 
 /// Use a document builder to insert a TC field.
 /// 
 public void insertTocEntry(final DocumentBuilder builder, final String text, final String typeIdentifier, final String entryLevel) throws Exception {
     FieldTC fieldTc = (FieldTC) builder.insertField(FieldType.FIELD_TOC_ENTRY, true);
     fieldTc.setOmitPageNumber(true);
     fieldTc.setText(text);
     fieldTc.setTypeIdentifier(typeIdentifier);
     fieldTc.setEntryLevel(entryLevel);
 }
 
```

**Returns:**
java.lang.String - Dahil edilen TC alanlarının tür tanımlayıcılarıyla eşleşmesi gereken bir dize.
### getEntryLevelRange() {#getEntryLevelRange}
```
public String getEntryLevelRange()
```


İçindekiler tablosu girişlerinin dahil edilecek seviye aralığını alır.

 **Examples:** 

Bir TOC alanı eklemenin ve hangi TC alanlarının giriş olarak sonlanacağını filtrelemenin nasıl yapılacağını gösterir.

```

 public void fieldTocEntryIdentifier() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOC field, which will compile all TC fields into a table of contents.
     FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Configure the field only to pick up TC entries of the "A" type, and an entry-level between 1 and 3.
     fieldToc.setEntryIdentifier("A");
     fieldToc.setEntryLevelRange("1-3");

     Assert.assertEquals(" TOC  \\f A \\l 1-3", fieldToc.getFieldCode());

     // These two entries will appear in the table.
     builder.insertBreak(BreakType.PAGE_BREAK);
     insertTocEntry(builder, "TC field 1", "A", "1");
     insertTocEntry(builder, "TC field 2", "A", "2");

     Assert.assertEquals(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.getRange().getFields().get(1).getFieldCode());

     // This entry will be omitted from the table because it has a different type from "A".
     insertTocEntry(builder, "TC field 3", "B", "1");

     // This entry will be omitted from the table because it has an entry-level outside of the 1-3 range.
     insertTocEntry(builder, "TC field 4", "A", "5");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TC.docx");
 }

 /// 
 /// Use a document builder to insert a TC field.
 /// 
 public void insertTocEntry(final DocumentBuilder builder, final String text, final String typeIdentifier, final String entryLevel) throws Exception {
     FieldTC fieldTc = (FieldTC) builder.insertField(FieldType.FIELD_TOC_ENTRY, true);
     fieldTc.setOmitPageNumber(true);
     fieldTc.setText(text);
     fieldTc.setTypeIdentifier(typeIdentifier);
     fieldTc.setEntryLevel(entryLevel);
 }
 
```

**Returns:**
java.lang.String - İçindekiler tablosu girişlerinin dahil edileceği seviye aralığı.
### getEntrySeparator() {#getEntrySeparator}
```
public String getEntrySeparator()
```


Bir giriş ile sayfa numarasını ayıran karakter dizisini alır.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
java.lang.String - Bir giriş ile sayfa numarasını ayıran karakter dizisi.
### getFieldCode() {#getFieldCode}
```
public String getFieldCode()
```


Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların sonuçları dahil edilir.

 **Examples:** 

Alan kodu kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Bir alanın alan kodunu nasıl alacağınızı gösterir.

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


Alan başlangıcı ile alan ayırıcı arasındaki metni (veya ayırıcı yoksa alan sonunu) döndürür.

 **Examples:** 

Bir alanın alan kodunu nasıl alacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| includeChildFieldCodes | boolean | true  eğer alt alan kodları dahil edilmeliyse. |

**Returns:**
java.lang.String
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../../com.aspose.words/fieldformat/) nesnesi alır.

 **Examples:** 

Alan sonuçlarını nasıl biçimlendireceğinizi gösterir.

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
### getHeadingLevelRange() {#getHeadingLevelRange}
```
public String getHeadingLevelRange()
```


Dahil edilecek başlık seviyelerinin aralığını alır.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
java.lang.String - Dahil edilecek başlık seviyeleri aralığı.
### getHideInWebLayout() {#getHideInWebLayout}
```
public boolean getHideInWebLayout()
```


Web düzeni görünümünde sekme lideri ve sayfa numaralarının gizlenip gizlenmeyeceğini alır.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
boolean - Web düzen görünümünde sekme lideri ve sayfa numaralarının gizlenip gizlenmeyeceği.
### getInsertHyperlinks() {#getInsertHyperlinks}
```
public boolean getInsertHyperlinks()
```


İçindekiler tablosu girişlerinin hiperlink olup olmayacağını alır.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
boolean - İçindekiler tablosu girişlerinin bağlantı (hyperlink) olup olmayacağı.
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Alanının LCID'sini alır.

 **Examples:** 

Bir alanı nasıl ekleyeceğinizi ve yerel ayarıyla nasıl çalışacağınızı gösterir.

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
int - Alanın LCID'si.
### getPageNumberOmittingLevelRange() {#getPageNumberOmittingLevelRange}
```
public String getPageNumberOmittingLevelRange()
```


Sayfa numaralarının atlanacağı içindekiler tablosu girişlerinin seviye aralığını alır.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
java.lang.String - İçindekiler tablosu girişlerinin sayfa numaralarının atlanacağı seviye aralığı.
### getPrefixedSequenceIdentifier() {#getPrefixedSequenceIdentifier}
```
public String getPrefixedSequenceIdentifier()
```


Girişin sayfa numarasına bir önek eklenmesi gereken dizinin tanımlayıcısını alır.

 **Examples:** 

SEQ alanlarını kullanarak bir TOC alanını girişlerle doldurmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```

**Returns:**
java.lang.String - Girişin sayfa numarasına bir önek eklenmesi gereken dizi tanımlayıcısı.
### getPreserveLineBreaks() {#getPreserveLineBreaks}
```
public boolean getPreserveLineBreaks()
```


Tablo girişleri içinde yeni satır karakterlerinin korunup korunmayacağını alır.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
boolean - Tablo girişleri içinde yeni satır karakterlerinin korunup korunmayacağı.
### getPreserveTabs() {#getPreserveTabs}
```
public boolean getPreserveTabs()
```


Tablo girişleri içinde sekme girişlerinin korunup korunmayacağını alır.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
boolean - Tablo girişleri içinde sekme girişlerinin korunup korunmayacağı.
### getResult() {#getResult}
```
public String getResult()
```


Alan ayırıcı ile alan sonu arasındaki metni alır.

 **Examples:** 

Alan kodu kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
java.lang.String - Alan ayırıcı ile alan sonu arasındaki metin.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Alan ayırıcıyı temsil eden düğümü alır. Null olabilir.

 **Examples:** 

Alan koleksiyonu ile nasıl çalışılacağını gösterir.

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
### getSequenceSeparator() {#getSequenceSeparator}
```
public String getSequenceSeparator()
```


Dizi numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter dizisini alır.

 **Examples:** 

SEQ alanlarını kullanarak bir TOC alanını girişlerle doldurmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```

**Returns:**
java.lang.String - Dizi numaraları ile sayfa numaralarını ayırmak için kullanılan karakter dizisi.
### getStart() {#getStart}
```
public FieldStart getStart()
```


Alan başlangıcını temsil eden düğümü alır.

 **Examples:** 

Alan koleksiyonu ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getTableOfFiguresLabel() {#getTableOfFiguresLabel}
```
public String getTableOfFiguresLabel()
```


Şekil tablosu oluşturulurken kullanılan dizi tanımlayıcısının adını alır.

 **Examples:** 

SEQ alanlarını kullanarak bir TOC alanını girişlerle doldurmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```

**Returns:**
java.lang.String - Şekil tablosu oluşturulurken kullanılan dizi tanımlayıcısının adı.
### getType() {#getType}
```
public int getType()
```


Microsoft Word alan türünü alır.

 **Examples:** 

Alan kodu kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
int - Microsoft Word alan türü. Döndürülen değer, [FieldType](../../com.aspose.words/fieldtype/) sabitlerinden biridir.
### getUseParagraphOutlineLevel() {#getUseParagraphOutlineLevel}
```
public boolean getUseParagraphOutlineLevel()
```


Uygulanan paragraf taslak seviyesinin kullanılıp kullanılmayacağını alır.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
boolean - Uygulanan paragraf taslak seviyesinin kullanılıp kullanılmayacağı.
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını alır.

 **Examples:** 

Alan sonucunu güncellemek için özel özelliğin nasıl kullanılacağını gösterir.

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
boolean - Alanın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru olmaması (eski) olup olmadığı.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını ayarlar.

 **Examples:** 

Alan sonucunu güncellemek için özel özelliğin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Alanın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru olmaması (eski) olup olmadığı. |

### isLocked() {#isLocked}
```
public boolean isLocked()
```


Alan kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır.

 **Examples:** 

Bir FieldStart düğümüyle nasıl çalışılacağını gösterir.

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
boolean - Alanın kilitli olup olmadığı (sonucunu yeniden hesaplamamalı).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Alan kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) ayarlar.

 **Examples:** 

Bir FieldStart düğümüyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Alanın kilitli olup olmadığı (sonucunu yeniden hesaplamamalı). |

### remove() {#remove}
```
public Node remove()
```


Alanı belgeden kaldırır. Alanın hemen sonrasında bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafı döndürür. Alan zaten kaldırılmışsa, null döndürür.

 **Examples:** 

Bir alan koleksiyonundan alanların nasıl kaldırılacağını gösterir.

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

PRIVATE alanların nasıl işleneceğini gösterir.

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


Tabloyu oluşturmak için kullanılan belgenin bölümünü işaretleyen yer iminin adını ayarlar.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Tablonun oluşturulması için kullanılan belge bölümünü işaretleyen yer iminin adı. |

### setCaptionlessTableOfFiguresLabel(String value) {#setCaptionlessTableOfFiguresLabel-java.lang.String}
```
public void setCaptionlessTableOfFiguresLabel(String value)
```


Altyazının etiketi ve numarasını içermeyen bir şekil tablosu oluşturulurken kullanılan dizi tanımlayıcısının adını ayarlar.

 **Examples:** 

Dizi tanımlayıcısının adının nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldToc fieldToc = (FieldToc)builder.insertField(FieldType.FIELD_TOC, true);
 fieldToc.setCaptionlessTableOfFiguresLabel("Test");

 Assert.assertEquals(" TOC  \\a Test", fieldToc.getFieldCode());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Başlık etiketini ve numarasını içermeyen bir şekil tablosu oluşturulurken kullanılan dizi tanımlayıcısının adı. |

### setCustomStyles(String value) {#setCustomStyles-java.lang.String}
```
public void setCustomStyles(String value)
```


İçindekiler tablosuna dahil edilecek, yerleşik başlık stilleri dışındaki stillerin bir listesini ayarlar.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İçindekiler tablosuna dahil edilecek yerleşik başlık stilleri dışındaki stil listesi. |

### setEntryIdentifier(String value) {#setEntryIdentifier-java.lang.String}
```
public void setEntryIdentifier(String value)
```


Dahil edilen TC alanlarının tip tanımlayıcılarıyla eşleşmesi gereken bir dizeyi ayarlar.

 **Examples:** 

Bir TOC alanı eklemenin ve hangi TC alanlarının giriş olarak sonlanacağını filtrelemenin nasıl yapılacağını gösterir.

```

 public void fieldTocEntryIdentifier() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOC field, which will compile all TC fields into a table of contents.
     FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Configure the field only to pick up TC entries of the "A" type, and an entry-level between 1 and 3.
     fieldToc.setEntryIdentifier("A");
     fieldToc.setEntryLevelRange("1-3");

     Assert.assertEquals(" TOC  \\f A \\l 1-3", fieldToc.getFieldCode());

     // These two entries will appear in the table.
     builder.insertBreak(BreakType.PAGE_BREAK);
     insertTocEntry(builder, "TC field 1", "A", "1");
     insertTocEntry(builder, "TC field 2", "A", "2");

     Assert.assertEquals(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.getRange().getFields().get(1).getFieldCode());

     // This entry will be omitted from the table because it has a different type from "A".
     insertTocEntry(builder, "TC field 3", "B", "1");

     // This entry will be omitted from the table because it has an entry-level outside of the 1-3 range.
     insertTocEntry(builder, "TC field 4", "A", "5");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TC.docx");
 }

 /// 
 /// Use a document builder to insert a TC field.
 /// 
 public void insertTocEntry(final DocumentBuilder builder, final String text, final String typeIdentifier, final String entryLevel) throws Exception {
     FieldTC fieldTc = (FieldTC) builder.insertField(FieldType.FIELD_TOC_ENTRY, true);
     fieldTc.setOmitPageNumber(true);
     fieldTc.setText(text);
     fieldTc.setTypeIdentifier(typeIdentifier);
     fieldTc.setEntryLevel(entryLevel);
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Dahil edilen TC alanlarının tür tanımlayıcılarıyla eşleşmesi gereken bir dize. |

### setEntryLevelRange(String value) {#setEntryLevelRange-java.lang.String}
```
public void setEntryLevelRange(String value)
```


İçindekiler tablosu girişlerinin dahil edilecek seviye aralığını ayarlar.

 **Examples:** 

Bir TOC alanı eklemenin ve hangi TC alanlarının giriş olarak sonlanacağını filtrelemenin nasıl yapılacağını gösterir.

```

 public void fieldTocEntryIdentifier() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Insert a TOC field, which will compile all TC fields into a table of contents.
     FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Configure the field only to pick up TC entries of the "A" type, and an entry-level between 1 and 3.
     fieldToc.setEntryIdentifier("A");
     fieldToc.setEntryLevelRange("1-3");

     Assert.assertEquals(" TOC  \\f A \\l 1-3", fieldToc.getFieldCode());

     // These two entries will appear in the table.
     builder.insertBreak(BreakType.PAGE_BREAK);
     insertTocEntry(builder, "TC field 1", "A", "1");
     insertTocEntry(builder, "TC field 2", "A", "2");

     Assert.assertEquals(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.getRange().getFields().get(1).getFieldCode());

     // This entry will be omitted from the table because it has a different type from "A".
     insertTocEntry(builder, "TC field 3", "B", "1");

     // This entry will be omitted from the table because it has an entry-level outside of the 1-3 range.
     insertTocEntry(builder, "TC field 4", "A", "5");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TC.docx");
 }

 /// 
 /// Use a document builder to insert a TC field.
 /// 
 public void insertTocEntry(final DocumentBuilder builder, final String text, final String typeIdentifier, final String entryLevel) throws Exception {
     FieldTC fieldTc = (FieldTC) builder.insertField(FieldType.FIELD_TOC_ENTRY, true);
     fieldTc.setOmitPageNumber(true);
     fieldTc.setText(text);
     fieldTc.setTypeIdentifier(typeIdentifier);
     fieldTc.setEntryLevel(entryLevel);
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İçindekiler tablosu girişlerinin dahil edileceği seviye aralığı. |

### setEntrySeparator(String value) {#setEntrySeparator-java.lang.String}
```
public void setEntrySeparator(String value)
```


Bir giriş ile sayfa numarasını ayıran karakter dizisini ayarlar.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Bir giriş ile sayfa numarasını ayıran karakter dizisi. |

### setHeadingLevelRange(String value) {#setHeadingLevelRange-java.lang.String}
```
public void setHeadingLevelRange(String value)
```


Dahil edilecek başlık seviyelerinin aralığını ayarlar.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Dahil edilecek başlık seviyeleri aralığı. |

### setHideInWebLayout(boolean value) {#setHideInWebLayout-boolean}
```
public void setHideInWebLayout(boolean value)
```


Web düzeni görünümünde sekme lideri ve sayfa numaralarının gizlenip gizlenmeyeceğini ayarlar.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Web düzen görünümünde sekme lideri ve sayfa numaralarının gizlenip gizlenmeyeceği. |

### setInsertHyperlinks(boolean value) {#setInsertHyperlinks-boolean}
```
public void setInsertHyperlinks(boolean value)
```


İçindekiler tablosu girişlerinin hiperlink olup olmayacağını ayarlar.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İçindekiler tablosu girişlerinin bağlantı olup olmayacağını belirler. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Alanının LCID'sini ayarlar.

 **Examples:** 

Bir alanı nasıl ekleyeceğinizi ve yerel ayarıyla nasıl çalışacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Alanın LCID'si. |

### setPageNumberOmittingLevelRange(String value) {#setPageNumberOmittingLevelRange-java.lang.String}
```
public void setPageNumberOmittingLevelRange(String value)
```


Sayfa numaralarının atlanacağı içindekiler tablosu girişlerinin seviye aralığını ayarlar.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Sayfa numaralarının atlanacağı içindekiler tablosu giriş seviyelerinin aralığı. |

### setPrefixedSequenceIdentifier(String value) {#setPrefixedSequenceIdentifier-java.lang.String}
```
public void setPrefixedSequenceIdentifier(String value)
```


Girişin sayfa numarasına bir önek eklenmesi gereken dizinin tanımlayıcısını ayarlar.

 **Examples:** 

SEQ alanlarını kullanarak bir TOC alanını girişlerle doldurmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Girişin sayfa numarasına ön ek eklenmesi gereken bir dizi tanımlayıcısı. |

### setPreserveLineBreaks(boolean value) {#setPreserveLineBreaks-boolean}
```
public void setPreserveLineBreaks(boolean value)
```


Tablo girişleri içinde yeni satır karakterlerinin korunup korunmayacağını ayarlar.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Tablo girişleri içinde yeni satır karakterlerinin korunup korunmayacağını belirler. |

### setPreserveTabs(boolean value) {#setPreserveTabs-boolean}
```
public void setPreserveTabs(boolean value)
```


Tablo girişleri içinde sekme girişlerinin korunup korunmayacağını ayarlar.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Tablo girişleri içinde sekme karakterlerinin korunup korunmayacağını belirler. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Alan ayırıcı ile alan sonu arasındaki metni ayarlar.

 **Examples:** 

Alan kodu kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Alan ayırıcı ile alan sonu arasındaki metin. |

### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String}
```
public void setSequenceSeparator(String value)
```


Dizi numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter dizisini ayarlar.

 **Examples:** 

SEQ alanlarını kullanarak bir TOC alanını girişlerle doldurmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Dizi numaraları ile sayfa numaralarını ayırmak için kullanılan karakter dizisi. |

### setTableOfFiguresLabel(String value) {#setTableOfFiguresLabel-java.lang.String}
```
public void setTableOfFiguresLabel(String value)
```


Şekil tablosu oluşturulurken kullanılan dizi tanımlayıcısının adını ayarlar.

 **Examples:** 

SEQ alanlarını kullanarak bir TOC alanını girişlerle doldurmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A TOC field can create an entry in its table of contents for each SEQ field found in the document.
 // Each entry contains the paragraph that includes the SEQ field and the page's number that the field appears on.
 FieldToc fieldToc = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

 // SEQ fields display a count that increments at each SEQ field.
 // These fields also maintain separate counts for each unique named sequence
 // identified by the SEQ field's "SequenceIdentifier" property.
 // Use the "TableOfFiguresLabel" property to name a main sequence for the TOC.
 // Now, this TOC will only create entries out of SEQ fields with their "SequenceIdentifier" set to "MySequence".
 fieldToc.setTableOfFiguresLabel("MySequence");

 // We can name another SEQ field sequence in the "PrefixedSequenceIdentifier" property.
 // SEQ fields from this prefix sequence will not create TOC entries.
 // Every TOC entry created from a main sequence SEQ field will now also display the count that
 // the prefix sequence is currently on at the primary sequence SEQ field that made the entry.
 fieldToc.setPrefixedSequenceIdentifier("PrefixSequence");

 // Each TOC entry will display the prefix sequence count immediately to the left
 // of the page number that the main sequence SEQ field appears on.
 // We can specify a custom separator that will appear between these two numbers.
 fieldToc.setSequenceSeparator(">");

 Assert.assertEquals(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.getFieldCode());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // There are two ways of using SEQ fields to populate this TOC.
 // 1 -  Inserting a SEQ field that belongs to the TOC's prefix sequence:
 // This field will increment the SEQ sequence count for the "PrefixSequence" by 1.
 // Since this field does not belong to the main sequence identified
 // by the "TableOfFiguresLabel" property of the TOC, it will not appear as an entry.
 FieldSeq fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();

 Assert.assertEquals(" SEQ  PrefixSequence", fieldSeq.getFieldCode());

 // 2 -  Inserting a SEQ field that belongs to the TOC's main sequence:
 // This SEQ field will create an entry in the TOC.
 // The TOC entry will contain the paragraph that the SEQ field is in and the number of the page that it appears on.
 // This entry will also display the count that the prefix sequence is currently at,
 // separated from the page number by the value in the TOC's SeqenceSeparator property.
 // The "PrefixSequence" count is at 1, this main sequence SEQ field is on page 2,
 // and the separator is ">", so entry will display "1>2".
 builder.write("First TOC entry, MySequence #");
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("MySequence");

 Assert.assertEquals(" SEQ  MySequence", fieldSeq.getFieldCode());

 // Insert a page, advance the prefix sequence by 2, and insert a SEQ field to create a TOC entry afterwards.
 // The prefix sequence is now at 2, and the main sequence SEQ field is on page 3,
 // so the TOC entry will display "2>3" at its page count.
 builder.insertBreak(BreakType.PAGE_BREAK);
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 fieldSeq.setSequenceIdentifier("PrefixSequence");
 builder.insertParagraph();
 fieldSeq = (FieldSeq) builder.insertField(FieldType.FIELD_SEQUENCE, true);
 builder.write("Second TOC entry, MySequence #");
 fieldSeq.setSequenceIdentifier("MySequence");

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.TOC.SEQ.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Şekil tablosu oluşturulurken kullanılan dizi tanımlayıcısının adı. |

### setUseParagraphOutlineLevel(boolean value) {#setUseParagraphOutlineLevel-boolean}
```
public void setUseParagraphOutlineLevel(boolean value)
```


Uygulanan paragraf taslak seviyesinin kullanılıp kullanılmayacağını ayarlar.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Uygulanan paragraf taslak seviyesinin kullanılıp kullanılmayacağını belirler. |

### unlink() {#unlink}
```
public boolean unlink()
```


Alan bağlantısını kaldırır.

 **Remarks:** 

Alanı en son sonucu ile değiştirir.

XE (Dizin Girişi) alanları ve SEQ (Sıra) alanları gibi bazı alanlar bağlantısı kesilemez.

 **Examples:** 

Bir alanın bağlantısını nasıl keseceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Linked fields.docx");
 doc.getRange().getFields().get(1).unlink();
 
```

**Returns:**
boolean -  true  ise alanın bağlantısı kesilmiş demektir, aksi takdirde  false .
### update() {#update}
```
public void update()
```


Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır.

 **Examples:** 

FieldType kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

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

Alan sonuçlarını nasıl biçimlendireceğinizi gösterir.

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


Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır.

 **Examples:** 

Bir belge yüklenirken INCLUDEPICTURE alanlarını korumanın veya atmanın nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ignoreMergeFormat | boolean | true ise, MERGEFORMAT anahtarına bakılmaksızın doğrudan alan sonucu biçimlendirmesi bırakılır, aksi takdirde normal güncelleme yapılır. |

### updatePageNumbers() {#updatePageNumbers}
```
public boolean updatePageNumbers()
```


Bu içindekiler tablosundaki öğeler için sayfa numaralarını günceller.

 **Examples:** 

Bir TOC eklemenin ve başlık stillerine dayalı girişlerle doldurmanın nasıl yapılacağını gösterir.

```

 public void fieldToc() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startBookmark("MyBookmark");

     // Insert a TOC field, which will compile all headings into a table of contents.
     // For each heading, this field will create a line with the text in that heading style to the left,
     // and the page the heading appears on to the right.
     FieldToc field = (FieldToc) builder.insertField(FieldType.FIELD_TOC, true);

     // Use the BookmarkName property to only list headings
     // that appear within the bounds of a bookmark with the "MyBookmark" name.
     field.setBookmarkName("MyBookmark");

     // Text with a built-in heading style, such as "Heading 1", applied to it will count as a heading.
     // We can name additional styles to be picked up as headings by the TOC in this property and their TOC levels.
     field.setCustomStyles("Quote; 6; Intense Quote; 7");

     // By default, Styles/TOC levels are separated in the CustomStyles property by a comma,
     // but we can set a custom delimiter in this property.
     doc.getFieldOptions().setCustomTocStyleSeparator(";");

     // Configure the field to exclude any headings that have TOC levels outside of this range.
     field.setHeadingLevelRange("1-3");

     // The TOC will not display the page numbers of headings whose TOC levels are within this range.
     field.setPageNumberOmittingLevelRange("2-5");

     // Set a custom string that will separate every heading from its page number.
     field.setEntrySeparator("-");
     field.setInsertHyperlinks(true);
     field.setHideInWebLayout(false);
     field.setPreserveLineBreaks(true);
     field.setPreserveTabs(true);
     field.setUseParagraphOutlineLevel(false);

     insertNewPageWithHeading(builder, "First entry", "Heading 1");
     builder.writeln("Paragraph text.");
     insertNewPageWithHeading(builder, "Second entry", "Heading 1");
     insertNewPageWithHeading(builder, "Third entry", "Quote");
     insertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

     // These two headings will have the page numbers omitted because they are within the "2-5" range.
     insertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
     insertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

     // This entry does not appear because "Heading 4" is outside of the "1-3" range that we have set earlier.
     insertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

     builder.endBookmark("MyBookmark");
     builder.writeln("Paragraph text.");

     // This entry does not appear because it is outside the bookmark specified by the TOC.
     insertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

     Assert.assertEquals(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.getFieldCode());

     field.updatePageNumbers();
     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.TOC.docx");
 }

 /// 
 /// Start a new page and insert a paragraph of a specified style.
 /// 
 public void insertNewPageWithHeading(final DocumentBuilder builder, final String captionText, final String styleName) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     String originalStyle = builder.getParagraphFormat().getStyleName();
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(styleName));
     builder.writeln(captionText);
     builder.getParagraphFormat().setStyle(builder.getDocument().getStyles().get(originalStyle));
 }
 
```

**Returns:**
boolean - işlem başarılıysa true. İlgili TOC yer imlerinden herhangi biri kaldırıldıysa false döndürülür.
