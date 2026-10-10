---
title: "ImportFormatOptions"
linktitle: "ImportFormatOptions"
second_title: "Aspose.Words Java için"
description: "Java'da çıktıyı biçimlendirmek için çeşitli içe aktarma seçeneklerini belirtmeye izin verir."
type: docs
weight: 401
url: /tr/java/com.aspose.words/importformatoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatOptions
```

Çıktıyı biçimlendirmek için çeşitli içe aktarma seçeneklerini belirtmeye izin verir.

Daha fazla bilgi edinmek için, [ Specify Load Options ][Specify Load Options] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Belgeler eklenirken yinelenen stillerin nasıl çözüleceğini gösterir.

```

 Document dstDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(dstDoc);

 Style myStyle = builder.getDocument().getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 myStyle.getFont().setSize(14.0);
 myStyle.getFont().setName("Courier New");
 myStyle.getFont().setColor(Color.BLUE);

 builder.getParagraphFormat().setStyleName(myStyle.getName());
 builder.writeln("Hello world!");

 // Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
 // If we insert the clone into the original document, the two styles with the same name will cause a clash.
 Document srcDoc = dstDoc.deepClone();
 srcDoc.getStyles().get("MyStyle").getFont().setColor(Color.RED);

 // When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
 // Aspose.Words will resolve style clashes by converting source document styles.
 // with the same names as destination styles into direct paragraph attributes.
 ImportFormatOptions options = new ImportFormatOptions();
 options.setSmartStyleBehavior(true);

 builder.insertDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.SmartStyleBehavior.docx");
 
```


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAdjustSentenceAndWordSpacing()](#getAdjustSentenceAndWordSpacing) | Cümle ve kelime aralığını otomatik olarak ayarlayıp ayarlamayacağını belirten bir boolean değer alır. |
| [getAppendDocumentWithNewPage()](#getAppendDocumentWithNewPage) | İlk içe aktarılan bölüm tipini, **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** çağrıldığında zorla [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) tipine değiştireceğini belirten bir boolean değer alır. |
| [getForceCopyStyles()](#getForceCopyStyles) | [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modunda çakışan stilleri kopyalayıp kopyalamayacağını belirten bir boolean değer alır. |
| [getIgnoreHeaderFooter()](#getIgnoreHeaderFooter) | [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modu kullanıldığında başlık/altbilgi içeriğinin kaynak biçimlendirmesinin yoksayılacağını belirten bir boolean değer alır. |
| [getIgnoreTextBoxes()](#getIgnoreTextBoxes) | [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modu kullanıldığında metin kutusu içeriğinin kaynak biçimlendirmesinin yoksayılacağını belirten bir boolean değer alır. |
| [getKeepSourceNumbering()](#getKeepSourceNumbering) | Kaynak ve hedef belgelerde numaralandırma çakıştığında nasıl içe aktarılacağını belirten bir boolean değer alır. |
| [getMergePastedLists()](#getMergePastedLists) | Yapıştırılan listelerin çevredeki listelerle birleştirileceğini belirten bir boolean değer alır. |
| [getResolveThemeColors()](#getResolveThemeColors) | Şekillerin tema renklerini zorla çözümleyip çözümlemeyeceğini belirten bir boolean değer alır. |
| [getSmartStyleBehavior()](#getSmartStyleBehavior) | Kaynak ve hedef belgelerde aynı ada sahip stillerin nasıl içe aktarılacağını belirten bir boolean değer alır. |
| [setAdjustSentenceAndWordSpacing(boolean value)](#setAdjustSentenceAndWordSpacing-boolean) | Cümle ve kelime aralığını otomatik olarak ayarlayıp ayarlamayacağını belirten bir boolean değer ayarlar. |
| [setAppendDocumentWithNewPage(boolean value)](#setAppendDocumentWithNewPage-boolean) | İlk içe aktarılan bölüm tipini, **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** çağrıldığında zorla [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) tipine değiştireceğini belirten bir boolean değer ayarlar. |
| [setForceCopyStyles(boolean value)](#setForceCopyStyles-boolean) | [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modunda çakışan stillerin kopyalanıp kopyalanmayacağını belirten bir boolean değer ayarlar. |
| [setIgnoreHeaderFooter(boolean value)](#setIgnoreHeaderFooter-boolean) | [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modu kullanıldığında üstbilgi/altbilgi içeriğinin kaynak biçimlendirmesinin yoksayılacağını belirten bir boolean değer ayarlar. |
| [setIgnoreTextBoxes(boolean value)](#setIgnoreTextBoxes-boolean) | [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modu kullanıldığında metin kutularının içeriğinin kaynak biçimlendirmesinin yoksayılacağını belirten bir boolean değer ayarlar. |
| [setKeepSourceNumbering(boolean value)](#setKeepSourceNumbering-boolean) | Kaynak ve hedef belgelerde numaralandırmanın çakıştığında nasıl içe aktarılacağını belirten bir boolean değer ayarlar. |
| [setMergePastedLists(boolean value)](#setMergePastedLists-boolean) | Yapıştırılan listelerin çevredeki listelerle birleştirileceğini belirten bir boolean değer ayarlar. |
| [setResolveThemeColors(boolean value)](#setResolveThemeColors-boolean) | Şekillerin tema renklerini zorla çözümleyip çözümlemeyeceğini belirten bir boolean değer ayarlar. |
| [setSmartStyleBehavior(boolean value)](#setSmartStyleBehavior-boolean) | Kaynak ve hedef belgelerde aynı ada sahip stillerin nasıl içe aktarılacağını belirten bir boolean değer alır. Varsayılan değer false'tur. |
### getAdjustSentenceAndWordSpacing() {#getAdjustSentenceAndWordSpacing}
```
public boolean getAdjustSentenceAndWordSpacing()
```


Cümle ve kelime aralığını otomatik olarak nasıl ayarlayacağınızı gösterir.

 **Examples:** 

boolean - Cümle ve kelime aralığını otomatik olarak ayarlayıp ayarlamayacağını belirten bir boolean değer.

```

 Document srcDoc = new Document();
 Document dstDoc = new Document();

 DocumentBuilder builder = new DocumentBuilder(srcDoc);
 builder.write("Dolor sit amet.");

 builder = new DocumentBuilder(dstDoc);
 builder.write("Lorem ipsum.");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setAdjustSentenceAndWordSpacing(true); }
 builder.insertDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 Assert.assertEquals("Lorem ipsum. Dolor sit amet.", dstDoc.getFirstSection().getBody().getFirstParagraph().getText().trim());
 
```

**Returns:**
Lütfen bu seçeneğin yalnızca **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** yöntemiyle ilgili olduğunu ve diğer içe aktarma ile ilgili yöntemleri etkilemediğini unutmayın.
### getAppendDocumentWithNewPage() {#getAppendDocumentWithNewPage}
```
public boolean getAppendDocumentWithNewPage()
```


İlk içe aktarılan bölüm tipini, **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** çağrıldığında zorla [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) tipine değiştireceğini belirten bir boolean değer alır.

Varsayılan değer  true .

 **Remarks:** 

Orijinal bölüm tipini nasıl koruyacağınızı gösterir.

 **Examples:** 

boolean - İlk içe aktarılan bölüm tipini, **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** çağrıldığında zorla [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) tipine değiştirip değiştirmeyeceğini belirten bir boolean değer.

```

 Document dstDoc = new Document();
 Document srcDoc = new Document();

 srcDoc.getFirstSection().getPageSetup().setSectionStart(SectionStart.CONTINUOUS);

 ImportFormatOptions options = new ImportFormatOptions();
 options.setAppendDocumentWithNewPage(false);
 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 Assert.assertEquals(SectionStart.CONTINUOUS, dstDoc.getSections().get(1).getPageSetup().getSectionStart());
 
```

**Returns:**
[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modunda çakışan stillerin kopyalanıp kopyalanmayacağını belirten bir boolean değer alır. Varsayılan değer false'tur.
### getForceCopyStyles() {#getForceCopyStyles}
```
public boolean getForceCopyStyles()
```


Varsayılan olarak, hedef belgede eşleşen bir stil zaten varsa, kaynak stil biçimlendirmesi doğrudan düğüm özniteliklerine genişletilir ve bu düğümün stili varsayılan olarak sıfırlanır.

 **Remarks:** 

Bu seçenek true olarak ayarlandığında, kaynak stil benzersiz bir adla zorla hedef belgeye kopyalanır ve içe aktarılan düğüme uygulanır.

Not: Bu durumda, hedef belgede içe aktarılan düğümün biçimlendirmesinin korunacağı garanti edilmez.

Kaynak stilleri benzersiz adlarla zorla nasıl kopyalayacağınızı gösterir.

 **Examples:** 

boolean - [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modunda çakışan stillerin kopyalanıp kopyalanmayacağını belirten bir boolean değer.

```

 // Both documents contain MyStyle1 and MyStyle2, MyStyle3 exists only in a source document.
 Document srcDoc = new Document(getMyDir() + "Styles source.docx");
 Document dstDoc = new Document(getMyDir() + "Styles destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setForceCopyStyles(true); }
 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 ParagraphCollection paras = dstDoc.getSections().get(1).getBody().getParagraphs();

 Assert.assertEquals(paras.get(0).getParagraphFormat().getStyle().getName(), "MyStyle1_0");
 Assert.assertEquals(paras.get(1).getParagraphFormat().getStyle().getName(), "MyStyle2_0");
 Assert.assertEquals(paras.get(2).getParagraphFormat().getStyle().getName(), "MyStyle3");
 
```

**Returns:**
[ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modu kullanıldığında üstbilgi/altbilgi içeriğinin kaynak biçimlendirmesinin yoksayılacağını belirten bir boolean değer alır. Varsayılan değer true'tur.
### getIgnoreHeaderFooter() {#getIgnoreHeaderFooter}
```
public boolean getIgnoreHeaderFooter()
```


Kaynak başlık/altbilgi içeriğinin biçimlendirmesinin, [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modu kullanıldığında yoksayıldığını belirten bir boolean değer döndürür. Varsayılan değer true.

 **Examples:** 

Üstbilgi/altbilgi içeriğinin kaynak biçimlendirmesinin yoksayılması veya yoksayılmaması nasıl gösterilir.

```

 Document dstDoc = new Document(getMyDir() + "Document.docx");
 Document srcDoc = new Document(getMyDir() + "Header and footer types.docx");

 // If 'IgnoreHeaderFooter' is false then the original formatting for header/footer content
 // from "Header and footer types.docx" will be used.
 // If 'IgnoreHeaderFooter' is true then the formatting for header/footer content
 // from "Document.docx" will be used.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setIgnoreHeaderFooter(false);

 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, importFormatOptions);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
 
```

**Returns:**
boolean - Başlık/altbilgi içeriğinin kaynak biçimlendirmesinin, [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modu kullanıldığında yoksayıldığını belirten bir boolean değerdir.
### getIgnoreTextBoxes() {#getIgnoreTextBoxes}
```
public boolean getIgnoreTextBoxes()
```


Kaynak biçimlendirmesinin, [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modu kullanıldığında metin kutusu içeriğinin yoksayıldığını belirten bir boolean değeri alır. Varsayılan değer true.

 **Examples:** 

Bir belge eklenirken metin kutusu biçimlendirmesinin nasıl yönetileceği gösterilir.

```

 // Create a document that will have nodes from another document inserted into it.
 Document dstDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(dstDoc);

 builder.writeln("Hello world!");

 // Create another document with a text box, which we will import into the first document.
 Document srcDoc = new Document();
 builder = new DocumentBuilder(srcDoc);

 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 300.0, 100.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.getParagraphFormat().getStyle().getFont().setName("Courier New");
 builder.getParagraphFormat().getStyle().getFont().setSize(24.0);
 builder.write("Textbox contents");

 // Set a flag to specify whether to clear or preserve text box formatting
 // while importing them to other documents.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setIgnoreTextBoxes(ignoreTextBoxes);

 // Import the text box from the source document into the destination document,
 // and then verify whether we have preserved the styling of its text contents.
 NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, importFormatOptions);
 Shape importedTextBox = (Shape) importer.importNode(textBox, true);
 dstDoc.getFirstSection().getBody().getParagraphs().get(1).appendChild(importedTextBox);

 if (ignoreTextBoxes) {
     Assert.assertEquals(12.0d, importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getSize());
     Assert.assertEquals("Times New Roman", importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getName());
 } else {
     Assert.assertEquals(24.0d, importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getSize());
     Assert.assertEquals("Courier New", importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getName());
 }

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.IgnoreTextBoxes.docx");
 
```

**Returns:**
boolean - Metin kutusu içeriğinin kaynak biçimlendirmesinin, [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modu kullanıldığında yoksayıldığını belirten bir boolean değerdir.
### getKeepSourceNumbering() {#getKeepSourceNumbering}
```
public boolean getKeepSourceNumbering()
```


Kaynak ve hedef belgelerde numaralandırma çakıştığında nasıl içe aktarılacağını belirten bir boolean değeri alır. Varsayılan değer false.

 **Examples:** 

Numaralı listeler içeren bir belgenin nasıl içe aktarılacağını gösterir.

```

 Document srcDoc = new Document(getMyDir() + "List source.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 Assert.assertEquals(dstDoc.getLists().getCount(), 4);

 ImportFormatOptions options = new ImportFormatOptions();

 // If there is a clash of list styles, apply the list format of the source document.
 // Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
 // Set the "KeepSourceNumbering" property to "true" import all clashing
 // list style numbering with the same appearance that it had in the source document.
 options.setKeepSourceNumbering(isKeepSourceNumbering);

 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);
 dstDoc.updateListLabels();

 if (isKeepSourceNumbering)
     Assert.assertEquals(dstDoc.getLists().getCount(), 5);
 else
     Assert.assertEquals(dstDoc.getLists().getCount(), 4);
 
```

Aynı liste tanım tanımlayıcısına sahip listeler içeren belgeler içe aktarılırken bir çakışmanın nasıl çözüleceğini gösterir.

```

 Document srcDoc = new Document(getMyDir() + "List with the same definition identifier - source.docx");
 Document dstDoc = new Document(getMyDir() + "List with the same definition identifier - destination.docx");

 ImportFormatOptions importFormatOptions = new ImportFormatOptions();

 // Set the "KeepSourceNumbering" property to "true" to apply a different list definition ID
 // to identical styles as Aspose.Words imports them into destination documents.
 importFormatOptions.setKeepSourceNumbering(true);
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, importFormatOptions);

 dstDoc.updateListLabels();
 
```

Kaynak ve hedef belgelerdeki liste numaralandırma çakışmalarının nasıl çözüleceğini gösterir.

```

 // Open a document with a custom list numbering scheme, and then clone it.
 // Since both have the same numbering format, the formats will clash if we import one document into the other.
 Document srcDoc = new Document(getMyDir() + "Custom list numbering.docx");
 Document dstDoc = srcDoc.deepClone();

 // When we import the document's clone into the original and then append it,
 // then the two lists with the same list format will join.
 // If we set the "KeepSourceNumbering" flag to "false", then the list from the document clone
 // that we append to the original will carry on the numbering of the list we append it to.
 // This will effectively merge the two lists into one.
 // If we set the "KeepSourceNumbering" flag to "true", then the document clone
 // list will preserve its original numbering, making the two lists appear as separate lists.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setKeepSourceNumbering(keepSourceNumbering);

 NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KEEP_DIFFERENT_STYLES, importFormatOptions);
 for (Paragraph paragraph : srcDoc.getFirstSection().getBody().getParagraphs()) {
     Node importedNode = importer.importNode(paragraph, true);
     dstDoc.getFirstSection().getBody().appendChild(importedNode);
 }

 dstDoc.updateListLabels();

 if (keepSourceNumbering) {
     Assert.assertEquals(
             "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4\r\n" +
                     "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4", dstDoc.getFirstSection().getBody().toString(SaveFormat.TEXT).trim());
 } else {
     Assert.assertEquals(
             "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4\r\n" +
                     "10. Item 1\r\n" +
                     "11. Item 2 \r\n" +
                     "12. Item 3\r\n" +
                     "13. Item 4", dstDoc.getFirstSection().getBody().toString(SaveFormat.TEXT).trim());
 }
 
```

**Returns:**
boolean - Kaynak ve hedef belgelerde numaralandırma çakıştığında nasıl içe aktarılacağını belirten bir boolean değerdir.
### getMergePastedLists() {#getMergePastedLists}
```
public boolean getMergePastedLists()
```


Yapıştırılan listelerin çevredeki listelerle birleştirileceğini belirten bir boolean değeri alır. Varsayılan değer false.

 **Examples:** 

Bir belgelerden listelerin nasıl birleştirileceğini gösterir.

```

 Document srcDoc = new Document(getMyDir() + "List item.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setMergePastedLists(true); }

 // Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 dstDoc.save(getArtifactsDir() + "Document.MergePastedLists.docx");
 
```

**Returns:**
boolean - Yapıştırılan listelerin çevredeki listelerle birleştirileceğini belirten bir boolean değerdir.
### getResolveThemeColors() {#getResolveThemeColors}
```
public boolean getResolveThemeColors()
```


Şekillerin tema renklerinin zorla çözüleceğini belirten bir boolean değeri alır. Varsayılan değer false.

 **Remarks:** 

Lütfen bu seçeneğin yalnızca [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modu için geçerli olduğunu unutmayın.

Normalde, Aspose.Words, biçimlendirme özniteliklerini doğrudan özniteliklere genişletmeden stiller korunabildiğinde kaynak tema renklerini çözmez. Ancak bu durumda içe aktarılan şekillerin gerçek renkleri, orijinal belgede sahip oldukları renklerden farklı olabilir. Bunun nedeni kaynak ve hedef belgelerdeki farklı tema renkleridir. Bu seçeneği true olarak ayarlamak, kaynak şekil tema renklerinin çözülmesini zorlar ve böylece şekillerin kaynak belgede sahip oldukları gerçek rengi korur.

 **Examples:** 

Şekillerin kaynak tema renklerini çözerken bir düğümün nasıl içe aktarılacağını gösterir.

```

 Document srcDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(srcDoc);

 // Move to the primary footer and insert a shape that uses theme colors.
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 50.0);
 shape.getStroke().setForeThemeColor(ThemeColor.DARK_1);

 Document dstDoc = new Document();
 // Import the source footer into the destination document with theme colors resolved,
 // so the shape preserves its actual color from the source document.
 HeaderFooter footer = srcDoc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_PRIMARY);

 ImportFormatOptions options = new ImportFormatOptions();
 options.setResolveThemeColors(true);
 HeaderFooter importedFooter = (HeaderFooter)dstDoc.importNode(footer, true, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 dstDoc.getFirstSection().getHeadersFooters().add(importedFooter);

 dstDoc.save(getArtifactsDir() + "DocumentBase.ImportNodeWithResolveThemeColors.docx");
 
```

**Returns:**
boolean - Şekillerin tema renklerinin zorla çözülüp çözülemeyeceğini belirten bir boolean değerdir.
### getSmartStyleBehavior() {#getSmartStyleBehavior}
```
public boolean getSmartStyleBehavior()
```


Kaynak ve hedef belgelerde aynı ada sahip stillerin nasıl içe aktarılacağını belirten bir boolean değeri alır. Varsayılan değer false.

 **Remarks:** 

Bu seçenek **etkin** olduğunda, [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) içe aktarma modu kullanılırsa, kaynak stil hedef belgede doğrudan özniteliklere genişletilir.

Bu seçenek **devre dışı** olduğunda, kaynak stil yalnızca numaralandırılmışsa genişletilir. Mevcut hedef öznitelikler, listeler dahil, üzerine yazılmaz.

 **Examples:** 

Belgeler eklenirken yinelenen stillerin nasıl çözüleceğini gösterir.

```

 Document dstDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(dstDoc);

 Style myStyle = builder.getDocument().getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 myStyle.getFont().setSize(14.0);
 myStyle.getFont().setName("Courier New");
 myStyle.getFont().setColor(Color.BLUE);

 builder.getParagraphFormat().setStyleName(myStyle.getName());
 builder.writeln("Hello world!");

 // Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
 // If we insert the clone into the original document, the two styles with the same name will cause a clash.
 Document srcDoc = dstDoc.deepClone();
 srcDoc.getStyles().get("MyStyle").getFont().setColor(Color.RED);

 // When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
 // Aspose.Words will resolve style clashes by converting source document styles.
 // with the same names as destination styles into direct paragraph attributes.
 ImportFormatOptions options = new ImportFormatOptions();
 options.setSmartStyleBehavior(true);

 builder.insertDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.SmartStyleBehavior.docx");
 
```

**Returns:**
boolean - Kaynak ve hedef belgelerde aynı ada sahip stillerin nasıl içe aktarılacağını belirten bir boolean değerdir.
### setAdjustSentenceAndWordSpacing(boolean value) {#setAdjustSentenceAndWordSpacing-boolean}
```
public void setAdjustSentenceAndWordSpacing(boolean value)
```


Cümle ve kelime aralığını otomatik olarak ayarlayıp ayarlamayacağını belirten bir boolean değeri ayarlar. Varsayılan değer false.

 **Examples:** 

boolean - Cümle ve kelime aralığını otomatik olarak ayarlayıp ayarlamayacağını belirten bir boolean değer.

```

 Document srcDoc = new Document();
 Document dstDoc = new Document();

 DocumentBuilder builder = new DocumentBuilder(srcDoc);
 builder.write("Dolor sit amet.");

 builder = new DocumentBuilder(dstDoc);
 builder.write("Lorem ipsum.");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setAdjustSentenceAndWordSpacing(true); }
 builder.insertDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 Assert.assertEquals("Lorem ipsum. Dolor sit amet.", dstDoc.getFirstSection().getBody().getFirstParagraph().getText().trim());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Cümle ve kelime aralığını otomatik olarak ayarlayıp ayarlamayacağını belirten bir boolean değerdir. |

### setAppendDocumentWithNewPage(boolean value) {#setAppendDocumentWithNewPage-boolean}
```
public void setAppendDocumentWithNewPage(boolean value)
```


İlk içe aktarılan bölüm tipini, **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** çağrıldığında zorla [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) tipine değiştireceğini belirten bir boolean değer ayarlar.

Varsayılan değer  true .

 **Remarks:** 

Orijinal bölüm tipini nasıl koruyacağınızı gösterir.

 **Examples:** 

boolean - İlk içe aktarılan bölüm tipini, **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** çağrıldığında zorla [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) tipine değiştirip değiştirmeyeceğini belirten bir boolean değer.

```

 Document dstDoc = new Document();
 Document srcDoc = new Document();

 srcDoc.getFirstSection().getPageSetup().setSectionStart(SectionStart.CONTINUOUS);

 ImportFormatOptions options = new ImportFormatOptions();
 options.setAppendDocumentWithNewPage(false);
 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 Assert.assertEquals(SectionStart.CONTINUOUS, dstDoc.getSections().get(1).getPageSetup().getSectionStart());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | boolean | İlk içe aktarılan bölüm tipinin, **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** çağrıldığında zorla [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) olarak değiştirilip değiştirilmeyeceğini belirten bir boolean değerdir. |

### setForceCopyStyles(boolean value) {#setForceCopyStyles-boolean}
```
public void setForceCopyStyles(boolean value)
```


Çakışan stillerin [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modunda kopyalanıp kopyalanmayacağını belirten bir boolean değer ayarlar. Varsayılan değer false.

 **Remarks:** 

Bu seçenek true olarak ayarlandığında, kaynak stil benzersiz bir adla zorla hedef belgeye kopyalanır ve içe aktarılan düğüme uygulanır.

Not: Bu durumda, hedef belgede içe aktarılan düğümün biçimlendirmesinin korunacağı garanti edilmez.

Kaynak stilleri benzersiz adlarla zorla nasıl kopyalayacağınızı gösterir.

 **Examples:** 

boolean - [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modunda çakışan stillerin kopyalanıp kopyalanmayacağını belirten bir boolean değer.

```

 // Both documents contain MyStyle1 and MyStyle2, MyStyle3 exists only in a source document.
 Document srcDoc = new Document(getMyDir() + "Styles source.docx");
 Document dstDoc = new Document(getMyDir() + "Styles destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setForceCopyStyles(true); }
 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 ParagraphCollection paras = dstDoc.getSections().get(1).getBody().getParagraphs();

 Assert.assertEquals(paras.get(0).getParagraphFormat().getStyle().getName(), "MyStyle1_0");
 Assert.assertEquals(paras.get(1).getParagraphFormat().getStyle().getName(), "MyStyle2_0");
 Assert.assertEquals(paras.get(2).getParagraphFormat().getStyle().getName(), "MyStyle3");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | boolean | Çakışan stillerin [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modunda kopyalanıp kopyalanmayacağını belirten bir boolean değer. |

### setIgnoreHeaderFooter(boolean value) {#setIgnoreHeaderFooter-boolean}
```
public void setIgnoreHeaderFooter(boolean value)
```


Başlık/altbilgi içeriğinin kaynak biçimlendirmesinin, [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modu kullanıldığında yoksayılacağını belirten bir boolean değer ayarlar. Varsayılan değer true.

 **Examples:** 

Üstbilgi/altbilgi içeriğinin kaynak biçimlendirmesinin yoksayılması veya yoksayılmaması nasıl gösterilir.

```

 Document dstDoc = new Document(getMyDir() + "Document.docx");
 Document srcDoc = new Document(getMyDir() + "Header and footer types.docx");

 // If 'IgnoreHeaderFooter' is false then the original formatting for header/footer content
 // from "Header and footer types.docx" will be used.
 // If 'IgnoreHeaderFooter' is true then the formatting for header/footer content
 // from "Document.docx" will be used.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setIgnoreHeaderFooter(false);

 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, importFormatOptions);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | boolean | Başlık/altbilgi içeriğinin kaynak biçimlendirmesinin, [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modu kullanıldığında yoksayılacağını belirten bir boolean değer. |

### setIgnoreTextBoxes(boolean value) {#setIgnoreTextBoxes-boolean}
```
public void setIgnoreTextBoxes(boolean value)
```


Metin kutularının içeriğinin kaynak biçimlendirmesinin, [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modu kullanıldığında yoksayılacağını belirten bir boolean değer ayarlar. Varsayılan değer true.

 **Examples:** 

Bir belge eklenirken metin kutusu biçimlendirmesinin nasıl yönetileceği gösterilir.

```

 // Create a document that will have nodes from another document inserted into it.
 Document dstDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(dstDoc);

 builder.writeln("Hello world!");

 // Create another document with a text box, which we will import into the first document.
 Document srcDoc = new Document();
 builder = new DocumentBuilder(srcDoc);

 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 300.0, 100.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.getParagraphFormat().getStyle().getFont().setName("Courier New");
 builder.getParagraphFormat().getStyle().getFont().setSize(24.0);
 builder.write("Textbox contents");

 // Set a flag to specify whether to clear or preserve text box formatting
 // while importing them to other documents.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setIgnoreTextBoxes(ignoreTextBoxes);

 // Import the text box from the source document into the destination document,
 // and then verify whether we have preserved the styling of its text contents.
 NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, importFormatOptions);
 Shape importedTextBox = (Shape) importer.importNode(textBox, true);
 dstDoc.getFirstSection().getBody().getParagraphs().get(1).appendChild(importedTextBox);

 if (ignoreTextBoxes) {
     Assert.assertEquals(12.0d, importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getSize());
     Assert.assertEquals("Times New Roman", importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getName());
 } else {
     Assert.assertEquals(24.0d, importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getSize());
     Assert.assertEquals("Courier New", importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getName());
 }

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.IgnoreTextBoxes.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | boolean | Metin kutularının içeriğinin kaynak biçimlendirmesinin, [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modu kullanıldığında yoksayılacağını belirten bir boolean değer. |

### setKeepSourceNumbering(boolean value) {#setKeepSourceNumbering-boolean}
```
public void setKeepSourceNumbering(boolean value)
```


Kaynak ve hedef belgelerde çakıştığında numaralandırmanın nasıl içe aktarılacağını belirten bir boolean değer ayarlar. Varsayılan değer false.

 **Examples:** 

Numaralı listeler içeren bir belgenin nasıl içe aktarılacağını gösterir.

```

 Document srcDoc = new Document(getMyDir() + "List source.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 Assert.assertEquals(dstDoc.getLists().getCount(), 4);

 ImportFormatOptions options = new ImportFormatOptions();

 // If there is a clash of list styles, apply the list format of the source document.
 // Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
 // Set the "KeepSourceNumbering" property to "true" import all clashing
 // list style numbering with the same appearance that it had in the source document.
 options.setKeepSourceNumbering(isKeepSourceNumbering);

 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);
 dstDoc.updateListLabels();

 if (isKeepSourceNumbering)
     Assert.assertEquals(dstDoc.getLists().getCount(), 5);
 else
     Assert.assertEquals(dstDoc.getLists().getCount(), 4);
 
```

Aynı liste tanım tanımlayıcısına sahip listeler içeren belgeler içe aktarılırken bir çakışmanın nasıl çözüleceğini gösterir.

```

 Document srcDoc = new Document(getMyDir() + "List with the same definition identifier - source.docx");
 Document dstDoc = new Document(getMyDir() + "List with the same definition identifier - destination.docx");

 ImportFormatOptions importFormatOptions = new ImportFormatOptions();

 // Set the "KeepSourceNumbering" property to "true" to apply a different list definition ID
 // to identical styles as Aspose.Words imports them into destination documents.
 importFormatOptions.setKeepSourceNumbering(true);
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, importFormatOptions);

 dstDoc.updateListLabels();
 
```

Kaynak ve hedef belgelerdeki liste numaralandırma çakışmalarının nasıl çözüleceğini gösterir.

```

 // Open a document with a custom list numbering scheme, and then clone it.
 // Since both have the same numbering format, the formats will clash if we import one document into the other.
 Document srcDoc = new Document(getMyDir() + "Custom list numbering.docx");
 Document dstDoc = srcDoc.deepClone();

 // When we import the document's clone into the original and then append it,
 // then the two lists with the same list format will join.
 // If we set the "KeepSourceNumbering" flag to "false", then the list from the document clone
 // that we append to the original will carry on the numbering of the list we append it to.
 // This will effectively merge the two lists into one.
 // If we set the "KeepSourceNumbering" flag to "true", then the document clone
 // list will preserve its original numbering, making the two lists appear as separate lists.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setKeepSourceNumbering(keepSourceNumbering);

 NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KEEP_DIFFERENT_STYLES, importFormatOptions);
 for (Paragraph paragraph : srcDoc.getFirstSection().getBody().getParagraphs()) {
     Node importedNode = importer.importNode(paragraph, true);
     dstDoc.getFirstSection().getBody().appendChild(importedNode);
 }

 dstDoc.updateListLabels();

 if (keepSourceNumbering) {
     Assert.assertEquals(
             "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4\r\n" +
                     "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4", dstDoc.getFirstSection().getBody().toString(SaveFormat.TEXT).trim());
 } else {
     Assert.assertEquals(
             "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4\r\n" +
                     "10. Item 1\r\n" +
                     "11. Item 2 \r\n" +
                     "12. Item 3\r\n" +
                     "13. Item 4", dstDoc.getFirstSection().getBody().toString(SaveFormat.TEXT).trim());
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Kaynak ve hedef belgelerde çakıştığında numaralandırmanın nasıl içe aktarılacağını belirten bir boolean değer. |

### setMergePastedLists(boolean value) {#setMergePastedLists-boolean}
```
public void setMergePastedLists(boolean value)
```


Yapıştırılan listelerin çevredeki listelerle birleştirileceğini belirten bir boolean değer ayarlar. Varsayılan değer false.

 **Examples:** 

Bir belgelerden listelerin nasıl birleştirileceğini gösterir.

```

 Document srcDoc = new Document(getMyDir() + "List item.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setMergePastedLists(true); }

 // Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 dstDoc.save(getArtifactsDir() + "Document.MergePastedLists.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Yapıştırılan listelerin çevredeki listelerle birleştirileceğini belirten bir boolean değer. |

### setResolveThemeColors(boolean value) {#setResolveThemeColors-boolean}
```
public void setResolveThemeColors(boolean value)
```


Şekillerin tema renklerinin zorla çözüleceğini belirten bir boolean değer ayarlar. Varsayılan değer false.

 **Remarks:** 

Lütfen bu seçeneğin yalnızca [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) modu için geçerli olduğunu unutmayın.

Normalde, Aspose.Words, biçimlendirme özniteliklerini doğrudan özniteliklere genişletmeden stiller korunabildiğinde kaynak tema renklerini çözmez. Ancak bu durumda içe aktarılan şekillerin gerçek renkleri, orijinal belgede sahip oldukları renklerden farklı olabilir. Bunun nedeni kaynak ve hedef belgelerdeki farklı tema renkleridir. Bu seçeneği true olarak ayarlamak, kaynak şekil tema renklerinin çözülmesini zorlar ve böylece şekillerin kaynak belgede sahip oldukları gerçek rengi korur.

 **Examples:** 

Şekillerin kaynak tema renklerini çözerken bir düğümün nasıl içe aktarılacağını gösterir.

```

 Document srcDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(srcDoc);

 // Move to the primary footer and insert a shape that uses theme colors.
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 50.0);
 shape.getStroke().setForeThemeColor(ThemeColor.DARK_1);

 Document dstDoc = new Document();
 // Import the source footer into the destination document with theme colors resolved,
 // so the shape preserves its actual color from the source document.
 HeaderFooter footer = srcDoc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_PRIMARY);

 ImportFormatOptions options = new ImportFormatOptions();
 options.setResolveThemeColors(true);
 HeaderFooter importedFooter = (HeaderFooter)dstDoc.importNode(footer, true, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 dstDoc.getFirstSection().getHeadersFooters().add(importedFooter);

 dstDoc.save(getArtifactsDir() + "DocumentBase.ImportNodeWithResolveThemeColors.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Şekillerin tema renklerinin zorla çözüleceğini belirten bir boolean değer. |

### setSmartStyleBehavior(boolean value) {#setSmartStyleBehavior-boolean}
```
public void setSmartStyleBehavior(boolean value)
```


Kaynak ve hedef belgelerde aynı ada sahip stillerin nasıl içe aktarılacağını belirten bir boolean değer ayarlar. Varsayılan değer false.

 **Remarks:** 

Bu seçenek **etkin** olduğunda, [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) içe aktarma modu kullanılırsa, kaynak stil hedef belgede doğrudan özniteliklere genişletilir.

Bu seçenek **devre dışı** olduğunda, kaynak stil yalnızca numaralandırılmışsa genişletilir. Mevcut hedef öznitelikler, listeler dahil, üzerine yazılmaz.

 **Examples:** 

Belgeler eklenirken yinelenen stillerin nasıl çözüleceğini gösterir.

```

 Document dstDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(dstDoc);

 Style myStyle = builder.getDocument().getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 myStyle.getFont().setSize(14.0);
 myStyle.getFont().setName("Courier New");
 myStyle.getFont().setColor(Color.BLUE);

 builder.getParagraphFormat().setStyleName(myStyle.getName());
 builder.writeln("Hello world!");

 // Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
 // If we insert the clone into the original document, the two styles with the same name will cause a clash.
 Document srcDoc = dstDoc.deepClone();
 srcDoc.getStyles().get("MyStyle").getFont().setColor(Color.RED);

 // When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
 // Aspose.Words will resolve style clashes by converting source document styles.
 // with the same names as destination styles into direct paragraph attributes.
 ImportFormatOptions options = new ImportFormatOptions();
 options.setSmartStyleBehavior(true);

 builder.insertDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.SmartStyleBehavior.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Kaynak ve hedef belgelerde aynı ada sahip stillerin nasıl içe aktarılacağını belirten bir boolean değer. |

