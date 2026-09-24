---
title: "DocumentBuilder"
linktitle: "DocumentBuilder"
second_title: "Aspose.Words Java için"
description: "Java'da yazı, resim ve diğer içerikleri eklemek, yazı tipi, paragraf ve bölüm biçimlendirmesini belirtmek için yöntemler sağlar."
type: docs
weight: 163
url: /tr/java/com.aspose.words/documentbuilder/
---

**Inheritance:**
java.lang.Object
```
public class DocumentBuilder
```

Metin, resim ve diğer içerikleri eklemek, yazı tipi, paragraf ve bölüm biçimlendirmesini belirtmek için yöntemler sağlar.

Daha fazla bilgi edinmek için, [ Document Builder Overview ][Document Builder Overview] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

[DocumentBuilder](../../com.aspose.words/documentbuilder/) makes the process of building a [Document](../../com.aspose.words/document/) easier. [Document](../../com.aspose.words/document/) is a composite object consisting of a tree of nodes and while inserting content nodes directly into the tree is possible, it requires good understanding of the tree structure. [DocumentBuilder](../../com.aspose.words/documentbuilder/) is a "facade" for the complex structure of [Document](../../com.aspose.words/document/) and allows to insert content and formatting quickly and easily.

Bir [DocumentBuilder](../../com.aspose.words/documentbuilder/) oluşturun ve bir [Document](../../com.aspose.words/document/) ile ilişkilendirin.

Bu [DocumentBuilder](../../com.aspose.words/documentbuilder/) içinde, [write(java.lang.String)](../../com.aspose.words/documentbuilder/\#write-java.lang.String), [writeln(java.lang.String)](../../com.aspose.words/documentbuilder/\#writeln-java.lang.String) ve **M:Aspose.Words.DocumentBuilder.InsertBreak(Aspose.Words.BreakType)** gibi diğer yöntemleri çağırdığınızda metin eklenecek dahili bir imleç bulunur. [DocumentBuilder](../../com.aspose.words/documentbuilder/) imlecini, çeşitli MoveToXXX yöntemlerini kullanarak bir belgedeki farklı bir konuma taşıyabilirsiniz.

Belgedeki mevcut konumdan itibaren eklenen tüm metne uygulanacak karakter biçimlendirmesini belirtmek için [getFont()](../../com.aspose.words/documentbuilder/\#getFont) özelliğini kullanın.

Mevcut ve eklenecek tüm paragraflar için paragraf biçimlendirmesini belirtmek üzere [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) özelliğini kullanın.

Mevcut bölüm ve eklenecek tüm bölümler için sayfa ve bölüm özelliklerini belirtmek üzere [getPageSetup()](../../com.aspose.words/documentbuilder/\#getPageSetup) özelliğini kullanın.

Tablo hücreleri ve satırları için biçimlendirme özelliklerini belirtmek üzere [getCellFormat()](../../com.aspose.words/documentbuilder/\#getCellFormat) ve [getRowFormat()](../../com.aspose.words/documentbuilder/\#getRowFormat) özelliklerini kullanın. Bir tablo oluşturmak için [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell) ve [endRow()](../../com.aspose.words/documentbuilder/\#endRow) yöntemlerini kullanın.

Belgedeki farklı bir konuma geçtiğinizde, mevcut konumdaki biçimlendirme özelliklerini yansıtmak için [getFont()](../../com.aspose.words/documentbuilder/\#getFont), [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) ve [getPageSetup()](../../com.aspose.words/documentbuilder/\#getPageSetup) özelliklerinin güncellendiğini unutmayın.

 **Examples:** 

DocumentBuilder kullanarak bir belgede üstbilgi ve altbilgi nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Özel kenarlıklarla bir tablo oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Bir belge oluşturucusunu kullanarak tablo oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start the table, then populate the first row with two cells.
 builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");

 // Call the builder's "EndRow" method to start a new row.
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateTable.docx");
 
```


[Document Builder Overview]: https://docs.aspose.com/words/java/document-builder-overview/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [DocumentBuilder()](#DocumentBuilder) | Bu sınıfın yeni bir örneğini başlatır. |
| [DocumentBuilder(DocumentBuilderOptions options)](#DocumentBuilder-com.aspose.words.DocumentBuilderOptions) | Bu sınıfın yeni bir örneğini başlatır. |
| [DocumentBuilder(Document doc)](#DocumentBuilder-com.aspose.words.Document) | Bu sınıfın yeni bir örneğini başlatır. |
| [DocumentBuilder(Document doc, DocumentBuilderOptions options)](#DocumentBuilder-com.aspose.words.Document-com.aspose.words.DocumentBuilderOptions) | Bu sınıfın yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [clearCellAttrs()](#clearCellAttrs) |  |
| [clearParaAttrs()](#clearParaAttrs) |  |
| [clearRowAttrs()](#clearRowAttrs) |  |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [deleteRow(int tableIndex, int rowIndex)](#deleteRow-int-int) | Bir tablodan satır siler. |
| [endBookmark(String bookmarkName)](#endBookmark-java.lang.String) | Belgedeki mevcut konumu bir yer imi sonu olarak işaretler. |
| [endColumnBookmark(String bookmarkName)](#endColumnBookmark-java.lang.String) | Belgedeki mevcut konumu bir sütun yer imi sonu olarak işaretler. |
| [endEditableRange()](#endEditableRange) | Belgedeki mevcut konumu düzenlenebilir bir aralık sonu olarak işaretler. |
| [endEditableRange(EditableRangeStart start)](#endEditableRange-com.aspose.words.EditableRangeStart) | Belgedeki mevcut konumu düzenlenebilir bir aralık sonu olarak işaretler. |
| [endRow()](#endRow) | Belgedeki bir tablo satırını sonlandırır. |
| [endTable()](#endTable) | Belgedeki bir tabloyu sonlandırır. |
| [fetchCellAttr(int key)](#fetchCellAttr-int) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int) |  |
| [getBold()](#getBold) | Yazı tipi kalın olarak biçimlendirilmişse True. |
| [getCellFormat()](#getCellFormat) | Mevcut tablo hücresi biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [getCurrentNode()](#getCurrentNode) | Bu DocumentBuilder içinde şu anda seçili olan düğümü alır. |
| [getCurrentParagraph()](#getCurrentParagraph) | Bu [DocumentBuilder](../../com.aspose.words/documentbuilder/) içinde şu anda seçili olan paragrafı alır. |
| [getCurrentSection()](#getCurrentSection) | Bu [DocumentBuilder](../../com.aspose.words/documentbuilder/) içinde şu anda seçili olan bölümü alır. |
| [getCurrentStory()](#getCurrentStory) | Bu [DocumentBuilder](../../com.aspose.words/documentbuilder/) içinde şu anda seçili olan hikayeyi alır. |
| [getCurrentStructuredDocumentTag()](#getCurrentStructuredDocumentTag) | Bu [DocumentBuilder](../../com.aspose.words/documentbuilder/) içinde şu anda seçili olan yapılandırılmış belge etiketini alır. |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int) |  |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int) |  |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Bu nesnenin bağlı olduğu [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) nesnesini alır. |
| [getFont()](#getFont) | Mevcut yazı tipi biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [getItalic()](#getItalic) | Yazı tipi italik olarak biçimlendirilmişse doğrudur. |
| [getListFormat()](#getListFormat) | Geçerli liste biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [getPageSetup()](#getPageSetup) | Geçerli sayfa ayarı ve bölüm özelliklerini temsil eden bir nesne döndürür. |
| [getParagraphFormat()](#getParagraphFormat) | Geçerli paragraf biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [getRowFormat()](#getRowFormat) | Geçerli tablo satırı biçimlendirme özelliklerini temsil eden bir nesne döndürür. |
| [getUnderline()](#getUnderline) | Geçerli yazı tipi için alt çizgi tipini alır/ayarlar. |
| [insertBreak(int breakType)](#insertBreak-int) |  |
| [insertCell()](#insertCell) | Belgeye bir tablo hücresi ekler. |
| [insertChart(int chartType, double width, double height)](#insertChart-int-double-double) |  |
| [insertChart(int chartType, double width, double height, int chartStyle)](#insertChart-int-double-double-int) |  |
| [insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertChart-int-int-double-int-double-double-double-int) |  |
| [insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType, int chartStyle)](#insertChart-int-int-double-int-double-double-double-int-int) |  |
| [insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-boolean-int) | Geçerli konuma bir onay kutusu form alanı ekler. |
| [insertCheckBox(String name, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-int) | Geçerli konuma bir onay kutusu form alanı ekler. |
| [insertComboBox(String name, String[] items, int selectedIndex)](#insertComboBox-java.lang.String-java.lang.String---int) | Geçerli konuma bir açılır kutu form alanı ekler. |
| [insertDocument(Document srcDoc, int importFormatMode)](#insertDocument-com.aspose.words.Document-int) |  |
| [insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#insertDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions) |  |
| [insertDocumentInline(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#insertDocumentInline-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions) |  |
| [insertField(int fieldType, boolean updateField)](#insertField-int-boolean) |  |
| [insertField(String fieldCode)](#insertField-java.lang.String) | Bir belgeye bir Word alanı ekler ve alan sonucunu günceller. |
| [insertField(String fieldCode, String fieldValue)](#insertField-java.lang.String-java.lang.String) | Bir belgeye bir Word alanı ekler ve alan sonucunu güncellemez. |
| [insertFootnote(int footnoteType, String footnoteText)](#insertFootnote-int-java.lang.String) |  |
| [insertFootnote(int footnoteType, String footnoteText, String referenceMark)](#insertFootnote-int-java.lang.String-java.lang.String) |  |
| [insertForms2OleControl(Forms2OleControl forms2OleControl)](#insertForms2OleControl-com.aspose.words.Forms2OleControl) | Geçerli konuma [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) nesnesi ekler.. |
| [insertGroupShape(ShapeBase[] shapes)](#insertGroupShape-com.aspose.words.ShapeBase...) | Parametre olarak verilen şekilleri yeni bir GroupShape düğümüne gruplar ve bu düğüm geçerli konuma eklenir. |
| [insertGroupShape(double left, double top, double width, double height, ShapeBase[] shapes)](#insertGroupShape-double-double-double-double-com.aspose.words.ShapeBase...) | Parametre olarak verilen şekilleri belirtilen boyutta yeni bir GroupShape düğümüne gruplar ve bu düğüm belirtilen konuma eklenir. |
| [insertHorizontalRule()](#insertHorizontalRule) | Belgeye yatay çizgi şekli ekler. |
| [insertHtml(String html)](#insertHtml-java.lang.String) | Belgeye bir HTML dizesi ekler. |
| [insertHtml(String html, boolean useBuilderFormatting)](#insertHtml-java.lang.String-boolean) | Belgeye bir HTML dizesi ekler. |
| [insertHtml(String html, int options)](#insertHtml-java.lang.String-int) |  |
| [insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)](#insertHyperlink-java.lang.String-java.lang.String-boolean) | Belgeye bir köprü ekler. |
| [insertImage(byte[] imageBytes)](#insertImage-byte) | Belgeye bir bayt dizisinden bir görüntü ekler. |
| [insertImage(byte[] imageBytes, double width, double height)](#insertImage-byte---double-double) | Belgeye bir bayt dizisinden satır içi bir görüntü ekler ve belirtilen boyuta ölçeklendirir. |
| [insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-byte---int-double-int-double-double-double-int) |  |
| [insertImage(BufferedImage image)](#insertImage-java.awt.image.BufferedImage) | Belgeye bir görüntü ekler. |
| [insertImage(BufferedImage image, double width, double height)](#insertImage-java.awt.image.BufferedImage-double-double) | Belgeye bir java.awt.image.BufferedImage nesnesinden satır içi bir görüntü ekler ve belirtilen boyuta ölçeklendirir. |
| [insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int) |  |
| [insertImage(InputStream stream)](#insertImage-java.io.InputStream) |  |
| [insertImage(InputStream stream, double width, double height)](#insertImage-java.io.InputStream-double-double) |  |
| [insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.io.InputStream-int-double-int-double-double-double-int) |  |
| [insertImage(String fileName)](#insertImage-java.lang.String) | Belgeye bir dosya veya URL'den bir görüntü ekler. |
| [insertImage(String fileName, double width, double height)](#insertImage-java.lang.String-double-double) | Belgeye bir dosya veya URL'den satır içi bir görüntü ekler ve belirtilen boyuta ölçeklendirir. |
| [insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.lang.String-int-double-int-double-double-double-int) |  |
| [insertNode(Node node)](#insertNode-com.aspose.words.Node) | İmlecin önüne bir düğüm ekler. |
| [insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation)](#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream) |  |
| [insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-boolean-boolean-java.io.InputStream) |  |
| [insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-java.lang.String-boolean-boolean-java.io.InputStream) |  |
| [insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.io.InputStream-java.lang.String-java.lang.String-java.lang.String) |  |
| [insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-boolean-java.lang.String-java.lang.String) | Belgeye gömülü veya bağlantılı bir OLE nesnesini simge olarak ekler. |
| [insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String) | Belgeye gömülü veya bağlantılı bir OLE nesnesini simge olarak ekler. |
| [insertOnlineVideo(String videoUrl, double width, double height)](#insertOnlineVideo-java.lang.String-double-double) | Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçeklendirir. |
| [insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int) |  |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double) | Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçeklendirir. |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int) |  |
| [insertParagraph()](#insertParagraph) | Belgeye bir paragraf sonu ekler. |
| [insertShape(int shapeType, double width, double height)](#insertShape-int-double-double) |  |
| [insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertShape-int-int-double-int-double-double-double-int) |  |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions)](#insertSignatureLine-com.aspose.words.SignatureLineOptions) | Geçerli konuma bir imza satırı ekler. |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)](#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int) |  |
| [insertStructuredDocumentTag(int type)](#insertStructuredDocumentTag-int) |  |
| [insertStyleSeparator()](#insertStyleSeparator) | Belgeye stil ayırıcı ekler. |
| [insertTableOfContents(String switches)](#insertTableOfContents-java.lang.String) | Belgeye bir TOC (içindekiler tablosu) alanı ekler. |
| [insertTextInput(String name, int type, String format, String fieldValue, int maxLength)](#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int) |  |
| [isAtEndOfParagraph()](#isAtEndOfParagraph) | İmleç geçerli paragrafın sonunda ise  true  döndürür. |
| [isAtEndOfStructuredDocumentTag()](#isAtEndOfStructuredDocumentTag) | İmleç yapılandırılmış belge etiketinin sonunda ise **true** döndürür. |
| [isAtStartOfParagraph()](#isAtStartOfParagraph) | İmleç geçerli paragrafın başında ise (imleçten önce metin yok)  true  döndürür. |
| [moveTo(Node node)](#moveTo-com.aspose.words.Node) | İmleci satır içi bir düğüme ya da bir paragrafın sonuna taşır. |
| [moveToBookmark(String bookmarkName)](#moveToBookmark-java.lang.String) | İmleci bir yer imine taşır. |
| [moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)](#moveToBookmark-java.lang.String-boolean-boolean) | İmleci daha yüksek hassasiyetle bir yer imine taşır. |
| [moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)](#moveToCell-int-int-int-int) | İmleci geçerli bölümdeki bir tablo hücresine taşır. |
| [moveToDocumentEnd()](#moveToDocumentEnd) | İmleci belgenin sonuna taşır. |
| [moveToDocumentStart()](#moveToDocumentStart) | İmleci belgenin başına taşır. |
| [moveToField(Field field, boolean isAfter)](#moveToField-com.aspose.words.Field-boolean) | İmleci belgede bir alana taşır. |
| [moveToHeaderFooter(int headerFooterType)](#moveToHeaderFooter-int) |  |
| [moveToMergeField(String fieldName)](#moveToMergeField-java.lang.String) | İmleci belirtilen birleştirme alanına taşır. |
| [moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)](#moveToMergeField-java.lang.String-boolean-boolean) | Birleştirme alanını belirtilen birleştirme alanına taşır. |
| [moveToParagraph(int paragraphIndex, int characterIndex)](#moveToParagraph-int-int) | İmleci geçerli bölümdeki bir paragrafına taşır. |
| [moveToSection(int sectionIndex)](#moveToSection-int) | İmleci belirtilen bölümdeki gövdenin başına taşır. |
| [moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)](#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int) | İmleci yapılandırılmış belge etiketine taşır. |
| [moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)](#moveToStructuredDocumentTag-int-int) | İmleci geçerli bölümdeki bir yapılandırılmış belge etiketine taşır. |
| [popFont()](#popFont) | Yığına daha önce kaydedilen karakter biçimlendirmesini alır. |
| [pushFont()](#pushFont) | Geçerli karakter biçimlendirmesini yığına kaydeder. |
| [removeParaAttr(int key)](#removeParaAttr-int) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs) |  |
| [setBold(boolean value)](#setBold-boolean) | Yazı tipi kalın olarak biçimlendirilmişse True. |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object) |  |
| [setDocument(Document value)](#setDocument-com.aspose.words.Document) | Bu nesnenin bağlı olduğu [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) nesnesini ayarlar. |
| [setItalic(boolean value)](#setItalic-boolean) | Yazı tipi italik olarak biçimlendirilmişse doğrudur. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object) |  |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object) |  |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setUnderline(int value)](#setUnderline-int) | Geçerli yazı tipi için alt çizgi tipini alır/ayarlar. |
| [startBookmark(String bookmarkName)](#startBookmark-java.lang.String) | Belgedeki geçerli konumu bir yer imi başlangıcı olarak işaretler. |
| [startColumnBookmark(String bookmarkName)](#startColumnBookmark-java.lang.String) | Belgedeki geçerli konumu bir sütun yer imi başlangıcı olarak işaretler. |
| [startEditableRange()](#startEditableRange) | Belge içinde geçerli konumu düzenlenebilir bir aralık başlangıcı olarak işaretler. |
| [startTable()](#startTable) | Belge içinde bir tablo başlatır. |
| [write(String text)](#write-java.lang.String) | Geçerli ekleme konumunda bir dizeyi belgeye ekler. |
| [writeln()](#writeln) | Belgeye bir paragraf sonu ekler. |
| [writeln(String text)](#writeln-java.lang.String) | Belgeye bir dize ve bir paragraf sonu ekler. |
### DocumentBuilder() {#DocumentBuilder}
```
public DocumentBuilder()
```


Bu sınıfın yeni bir örneğini başlatır.

 **Remarks:** 

Yeni bir [DocumentBuilder](../../com.aspose.words/documentbuilder/) nesnesi oluşturur ve yeni bir [Document](../../com.aspose.words/document/) nesnesine ekler.

 **Examples:** 

DocumentBuilder kullanarak biçimlendirilmiş metin eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify font formatting, then add text.
 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Courier New");
 font.setUnderline(Underline.DASH);

 builder.write("Hello world!");
 
```

### DocumentBuilder(DocumentBuilderOptions options) {#DocumentBuilder-com.aspose.words.DocumentBuilderOptions}
```
public DocumentBuilder(DocumentBuilderOptions options)
```


Bu sınıfın yeni bir örneğini başlatır.

 **Remarks:** 

Yeni bir [DocumentBuilder](../../com.aspose.words/documentbuilder/) nesnesi oluşturur ve yeni bir [Document](../../com.aspose.words/document/) nesnesine ekler. Ek belge oluşturma seçenekleri belirtilebilir.

 **Examples:** 

Tablo biçimlendirmesini sonrasındaki içerik için nasıl yok sayacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
 builderOptions.setContextTableFormatting(true);
 DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

 // Adds content before the table.
 // Default font size is 12.
 builder.writeln("Font size 12 here.");
 builder.startTable();
 builder.insertCell();
 // Changes the font size inside the table.
 builder.getFont().setSize(5.0);
 builder.write("Font size 5 here");
 builder.insertCell();
 builder.write("Font size 5 here");
 builder.endRow();
 builder.endTable();

 // If ContextTableFormatting is true, then table formatting isn't applied to the content after.
 // If ContextTableFormatting is false, then table formatting is applied to the content after.
 builder.writeln("Font size 12 here.");

 doc.save(getArtifactsDir() + "Table.ContextTableFormatting.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| options | [DocumentBuilderOptions](../../com.aspose.words/documentbuilderoptions/) |  |

### DocumentBuilder(Document doc) {#DocumentBuilder-com.aspose.words.Document}
```
public DocumentBuilder(Document doc)
```


Bu sınıfın yeni bir örneğini başlatır.

 **Remarks:** 

Yeni bir [DocumentBuilder](../../com.aspose.words/documentbuilder/) nesnesi oluşturur, belirtilen [Document](../../com.aspose.words/document/) nesnesine ekler. İmleç belgenin başına konumlandırılır.

 **Examples:** 

DocumentBuilder kullanarak bir belgede üstbilgi ve altbilgi nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Başlık stillerini giriş olarak kullanarak bir belgeye İçindekiler Tablosu (TOC) nasıl eklenir gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents for the first page of the document.
 // Configure the table to pick up paragraphs with headings of levels 1 to 3.
 // Also, set its entries to be hyperlinks that will take us
 // to the location of the heading when left-clicked in Microsoft Word.
 builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Populate the table of contents by adding paragraphs with heading styles.
 // Each such heading with a level between 1 and 3 will create an entry in the table.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 2");
 builder.writeln("Heading 3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);
 builder.writeln("Heading 3.1.1");
 builder.writeln("Heading 3.1.2");
 builder.writeln("Heading 3.1.3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);
 builder.writeln("Heading 3.1.3.1");
 builder.writeln("Heading 3.1.3.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.2");
 builder.writeln("Heading 3.3");

 // A table of contents is a field of a type that needs to be updated to show an up-to-date result.
 doc.updateFields();
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertToc.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | Eklenilecek [Document](../../com.aspose.words/document/) nesnesi. |

### DocumentBuilder(Document doc, DocumentBuilderOptions options) {#DocumentBuilder-com.aspose.words.Document-com.aspose.words.DocumentBuilderOptions}
```
public DocumentBuilder(Document doc, DocumentBuilderOptions options)
```


Bu sınıfın yeni bir örneğini başlatır.

 **Remarks:** 

Yeni bir [DocumentBuilder](../../com.aspose.words/documentbuilder/) nesnesi oluşturur, belirtilen [Document](../../com.aspose.words/document/) nesnesine ekler. İmleç belgenin başına konumlandırılır.

 **Examples:** 

Tablo biçimlendirmesini sonrasındaki içerik için nasıl yok sayacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
 builderOptions.setContextTableFormatting(true);
 DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

 // Adds content before the table.
 // Default font size is 12.
 builder.writeln("Font size 12 here.");
 builder.startTable();
 builder.insertCell();
 // Changes the font size inside the table.
 builder.getFont().setSize(5.0);
 builder.write("Font size 5 here");
 builder.insertCell();
 builder.write("Font size 5 here");
 builder.endRow();
 builder.endTable();

 // If ContextTableFormatting is true, then table formatting isn't applied to the content after.
 // If ContextTableFormatting is false, then table formatting is applied to the content after.
 builder.writeln("Font size 12 here.");

 doc.save(getArtifactsDir() + "Table.ContextTableFormatting.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | Eklenilecek [Document](../../com.aspose.words/document/) nesnesi. |
| options | [DocumentBuilderOptions](../../com.aspose.words/documentbuilderoptions/) | Belge oluşturma süreci için ek seçenekler. |

### clearCellAttrs() {#clearCellAttrs}
```
public void clearCellAttrs()
```




### clearParaAttrs() {#clearParaAttrs}
```
public void clearParaAttrs()
```




### clearRowAttrs() {#clearRowAttrs}
```
public void clearRowAttrs()
```




### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### deleteRow(int tableIndex, int rowIndex) {#deleteRow-int-int}
```
public Row deleteRow(int tableIndex, int rowIndex)
```


Bir tablodan satır siler.

 **Remarks:** 

İmleç silinen satırın içinde ise, imleç bir sonraki satıra ya da tablodan sonraki paragrafın başına taşınır.

Sadece bir satır içeren bir tablodan bir satır silerseniz, tüm tablo silinir.

Dizin parametreleri için, dizin 0'a eşit veya büyük olduğunda, 0 ilk öğe olmak üzere baştan bir dizin belirtir. Dizin 0'dan küçük olduğunda, -1 son öğe olmak üzere sondan bir dizin belirtir.

 **Examples:** 

Bir tablodan satır silmenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.write("Row 2, cell 2.");
 builder.endTable();

 Assert.assertEquals(2, table.getRows().getCount());

 // Delete the first row of the first table in the document.
 builder.deleteRow(0, 0);

 Assert.assertEquals(1, table.getRows().getCount());
 Assert.assertEquals("Row 2, cell 1.Row 2, cell 2.", table.getText().trim());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableIndex | int | Tablonun dizini. |
| rowIndex | int | Tablodaki satırın dizini. |

**Returns:**
[Row](../../com.aspose.words/row/) - The row node that was just removed.
### endBookmark(String bookmarkName) {#endBookmark-java.lang.String}
```
public BookmarkEnd endBookmark(String bookmarkName)
```


Belgedeki mevcut konumu bir yer imi sonu olarak işaretler.

 **Remarks:** 

Bir belgede yer imleri çakışabilir ve herhangi bir aralığı kapsayabilir. Geçerli bir yer imi oluşturmak için aynı bookmarkName parametresiyle hem [startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startBookmark-java.lang.String) hem de [endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endBookmark-java.lang.String) metodlarını çağırmanız gerekir.

Kötü biçimlendirilmiş yer imleri veya aynı ada sahip yer imleri belge kaydedildiğinde yok sayılacaktır.

 **Examples:** 

Bir yer imi oluşturmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A valid bookmark needs to have document body text enclosed by
 // BookmarkStart and BookmarkEnd nodes created with a matching bookmark name.
 builder.startBookmark("MyBookmark");
 builder.writeln("Hello world!");
 builder.endBookmark("MyBookmark");

 Assert.assertEquals(1, doc.getRange().getBookmarks().getCount());
 Assert.assertEquals("MyBookmark", doc.getRange().getBookmarks().get(0).getName());
 Assert.assertEquals("Hello world!", doc.getRange().getBookmarks().get(0).getText().trim());
 
```

Yerel bir yer imine referans veren bir köprü eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startBookmark("Bookmark1");
 builder.write("Bookmarked text. ");
 builder.endBookmark("Bookmark1");
 builder.writeln("Text outside of the bookmark.");

 // Insert a HYPERLINK field that links to the bookmark. We can pass field switches
 // to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 FieldHyperlink hyperlink = (FieldHyperlink)builder.insertHyperlink("Link to Bookmark1", "Bookmark1", true);
 hyperlink.setScreenTip("Hyperlink Tip");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| bookmarkName | java.lang.String | Yer iminin adı. |

**Returns:**
[BookmarkEnd](../../com.aspose.words/bookmarkend/) - The bookmark end node that was just created.
### endColumnBookmark(String bookmarkName) {#endColumnBookmark-java.lang.String}
```
public BookmarkEnd endColumnBookmark(String bookmarkName)
```


Belgedeki geçerli konumu bir sütun yer imi sonu olarak işaretler. Konum bir tablo hücresi içinde olmalıdır.

 **Remarks:** 

Bir sütun yer imi, satır aralığında bir veya daha fazla sütunu kapsar. Geçerli bir yer imi oluşturmak için aynı bookmarkName parametresiyle hem [startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startColumnBookmark-java.lang.String) hem de [endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endColumnBookmark-java.lang.String) metodlarını çağırmanız gerekir.

Kötü biçimlendirilmiş yer imleri veya aynı ada sahip yer imleri belge kaydedildiğinde yok sayılacaktır.

Eklemiş olduğunuz [BookmarkEnd](../../com.aspose.words/bookmarkend/) düğümünün gerçek konumu, mevcut belge oluşturucu konumundan farklı olabilir.

 **Examples:** 

Bir sütun yer işareti oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 builder.insertCell();
 // Cells 1,2,4,5 will be bookmarked.
 builder.startColumnBookmark("MyBookmark_1");
 // Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.
 builder.startColumnBookmark("MyBookmark_1");
 builder.startColumnBookmark("BadStartBookmark");
 builder.write("Cell 1");

 builder.insertCell();
 builder.write("Cell 2");

 builder.insertCell();
 builder.write("Cell 3");

 builder.endRow();

 builder.insertCell();
 builder.write("Cell 4");

 builder.insertCell();
 builder.write("Cell 5");
 builder.endColumnBookmark("MyBookmark_1");
 builder.endColumnBookmark("MyBookmark_1");

 builder.insertCell();
 builder.write("Cell 6");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "Bookmarks.CreateColumnBookmark.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| bookmarkName | java.lang.String | Yer iminin adı. |

**Returns:**
[BookmarkEnd](../../com.aspose.words/bookmarkend/) - The bookmark end node that was just created.
### endEditableRange() {#endEditableRange}
```
public EditableRangeEnd endEditableRange()
```


Belgedeki mevcut konumu düzenlenebilir bir aralık sonu olarak işaretler.

 **Remarks:** 

Bir belgede düzenlenebilir aralık çakışabilir ve herhangi bir aralığı kapsayabilir. Geçerli bir düzenlenebilir aralık oluşturmak için hem [startEditableRange()](../../com.aspose.words/documentbuilder/\#startEditableRange) hem de [endEditableRange()](../../com.aspose.words/documentbuilder/\#endEditableRange) ya da [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder/\#endEditableRange-com.aspose.words.EditableRangeStart) yöntemlerini çağırmanız gerekir.

Kötü biçimlendirilmiş düzenlenebilir aralık, belge kaydedildiğinde yok sayılacaktır.

 **Examples:** 

Düzenlenebilir bir aralıkla nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
         " we cannot edit this paragraph without the password.");

 // Editable ranges allow us to leave parts of protected documents open for editing.
 EditableRangeStart editableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph is inside an editable range, and can be edited.");
 EditableRangeEnd editableRangeEnd = builder.endEditableRange();

 // A well-formed editable range has a start node, and end node.
 // These nodes have matching IDs and encompass editable nodes.
 EditableRange editableRange = editableRangeStart.getEditableRange();

 Assert.assertEquals(editableRangeStart.getId(), editableRange.getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getId());

 // Different parts of the editable range link to each other.
 Assert.assertEquals(editableRangeStart.getId(), editableRange.getEditableRangeStart().getId());
 Assert.assertEquals(editableRangeStart.getId(), editableRangeEnd.getEditableRangeStart().getId());
 Assert.assertEquals(editableRange.getId(), editableRangeStart.getEditableRange().getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getEditableRangeEnd().getId());

 // We can access the node types of each part like this. The editable range itself is not a node,
 // but an entity which consists of a start, an end, and their enclosed contents.
 Assert.assertEquals(NodeType.EDITABLE_RANGE_START, editableRangeStart.getNodeType());
 Assert.assertEquals(NodeType.EDITABLE_RANGE_END, editableRangeEnd.getNodeType());

 builder.writeln("This paragraph is outside the editable range, and cannot be edited.");

 doc.save(getArtifactsDir() + "EditableRange.CreateAndRemove.docx");

 // Remove an editable range. All the nodes that were inside the range will remain intact.
 editableRange.remove();
 
```

**Returns:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend/) - The editable range end node that was just created.
### endEditableRange(EditableRangeStart start) {#endEditableRange-com.aspose.words.EditableRangeStart}
```
public EditableRangeEnd endEditableRange(EditableRangeStart start)
```


Belgedeki mevcut konumu düzenlenebilir bir aralık sonu olarak işaretler.

 **Remarks:** 

İç içe düzenlenebilir aralıklar oluştururken bu aşırı yüklemeyi kullanın.

Bir belgede düzenlenebilir aralık çakışabilir ve herhangi bir aralığı kapsayabilir. Geçerli bir düzenlenebilir aralık oluşturmak için hem [startEditableRange()](../../com.aspose.words/documentbuilder/\#startEditableRange) hem de [endEditableRange()](../../com.aspose.words/documentbuilder/\#endEditableRange) ya da [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder/\#endEditableRange-com.aspose.words.EditableRangeStart) yöntemlerini çağırmanız gerekir.

Kötü biçimlendirilmiş düzenlenebilir aralık, belge kaydedildiğinde yok sayılacaktır.

 **Examples:** 

İç içe düzenlenebilir aralıkların nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only, " +
         "we cannot edit this paragraph without the password.");

 // Create two nested editable ranges.
 EditableRangeStart outerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 EditableRangeStart innerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

 // Currently, the document builder's node insertion cursor is in more than one ongoing editable range.
 // When we want to end an editable range in this situation,
 // we need to specify which of the ranges we wish to end by passing its EditableRangeStart node.
 builder.endEditableRange(innerEditableRangeStart);

 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 builder.endEditableRange(outerEditableRangeStart);

 builder.writeln("This paragraph is outside any editable ranges, and cannot be edited.");

 // If a region of text has two overlapping editable ranges with specified groups,
 // the combined group of users excluded by both groups are prevented from editing it.
 outerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.EVERYONE);
 innerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.CONTRIBUTORS);

 doc.save(getArtifactsDir() + "EditableRange.Nested.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| start | [EditableRangeStart](../../com.aspose.words/editablerangestart/) | Bu düzenlenebilir aralık başlangıcı. |

**Returns:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend/) - The editable range end node that was just created.
### endRow() {#endRow}
```
public Row endRow()
```


Belgedeki bir tablo satırını sonlandırır.

 **Remarks:** 

[endRow()](../../com.aspose.words/documentbuilder/\#endRow) metodunu bir tablo satırını sonlandırmak için çağırın. Ardından hemen [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell) metodunu çağırırsanız, tablo yeni bir satırda devam eder.

Satır biçimlendirmesini belirtmek için [getRowFormat()](../../com.aspose.words/documentbuilder/\#getRowFormat) özelliğini kullanın.

 **Examples:** 

Tablo hücrelerini dikey olarak birleştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a cell into the first column of the first row.
 // This cell will be the first in a range of vertically merged cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.FIRST);
 builder.write("Text in merged cells.");

 // Insert a cell into the second column of the first row, then end the row.
 // Also, configure the builder to disable vertical merging in created cells.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();

 // Insert a cell into the first column of the second row.
 // Instead of adding text contents, we will merge this cell with the first cell that we added directly above.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.PREVIOUS);

 // Insert another independent cell in the second column of the second row.
 builder.insertCell();
 builder.getCellFormat().setVerticalMerge(CellMerge.NONE);
 builder.write("Text in unmerged cell.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "CellFormat.VerticalMerge.docx");
 
```

Özel kenarlıklarla bir tablo oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Biçimlendirilmiş 2x2 bir tablo nasıl oluşturulur gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Returns:**
[Row](../../com.aspose.words/row/) - The row node that was just finished.
### endTable() {#endTable}
```
public Table endTable()
```


Belgedeki bir tabloyu sonlandırır.

 **Remarks:** 

Bu yöntem, [endRow()](../../com.aspose.words/documentbuilder/\#endRow) çağrıldıktan sonra yalnızca bir kez çağrılmalıdır. Çağrıldığında, [endTable()](../../com.aspose.words/documentbuilder/\#endTable) imleci mevcut hücreden çıkararak tabloyun hemen sonrasına konumlandırır.

 **Examples:** 

Özel kenarlıklarla bir tablo oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Biçimlendirilmiş 2x2 bir tablo nasıl oluşturulur gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

Bir belge oluşturucu ile hücreleri biçimlendirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
[Table](../../com.aspose.words/table/) - The table node that was just finished.
### fetchCellAttr(int key) {#fetchCellAttr-int}
```
public Object fetchCellAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int}
```
public Object fetchInheritedCellAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int}
```
public Object fetchInheritedRowAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int}
```
public Object fetchRowAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getBold() {#getBold}
```
public boolean getBold()
```


Yazı tipi kalın olarak biçimlendirilmişse True.

 **Examples:** 

Posta birleştirme yerine bir belge oluşturucu kullanarak MERGEFIELD'leri veri ile doldurmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getCellFormat() {#getCellFormat}
```
public CellFormat getCellFormat()
```


Mevcut tablo hücresi biçimlendirme özelliklerini temsil eden bir nesne döndürür.

 **Examples:** 

Özel kenarlıklarla bir tablo oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Biçimlendirilmiş 2x2 bir tablo nasıl oluşturulur gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

Bir belge oluşturucu ile hücreleri biçimlendirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
[CellFormat](../../com.aspose.words/cellformat/) - An object that represents current table cell formatting properties.
### getCurrentNode() {#getCurrentNode}
```
public Node getCurrentNode()
```


Bu DocumentBuilder içinde şu anda seçili olan düğümü alır.

 **Remarks:** 

[getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode) is a cursor of [DocumentBuilder](../../com.aspose.words/documentbuilder/) and points to a [Node](../../com.aspose.words/node/) that is a direct child of a [Paragraph](../../com.aspose.words/paragraph/). Any insert operations you perform using [DocumentBuilder](../../com.aspose.words/documentbuilder/) will insert before the [getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode).

Mevcut paragraf boş olduğunda veya imleç bir paragrafın ya da yapılandırılmış belge etiketinin sonundan hemen önce konumlandığında, [getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode) null döndürür.

 **Examples:** 

Bir belge oluşturucunun imlecini belgede farklı düğümlere taşımayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node that is currently selected in this DocumentBuilder.
### getCurrentParagraph() {#getCurrentParagraph}
```
public Paragraph getCurrentParagraph()
```


Bu [DocumentBuilder](../../com.aspose.words/documentbuilder/) içinde şu anda seçili olan paragrafı alır.

 **Remarks:** 

[getCurrentNode()](../../com.aspose.words/documentbuilder/\#getCurrentNode)

 **Examples:** 

Bir belge oluşturucunun imlecini belgede farklı düğümlere taşımayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The paragraph that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getCurrentSection() {#getCurrentSection}
```
public Section getCurrentSection()
```


Bu [DocumentBuilder](../../com.aspose.words/documentbuilder/) içinde şu anda seçili olan bölümü alır.

 **Examples:** 

Yüzen bir görüntünün nasıl ekleneceğini ve konumunun ve boyutunun nasıl belirtileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);

 // Configure the shape's "RelativeHorizontalPosition" property to treat the value of the "Left" property
 // as the shape's horizontal distance, in points, from the left side of the page.
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);

 // Set the shape's horizontal distance from the left side of the page to 100.
 shape.setLeft(100.0);

 // Use the "RelativeVerticalPosition" property in a similar way to position the shape 80pt below the top of the page.
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setTop(80.0);

 // Set the shape's height, which will automatically scale the width to preserve dimensions.
 shape.setHeight(125.0);

 Assert.assertEquals(125.0d, shape.getWidth());

 // The "Bottom" and "Right" properties contain the bottom and right edges of the image.
 Assert.assertEquals(shape.getTop() + shape.getHeight(), shape.getBottom());
 Assert.assertEquals(shape.getLeft() + shape.getWidth(), shape.getRight());

 doc.save(getArtifactsDir() + "Image.CreateFloatingPositionSize.docx");
 
```

**Returns:**
[Section](../../com.aspose.words/section/) - The section that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getCurrentStory() {#getCurrentStory}
```
public Story getCurrentStory()
```


Bu [DocumentBuilder](../../com.aspose.words/documentbuilder/) içinde şu anda seçili olan hikayeyi alır.

 **Examples:** 

Bir belge oluşturucunun mevcut hikayesiyle çalışmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A Story is a type of node that has child Paragraph nodes, such as a Body.
 Assert.assertEquals(builder.getCurrentStory(), doc.getFirstSection().getBody());
 Assert.assertEquals(builder.getCurrentStory(), builder.getCurrentParagraph().getParentNode());
 Assert.assertEquals(StoryType.MAIN_TEXT, builder.getCurrentStory().getStoryType());

 builder.getCurrentStory().appendParagraph("Text added to current Story.");

 // A Story can also contain tables.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1");
 builder.insertCell();
 builder.write("Row 1, cell 2");
 builder.endTable();

 Assert.assertTrue(builder.getCurrentStory().getTables().contains(table));
 
```

**Returns:**
[Story](../../com.aspose.words/story/) - The story that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getCurrentStructuredDocumentTag() {#getCurrentStructuredDocumentTag}
```
public StructuredDocumentTag getCurrentStructuredDocumentTag()
```


Bu [DocumentBuilder](../../com.aspose.words/documentbuilder/) içinde şu anda seçili olan yapılandırılmış belge etiketini alır.

 **Examples:** 

DocumentBuilder'ın imlecini yapılandırılmış belge etiketi içinde taşımayı gösterir.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Returns:**
[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) - The structured document tag that is currently selected in this [DocumentBuilder](../../com.aspose.words/documentbuilder/).
### getDirectCellAttr(int key) {#getDirectCellAttr-int}
```
public Object getDirectCellAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key) {#getDirectParaAttr-int}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDirectRowAttr(int key) {#getDirectRowAttr-int}
```
public Object getDirectRowAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int fontAttr)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontAttr | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public Document getDocument()
```


Bu nesnenin bağlı olduğu [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) nesnesini alır.

 **Examples:** 

Bir belgede bölümlere sayfa ayarı seçeneklerini uygulama ve geri alma işlemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Returns:**
[Document](../../com.aspose.words/document/) - The [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) object that this object is attached to.
### getFont() {#getFont}
```
public Font getFont()
```


Mevcut yazı tipi biçimlendirme özelliklerini temsil eden bir nesne döndürür.

 **Remarks:** 

Yazı tipi biçimlendirme özelliklerine erişmek ve değiştirmek için [getFont()](../../com.aspose.words/documentbuilder/\#getFont) kullanın.

Metin eklemeden önce yazı tipi biçimlendirmesini belirtin.

 **Examples:** 

Bir dizeyi kenarlıkla çevreleyerek belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

DocumentBuilder kullanarak biçimlendirilmiş bir tablo nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 table.setLeftIndent(20.0);

 // Set some formatting options for text and table appearance.
 builder.getRowFormat().setHeight(40.0);
 builder.getRowFormat().setHeightRule(HeightRule.AT_LEAST);
 builder.getCellFormat().getShading().setBackgroundPatternColor(new Color((198), (217), (241)));

 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getFont().setSize(16.0);
 builder.getFont().setName("Arial");
 builder.getFont().setBold(true);

 // Configuring the formatting options in a document builder will apply them
 // to the current cell/row its cursor is in,
 // as well as any new cells and rows created using that builder.
 builder.write("Header Row,\n Cell 1");
 builder.insertCell();
 builder.write("Header Row,\n Cell 2");
 builder.insertCell();
 builder.write("Header Row,\n Cell 3");
 builder.endRow();

 // Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
 // The builder will not apply these to the first row already created so that it will stand out as a header row.
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.WHITE);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getRowFormat().setHeight(30.0);
 builder.getRowFormat().setHeightRule(HeightRule.AUTO);
 builder.insertCell();
 builder.getFont().setSize(12.0);
 builder.getFont().setBold(false);

 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");
 builder.insertCell();
 builder.write("Row 1, Cell 3.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.insertCell();
 builder.write("Row 2, Cell 3.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateFormattedTable.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - An object that represents current font formatting properties.
### getItalic() {#getItalic}
```
public boolean getItalic()
```


Yazı tipi italik olarak biçimlendirilmişse doğrudur.

 **Examples:** 

Posta birleştirme yerine bir belge oluşturucu kullanarak MERGEFIELD'leri veri ile doldurmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getListFormat() {#getListFormat}
```
public ListFormat getListFormat()
```


Geçerli liste biçimlendirme özelliklerini temsil eden bir nesne döndürür.

 **Examples:** 

Madde işaretli ve numaralı listeler oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Aspose.Words main advantages are:");

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Below are two types of lists that we can create with a document builder.
 // 1 -  A bulleted list:
 // This list will apply an indent and a bullet symbol ("\u2022") before each paragraph.
 builder.getListFormat().applyBulletDefault();
 builder.writeln("Great performance");
 builder.writeln("High reliability");
 builder.writeln("Quality code and working");
 builder.writeln("Wide variety of features");
 builder.writeln("Easy to understand API");

 // End the bulleted list.
 builder.getListFormat().removeNumbers();

 builder.insertBreak(BreakType.PARAGRAPH_BREAK);
 builder.writeln("Aspose.Words allows:");

 // 2 -  A numbered list:
 // Numbered lists create a logical order for their paragraphs by numbering each item.
 builder.getListFormat().applyNumberDefault();

 // This paragraph is the first item. The first item of a numbered list will have a "1." as its list item symbol.
 builder.writeln("Opening documents from different formats:");

 Assert.assertEquals(0, builder.getListFormat().getListLevelNumber());

 // Call the "ListIndent" method to increase the current list level,
 // which will start a new self-contained list, with a deeper indent, at the current item of the first list level.
 builder.getListFormat().listIndent();

 Assert.assertEquals(1, builder.getListFormat().getListLevelNumber());

 // These are the first three list items of the second list level, which will maintain a count
 // independent of the count of the first list level. According to the current list format,
 // they will have symbols of "a.", "b.", and "c.".
 builder.writeln("DOC");
 builder.writeln("PDF");
 builder.writeln("HTML");

 // Call the "ListOutdent" method to return to the previous list level.
 builder.getListFormat().listOutdent();

 Assert.assertEquals(0, builder.getListFormat().getListLevelNumber());

 // These two paragraphs will continue the count of the first list level.
 // These items will have symbols of "2.", and "3."
 builder.writeln("Processing documents");
 builder.writeln("Saving documents in different formats:");

 // If we increase the list level to a level that we have added items to previously,
 // the nested list will be separate from the previous, and its numbering will start from the beginning.
 // These list items will have symbols of "a.", "b.", "c.", "d.", and "e".
 builder.getListFormat().listIndent();
 builder.writeln("DOC");
 builder.writeln("PDF");
 builder.writeln("HTML");
 builder.writeln("MHTML");
 builder.writeln("Plain text");

 // Outdent the list level again.
 builder.getListFormat().listOutdent();
 builder.writeln("Doing many other things!");

 // End the numbered list.
 builder.getListFormat().removeNumbers();

 doc.save(getArtifactsDir() + "Lists.ApplyDefaultBulletsAndNumbers.docx");
 
```

**Returns:**
[ListFormat](../../com.aspose.words/listformat/) - An object that represents current list formatting properties.
### getPageSetup() {#getPageSetup}
```
public PageSetup getPageSetup()
```


Geçerli sayfa ayarı ve bölüm özelliklerini temsil eden bir nesne döndürür.

 **Examples:** 

Bir belgede bölümlere sayfa ayarı seçeneklerini uygulama ve geri alma işlemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Returns:**
[PageSetup](../../com.aspose.words/pagesetup/) - An object that represents current page setup and section properties.
### getParagraphFormat() {#getParagraphFormat}
```
public ParagraphFormat getParagraphFormat()
```


Geçerli paragraf biçimlendirme özelliklerini temsil eden bir nesne döndürür.

 **Examples:** 

DocumentBuilder kullanarak biçimlendirilmiş bir tablo nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 table.setLeftIndent(20.0);

 // Set some formatting options for text and table appearance.
 builder.getRowFormat().setHeight(40.0);
 builder.getRowFormat().setHeightRule(HeightRule.AT_LEAST);
 builder.getCellFormat().getShading().setBackgroundPatternColor(new Color((198), (217), (241)));

 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.getFont().setSize(16.0);
 builder.getFont().setName("Arial");
 builder.getFont().setBold(true);

 // Configuring the formatting options in a document builder will apply them
 // to the current cell/row its cursor is in,
 // as well as any new cells and rows created using that builder.
 builder.write("Header Row,\n Cell 1");
 builder.insertCell();
 builder.write("Header Row,\n Cell 2");
 builder.insertCell();
 builder.write("Header Row,\n Cell 3");
 builder.endRow();

 // Reconfigure the builder's formatting objects for new rows and cells that we are about to make.
 // The builder will not apply these to the first row already created so that it will stand out as a header row.
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.WHITE);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getRowFormat().setHeight(30.0);
 builder.getRowFormat().setHeightRule(HeightRule.AUTO);
 builder.insertCell();
 builder.getFont().setSize(12.0);
 builder.getFont().setBold(false);

 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");
 builder.insertCell();
 builder.write("Row 1, Cell 3.");
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.insertCell();
 builder.write("Row 2, Cell 3.");
 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateFormattedTable.docx");
 
```

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - An object that represents current paragraph formatting properties.
### getRowFormat() {#getRowFormat}
```
public RowFormat getRowFormat()
```


Geçerli tablo satırı biçimlendirme özelliklerini temsil eden bir nesne döndürür.

 **Examples:** 

Özel kenarlıklarla bir tablo oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Biçimlendirilmiş 2x2 bir tablo nasıl oluşturulur gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

DocumentBuilder ile satırların nasıl biçimlendirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Start a second row, and then configure its height. The builder will apply these settings to
 // its current row, as well as any new rows it creates afterwards.
 builder.endRow();

 RowFormat rowFormat = builder.getRowFormat();
 rowFormat.setHeight(100.0);
 rowFormat.setHeightRule(HeightRule.EXACTLY);

 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.endTable();

 // The first row was unaffected by the padding reconfiguration and still holds the default values.
 Assert.assertEquals(0.0d, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());

 Assert.assertEquals(100.0d, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```

**Returns:**
[RowFormat](../../com.aspose.words/rowformat/) - An object that represents current table row formatting properties.
### getUnderline() {#getUnderline}
```
public int getUnderline()
```


Geçerli yazı tipi için alt çizgi tipini alır/ayarlar.

 **Examples:** 

Bir belge oluşturucu tarafından eklenen metni biçimlendirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.setUnderline(Underline.DASH);
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setSize(32.0);

 // The builder applies formatting to its current paragraph and any new text added by it afterward.
 builder.writeln("Large, blue, and underlined text.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertUnderline.docx");
 
```

**Returns:**
int - İlgili  int  değeri. Döndürülen değer, [Underline](../../com.aspose.words/underline/) sabitlerinden biridir.
### insertBreak(int breakType) {#insertBreak-int}
```
public void insertBreak(int breakType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| breakType | int |  |

### insertCell() {#insertCell}
```
public Cell insertCell()
```


Belgeye bir tablo hücresi ekler.

 **Remarks:** 

Bir tablo başlatmak için sadece [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell) metodunu çağırın. Bundan sonra, [DocumentBuilder](../../com.aspose.words/documentbuilder/) sınıfının diğer yöntemlerini kullanarak eklediğiniz tüm içerik mevcut hücreye eklenecektir.

Aynı satırda yeni bir hücre başlatmak için [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell) metodunu tekrar çağırın.

Bir tablo satırını sonlandırmak için [endRow()](../../com.aspose.words/documentbuilder/\#endRow) metodunu çağırın.

Hücre biçimlendirmesini belirtmek için [getCellFormat()](../../com.aspose.words/documentbuilder/\#getCellFormat) özelliğini kullanın.

 **Examples:** 

Özel kenarlıklarla bir tablo oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Bir belge oluşturucusunu kullanarak tablo oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start the table, then populate the first row with two cells.
 builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");

 // Call the builder's "EndRow" method to start a new row.
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateTable.docx");
 
```

**Returns:**
[Cell](../../com.aspose.words/cell/) - The cell node that was just inserted.
### insertChart(int chartType, double width, double height) {#insertChart-int-double-double}
```
public Shape insertChart(int chartType, double width, double height)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartType | int |  |
| genişlik | double |  |
| yükseklik | double |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertChart(int chartType, double width, double height, int chartStyle) {#insertChart-int-double-double-int}
```
public Shape insertChart(int chartType, double width, double height, int chartStyle)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartType | int |  |
| genişlik | double |  |
| yükseklik | double |  |
| chartStyle | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertChart-int-int-double-int-double-double-double-int}
```
public Shape insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartType | int |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| genişlik | double |  |
| yükseklik | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType, int chartStyle) {#insertChart-int-int-double-int-double-double-double-int-int}
```
public Shape insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType, int chartStyle)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartType | int |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| genişlik | double |  |
| yükseklik | double |  |
| wrapType | int |  |
| chartStyle | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-boolean-int}
```
public FormField insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)
```


Geçerli konuma bir onay kutusu form alanı ekler.

 **Remarks:** 

Form alanı için bir ad belirtirseniz, aynı adla bir yer imi otomatik olarak oluşturulur.

 **Examples:** 

Belgeye onay kutuları eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert checkboxes of varying sizes and default checked statuses.
 builder.write("Unchecked check box of a default size: ");
 builder.insertCheckBox("", false, false, 0);
 builder.insertParagraph();

 builder.write("Large checked check box: ");
 builder.insertCheckBox("CheckBox_Default", true, true, 50);
 builder.insertParagraph();

 // Form fields have a name length limit of 20 characters.
 builder.write("Very large checked check box: ");
 builder.insertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

 Assert.assertEquals("CheckBox_OnlyChecked", doc.getRange().getFormFields().get(2).getName());

 // We can interact with these check boxes in Microsoft Word by double clicking them.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCheckBox.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Form alanının adı. Boş bir dize olabilir. 20 karakterden uzun değerler kırpılacaktır. |
| defaultValue | boolean | Onay kutusu form alanının varsayılan değeri. |
| checkedValue | boolean | Onay kutusu form alanının mevcut işaretlenme durumu. |
| size | int | Onay kutusunun boyutunu puan cinsinden belirtir. MS Word'ün onay kutusunun boyutunu otomatik olarak hesaplaması için 0 girin. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - The form field node that was just inserted.
### insertCheckBox(String name, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-int}
```
public FormField insertCheckBox(String name, boolean checkedValue, int size)
```


Geçerli konuma bir onay kutusu form alanı ekler.

 **Remarks:** 

Form alanı için bir ad belirtirseniz, aynı adla bir yer imi otomatik olarak oluşturulur.

 **Examples:** 

Belgeye onay kutuları eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert checkboxes of varying sizes and default checked statuses.
 builder.write("Unchecked check box of a default size: ");
 builder.insertCheckBox("", false, false, 0);
 builder.insertParagraph();

 builder.write("Large checked check box: ");
 builder.insertCheckBox("CheckBox_Default", true, true, 50);
 builder.insertParagraph();

 // Form fields have a name length limit of 20 characters.
 builder.write("Very large checked check box: ");
 builder.insertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

 Assert.assertEquals("CheckBox_OnlyChecked", doc.getRange().getFormFields().get(2).getName());

 // We can interact with these check boxes in Microsoft Word by double clicking them.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCheckBox.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Form alanının adı. Boş bir dize olabilir. 20 karakterden uzun değerler kırpılacaktır. |
| checkedValue | boolean | Onay kutusu form alanının işaretlenme durumu. |
| size | int | Onay kutusunun boyutunu puan cinsinden belirtir. MS Word'ün onay kutusunun boyutunu otomatik olarak hesaplaması için 0 girin. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - The form field node that was just inserted.
### insertComboBox(String name, String[] items, int selectedIndex) {#insertComboBox-java.lang.String-java.lang.String---int}
```
public FormField insertComboBox(String name, String[] items, int selectedIndex)
```


Geçerli konuma bir açılır kutu form alanı ekler.

 **Remarks:** 

Form alanı için bir ad belirtirseniz, aynı adla bir yer imi otomatik olarak oluşturulur.

 **Examples:** 

Form alanları oluşturmanın nasıl yapılacağını gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();

 // Form fields are objects in the document that the user can interact with by being prompted to enter values.
 // We can create them using a document builder, and below are two ways of doing so.
 // 1 -  Basic text input:
 builder.insertTextInput("My text input", TextFormFieldType.REGULAR,
         "", "Enter your name here", 30);

 // 2 -  Combo box with prompt text, and a range of possible values:
 String[] items =
         {
                 "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
         };

 builder.insertParagraph();
 builder.insertComboBox("My combo box", items, 0);

 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.CreateForm.docx");
 
```

Belgeye bir combo kutu form alanı eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a form that prompts the user to pick one of the items from the menu.
 builder.write("Pick a fruit: ");
 String[] items = {"Apple", "Banana", "Cherry"};
 builder.insertComboBox("DropDown", items, 0);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertComboBox.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Form alanının adı. Boş bir dize olabilir. 20 karakterden uzun değerler kırpılacaktır. |
| items | java.lang.String[] | ComboBox öğeleri. Azami 25 öğe. |
| selectedIndex | int | ComboBox'ta seçili öğenin indeksi. |

**Returns:**
[FormField](../../com.aspose.words/formfield/) - The form field node that was just inserted.
### insertDocument(Document srcDoc, int importFormatMode) {#insertDocument-com.aspose.words.Document-int}
```
public Node insertDocument(Document srcDoc, int importFormatMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document/) |  |
| importFormatMode | int |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#insertDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions}
```
public Node insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### insertDocumentInline(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#insertDocumentInline-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions}
```
public Node insertDocumentInline(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### insertField(int fieldType, boolean updateField) {#insertField-int-boolean}
```
public Field insertField(int fieldType, boolean updateField)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |

**Returns:**
[Field](../../com.aspose.words/field/)
### insertField(String fieldCode) {#insertField-java.lang.String}
```
public Field insertField(String fieldCode)
```


Bir belgeye bir Word alanı ekler ve alan sonucunu günceller.

 **Remarks:** 

Bu yöntem bir alanı belgeye ekler ve alan sonucunu hemen günceller. Aspose.Words çoğu türdeki alanları güncelleyebilir, ancak hepsini değil. Daha fazla ayrıntı için [insertField(java.lang.String, java.lang.String)](../../com.aspose.words/documentbuilder/\#insertField-java.lang.String--java.lang.String) aşırı yüklemesine bakın.

 **Examples:** 

Alanları eklemenin ve belge oluşturucunun imlecini onlara taşımanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField("MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
 builder.insertField("MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

 // Move the cursor to the first MERGEFIELD.
 builder.moveToMergeField("MyMergeField1", true, false);

 // Note that the cursor is placed immediately after the first MERGEFIELD, and before the second.
 Assert.assertEquals(doc.getRange().getFields().get(1).getStart(), builder.getCurrentNode());
 Assert.assertEquals(doc.getRange().getFields().get(0).getEnd(), builder.getCurrentNode().getPreviousSibling());

 // If we wish to edit the field's field code or contents using the builder,
 // its cursor would need to be inside a field.
 // To place it inside a field, we would need to call the document builder's MoveTo method
 // and pass the field's start or separator node as an argument.
 builder.write(" Text between our merge fields. ");

 doc.save(getArtifactsDir() + "DocumentBuilder.MergeFields.docx");
 
```

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
| fieldCode | java.lang.String | Eklenecek alan kodu (küme parantezleri olmadan). |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertField(String fieldCode, String fieldValue) {#insertField-java.lang.String-java.lang.String}
```
public Field insertField(String fieldCode, String fieldValue)
```


Bir belgeye bir Word alanı ekler ve alan sonucunu güncellemez.

 **Remarks:** 

Microsoft Word belgelerindeki alanlar bir alan kodu ve bir alan sonucu içerir. Alan kodu bir formül gibidir ve alan sonucu, formülün ürettiği değer gibidir. Alan kodu ayrıca belirli bir eylemi gerçekleştirmek için ek talimatlar gibi alan anahtarları da içerebilir.

Microsoft Word'de belge içinde alan kodlarını ve sonuçlarını görüntülemeyi Alt+F9 klavye kısayolu ile değiştirebilirsiniz. Alan kodları küme parantezleri ( \{ \} ) arasında görünür.

Bir alan oluşturmak için alan türünü, alan kodunu ve bir \"yer tutucu\" alan değerini belirtmeniz gerekir. Belirli bir alan kodu sözdiziminden emin değilseniz, önce Microsoft Word'de alanı oluşturun ve alan kodunu görmek için geçiş yapın.

Aspose.Words, çoğu alan türü için alan sonuçlarını hesaplayabilir, ancak bu yöntem alan sonucunu otomatik olarak güncellemez. Alan sonucu otomatik olarak hesaplanmadığı için, alan sonucuna eklenecek bir dize değeri (ya da boş bir dize) geçirmeniz beklenir. Bu değer, alan güncellenene kadar yer tutucu olarak alan sonucunda kalır. Alan sonucunu güncellemek için size döndürülen alan nesnesi üzerinde [Field.update()](../../com.aspose.words/field/\#update) metodunu çağırabilir veya belgedeki tüm alanları güncellemek için [Document.updateFields()](../../com.aspose.words/document/\#updateFields) metodunu kullanabilirsiniz.

 **Examples:** 

Bir bölümde sayfa numaralandırmayı nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 1, page 3.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("Section 2, page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Section 2, page 3.");

 // Move the document builder to the first section's primary header,
 // which every page in that section will display.
 builder.moveToSection(0);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);

 // Insert a PAGE field, which will display the number of the current page.
 builder.write("Page ");
 builder.insertField("PAGE", "");

 // Configure the section to have the page count that PAGE fields display start from 5.
 // Also, configure all PAGE fields to display their page numbers using uppercase Roman numerals.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageStartingNumber(5);
 pageSetup.setPageNumberStyle(NumberStyle.UPPERCASE_ROMAN);

 // Create another primary header for the second section, with another PAGE field.
 builder.moveToSection(1);
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);
 builder.write(" - ");
 builder.insertField("PAGE", "");
 builder.write(" - ");

 // Configure the section to have the page count that PAGE fields display start from 10.
 // Also, configure all PAGE fields to display their page numbers using Arabic numbers.
 pageSetup = doc.getSections().get(1).getPageSetup();
 pageSetup.setPageStartingNumber(10);
 pageSetup.setRestartPageNumbering(true);
 pageSetup.setPageNumberStyle(NumberStyle.ARABIC);

 doc.save(getArtifactsDir() + "PageSetup.PageNumbering.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldCode | java.lang.String | Eklenecek alan kodu (küme parantezleri olmadan). |
| fieldValue | java.lang.String | Eklenecek alan değeri. Değeri olmayan alanlar için  null  geçirin. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertFootnote(int footnoteType, String footnoteText) {#insertFootnote-int-java.lang.String}
```
public Footnote insertFootnote(int footnoteType, String footnoteText)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| footnoteType | int |  |
| footnoteText | java.lang.String |  |

**Returns:**
[Footnote](../../com.aspose.words/footnote/)
### insertFootnote(int footnoteType, String footnoteText, String referenceMark) {#insertFootnote-int-java.lang.String-java.lang.String}
```
public Footnote insertFootnote(int footnoteType, String footnoteText, String referenceMark)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| footnoteType | int |  |
| footnoteText | java.lang.String |  |
| referenceMark | java.lang.String |  |

**Returns:**
[Footnote](../../com.aspose.words/footnote/)
### insertForms2OleControl(Forms2OleControl forms2OleControl) {#insertForms2OleControl-com.aspose.words.Forms2OleControl}
```
public Shape insertForms2OleControl(Forms2OleControl forms2OleControl)
```


Geçerli konuma [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) nesnesi ekler..

 **Examples:** 

ActiveX kontrolünün nasıl ekleneceğini gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl();
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals(Forms2OleControlType.COMMAND_BUTTON, button1.getType());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| forms2OleControl | [Forms2OleControl](../../com.aspose.words/forms2olecontrol/) |  |

**Returns:**
[Shape](../../com.aspose.words/shape/) - [Shape](../../com.aspose.words/shape/) object that contains passed [Forms2OleControl](../../com.aspose.words/forms2olecontrol/)
### insertGroupShape(ShapeBase[] shapes) {#insertGroupShape-com.aspose.words.ShapeBase...}
```
public GroupShape insertGroupShape(ShapeBase[] shapes)
```


Parametre olarak verilen şekilleri yeni bir GroupShape düğümüne gruplar ve bu düğüm geçerli konuma eklenir.

 **Remarks:** 

Yeni GroupShape'in konumu ve boyutu otomatik olarak hesaplanacaktır.

VML ve DML şekilleri birlikte gruplanamaz.

 **Examples:** 

DML grup şeklinin nasıl ekleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape1 = builder.insertShape(ShapeType.RECTANGLE, 200.0, 250.0);
 shape1.setLeft(20.0);
 shape1.setTop(20.0);
 shape1.getStroke().setColor(Color.RED);

 Shape shape2 = builder.insertShape(ShapeType.ELLIPSE, 150.0, 200.0);
 shape2.setLeft(40.0);
 shape2.setTop(50.0);
 shape2.getStroke().setColor(Color.GREEN);

 // Dimensions for the new GroupShape node.
 double left = 10.0;
 double top = 10.0;
 double width = 200.0;
 double height = 300.0;
 // Insert GroupShape node for the specified size which is inserted into the specified position.
 GroupShape groupShape1 = builder.insertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

 // Insert GroupShape node which position and dimension will be calculated automatically.
 Shape shape3 = (Shape)shape1.deepClone(true);
 GroupShape groupShape2 = builder.insertGroupShape(shape3);

 doc.save(getArtifactsDir() + "Shape.InsertGroupShape.docx");
 
```

Grup şeklinin şekil ile nasıl birleştirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape1 = builder.insertShape(ShapeType.RECTANGLE, 200.0, 250.0);
 shape1.setLeft(20.0);
 shape1.setTop(20.0);
 shape1.getStroke().setColor(Color.RED);

 Shape shape2 = builder.insertShape(ShapeType.ELLIPSE, 150.0, 200.0);
 shape2.setLeft(40.0);
 shape2.setTop(50.0);
 shape2.getStroke().setColor(Color.GREEN);

 // Combine shapes into a GroupShape node which is inserted into the specified position.
 GroupShape groupShape1 = builder.insertGroupShape(shape1, shape2);

 // Combine Shape and GroupShape nodes.
 Shape shape3 = (Shape)shape1.deepClone(true);
 GroupShape groupShape2 = builder.insertGroupShape(groupShape1, shape3);

 doc.save(getArtifactsDir() + "Shape.CombineGroupShape.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapes | [ShapeBase\[\]](../../com.aspose.words/shapebase/) | Gruplanacak şekillerin listesi. |

**Returns:**
[GroupShape](../../com.aspose.words/groupshape/)
### insertGroupShape(double left, double top, double width, double height, ShapeBase[] shapes) {#insertGroupShape-double-double-double-double-com.aspose.words.ShapeBase...}
```
public GroupShape insertGroupShape(double left, double top, double width, double height, ShapeBase[] shapes)
```


Parametre olarak verilen şekilleri belirtilen boyutta yeni bir GroupShape düğümüne gruplar ve bu düğüm belirtilen konuma eklenir.

 **Remarks:** 

VML ve DML şekilleri birlikte gruplanamaz.

 **Examples:** 

DML grup şeklinin nasıl ekleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape1 = builder.insertShape(ShapeType.RECTANGLE, 200.0, 250.0);
 shape1.setLeft(20.0);
 shape1.setTop(20.0);
 shape1.getStroke().setColor(Color.RED);

 Shape shape2 = builder.insertShape(ShapeType.ELLIPSE, 150.0, 200.0);
 shape2.setLeft(40.0);
 shape2.setTop(50.0);
 shape2.getStroke().setColor(Color.GREEN);

 // Dimensions for the new GroupShape node.
 double left = 10.0;
 double top = 10.0;
 double width = 200.0;
 double height = 300.0;
 // Insert GroupShape node for the specified size which is inserted into the specified position.
 GroupShape groupShape1 = builder.insertGroupShape(left, top, width, height, new Shape[] { shape1, shape2 });

 // Insert GroupShape node which position and dimension will be calculated automatically.
 Shape shape3 = (Shape)shape1.deepClone(true);
 GroupShape groupShape2 = builder.insertGroupShape(shape3);

 doc.save(getArtifactsDir() + "Shape.InsertGroupShape.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| left | double | Orijinden grup şeklinin sol tarafına kadar olan mesafe (puan cinsinden). |
| top | double | Orijinden grup şeklinin üst tarafına kadar olan mesafe (puan cinsinden). |
| genişlik | double | Grup şeklinin genişliği (puan cinsinden). Negatif bir değer kabul edilmez. |
| yükseklik | double | Grup şeklinin yüksekliği (puan cinsinden). Negatif bir değer kabul edilmez. |
| shapes | [ShapeBase\[\]](../../com.aspose.words/shapebase/) | Gruplanacak şekillerin listesi. |

**Returns:**
[GroupShape](../../com.aspose.words/groupshape/)
### insertHorizontalRule() {#insertHorizontalRule}
```
public Shape insertHorizontalRule()
```


Belgeye yatay çizgi şekli ekler.

 **Examples:** 

Yatay kural şekli eklemeyi ve biçimlendirmesini özelleştirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Shape shape = builder.insertHorizontalRule();

 HorizontalRuleFormat horizontalRuleFormat = shape.getHorizontalRuleFormat();
 horizontalRuleFormat.setAlignment(HorizontalRuleAlignment.CENTER);
 horizontalRuleFormat.setWidthPercent(70.0);
 horizontalRuleFormat.setHeight(3.0);
 horizontalRuleFormat.setColor(Color.BLUE);
 horizontalRuleFormat.setNoShade(true);

 Assert.assertTrue(shape.isHorizontalRule());
 Assert.assertTrue(shape.getHorizontalRuleFormat().getNoShade());
 
```

**Returns:**
[Shape](../../com.aspose.words/shape/) - The shape that is a horizontal rule.
### insertHtml(String html) {#insertHtml-java.lang.String}
```
public void insertHtml(String html)
```


Belgeye bir HTML dizesi ekler.

 **Remarks:** 

Bu yöntemi bir HTML parçacığı veya tam bir HTML belgesi eklemek için kullanabilirsiniz.

 **Examples:** 

Bir belge oluşturucusunu kullanarak belgeye html içeriği eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final String HTML = " Paragraph right" +
         "Implicit paragraph left" +
         " Div center" +
         " Heading 1 left.";

 builder.insertHtml(HTML);

 // Inserting HTML code parses the formatting of each element into equivalent document text formatting.
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals("Paragraph right", paragraphs.get(0).getText().trim());
 Assert.assertEquals(ParagraphAlignment.RIGHT, paragraphs.get(0).getParagraphFormat().getAlignment());

 Assert.assertEquals("Implicit paragraph left", paragraphs.get(1).getText().trim());
 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(1).getParagraphFormat().getAlignment());
 Assert.assertTrue(paragraphs.get(1).getRuns().get(0).getFont().getBold());

 Assert.assertEquals("Div center", paragraphs.get(2).getText().trim());
 Assert.assertEquals(ParagraphAlignment.CENTER, paragraphs.get(2).getParagraphFormat().getAlignment());

 Assert.assertEquals("Heading 1 left.", paragraphs.get(3).getText().trim());
 Assert.assertEquals("Heading 1", paragraphs.get(3).getParagraphFormat().getStyle().getName());

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHtml.docx");
 
```

HTML belgeleri biçiminde birleştirme verilerini işleyen özel bir geri arama ile posta birleştirme nasıl yürütülür gösterir.

```

 public void insertHtml() throws Exception {
     Document doc = new Document(getMyDir() + "Field sample - MERGEFIELD.docx");

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertHtml());

     final String htmlText = "\r\n Hello world!\r\n";

     // Execute mail merge
     doc.getMailMerge().execute(new String[]{"htmlField1"}, new String[]{htmlText});

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertHtml.docx");
 }

 private class HandleMergeFieldInsertHtml implements IFieldMergingCallback {
     // This is called when merge field is actually merged with data in the document.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         // All merge fields that expect HTML data should be marked with some prefix, e.g. 'html'
         if (args.getDocumentFieldName().startsWith("html") && args.getField().getFieldCode().contains("\\b")) {
             FieldMergeField field = args.getField();

             // Insert the text for this merge field as HTML data, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getDocumentFieldName());
             builder.write(field.getTextBefore());
             builder.insertHtml((String) args.getFieldValue());

             // The HTML text itself should not be inserted
             // We have already inserted it as an HTML
             args.setText("");
         }
     }

     public void imageFieldMerging(ImageFieldMergingArgs args) {
         // Do nothing
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| html | java.lang.String | Belgeye eklenecek bir HTML dizesi. |

### insertHtml(String html, boolean useBuilderFormatting) {#insertHtml-java.lang.String-boolean}
```
public void insertHtml(String html, boolean useBuilderFormatting)
```


Belgeye bir HTML dizesi ekler.

 **Remarks:** 

Bu yöntemi bir HTML parçacığı veya tam bir HTML belgesi eklemek için kullanabilirsiniz.

useBuilderFormatting  false  olduğunda, [DocumentBuilder](../../com.aspose.words/documentbuilder/) biçimlendirmesi yok sayılır ve eklenen metnin biçimlendirmesi varsayılan HTML biçimlendirmesine dayanır. Sonuç olarak, metin tarayıcılarda render edildiği gibi görünür.

useBuilderFormatting true olduğunda, eklenen metnin biçimlendirmesi [DocumentBuilder](../../com.aspose.words/documentbuilder/) biçimlendirmesine dayanır ve metin, [write(java.lang.String)](../../com.aspose.words/documentbuilder/\#write-java.lang.String) ile eklenmiş gibi görünür.

 **Examples:** 

HTML içeriği eklerken bir DocumentBuilder'ın biçimlendirmesinin nasıl uygulanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set a text alignment for the builder, insert an HTML paragraph with a specified alignment, and one without.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.DISTRIBUTED);
 builder.insertHtml(
         " Paragraph 1." +
                 " Paragraph 2.", useBuilderFormatting);

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 // The first paragraph has an alignment specified. When InsertHtml parses the HTML code,
 // the paragraph alignment value found in the HTML code always supersedes the document builder's value.
 Assert.assertEquals("Paragraph 1.", paragraphs.get(0).getText().trim());
 Assert.assertEquals(ParagraphAlignment.RIGHT, paragraphs.get(0).getParagraphFormat().getAlignment());

 // The second paragraph has no alignment specified. It can have its alignment value filled in
 // by the builder's value depending on the flag we passed to the InsertHtml method.
 Assert.assertEquals("Paragraph 2.", paragraphs.get(1).getText().trim());
 Assert.assertEquals(useBuilderFormatting ? ParagraphAlignment.DISTRIBUTED : ParagraphAlignment.LEFT,
         paragraphs.get(1).getParagraphFormat().getAlignment());

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHtmlWithFormatting.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| html | java.lang.String | Belgeye eklenecek bir HTML dizesi. |
| useBuilderFormatting | boolean | [DocumentBuilder](../../com.aspose.words/documentbuilder/) içinde belirtilen biçimlendirmenin, HTML'den içe aktarılan metin için temel biçimlendirme olarak kullanılıp kullanılmadığını gösteren bir değer. |

### insertHtml(String html, int options) {#insertHtml-java.lang.String-int}
```
public void insertHtml(String html, int options)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| html | java.lang.String |  |
| seçenekler | int |  |

### insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark) {#insertHyperlink-java.lang.String-java.lang.String-boolean}
```
public Field insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)
```


Belgeye bir köprü ekler.

 **Remarks:** 

Hipermetin görüntü metni için yazı tipi biçimlendirmesini açıkça [getFont()](../../com.aspose.words/documentbuilder/\#getFont) özelliğini kullanarak belirtmeniz gerektiğini unutmayın.

Bu yöntem, belgeye bir MS Word HYPERLINK alanı eklemek için dahili olarak [insertField(java.lang.String)](../../com.aspose.words/documentbuilder/\#insertField-java.lang.String) metodunu çağırır.

 **Examples:** 

Bir hyperlink alanının nasıl ekleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("For more information, please visit the ");

 // Insert a hyperlink and emphasize it with custom formatting.
 // The hyperlink will be a clickable piece of text which will take us to the location specified in the URL.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 builder.insertHyperlink("Google website", "https://www.google.com", false);
 builder.getFont().clearFormatting();
 builder.writeln(".");

 // Ctrl + left clicking the link in the text in Microsoft Word will take us to the URL via a new web browser window.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlink.docx");
 
```

Bir DocumentBuilder'ın biçimlendirme yığını nasıl kullanılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set up font formatting, then write the text that goes before the hyperlink.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(24.0);
 builder.write("To visit Google, hold Ctrl and click ");

 // Preserve our current formatting configuration on the stack.
 builder.pushFont();

 // Alter the builder's current formatting by applying a new style.
 builder.getFont().setStyleIdentifier(StyleIdentifier.HYPERLINK);
 builder.insertHyperlink("here", "http://www.google.com", false);

 Assert.assertEquals(Color.BLUE.getRGB(), builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.SINGLE, builder.getFont().getUnderline());

 // Restore the font formatting that we saved earlier and remove the element from the stack.
 builder.popFont();

 Assert.assertEquals(0, builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.NONE, builder.getFont().getUnderline());

 builder.write(". We hope you enjoyed the example.");

 doc.save(getArtifactsDir() + "DocumentBuilder.PushPopFont.docx");
 
```

Yerel bir yer imine referans veren bir köprü eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startBookmark("Bookmark1");
 builder.write("Bookmarked text. ");
 builder.endBookmark("Bookmark1");
 builder.writeln("Text outside of the bookmark.");

 // Insert a HYPERLINK field that links to the bookmark. We can pass field switches
 // to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 FieldHyperlink hyperlink = (FieldHyperlink)builder.insertHyperlink("Link to Bookmark1", "Bookmark1", true);
 hyperlink.setScreenTip("Hyperlink Tip");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| displayText | java.lang.String | Belgede görüntülenecek bağlantının metni. |
| urlOrBookmark | java.lang.String | Bağlantı hedefi. Bir URL veya belgedeki bir yer işareti adı olabilir. Bu yöntem, URL'nin başına ve sonuna her zaman tek tırnak ekler. |
| isBookmark | boolean | true ise önceki parametre belgedeki bir yer işareti adıdır; false ise önceki parametre bir URL'dir. |

**Returns:**
[Field](../../com.aspose.words/field/) - A [Field](../../com.aspose.words/field/) object that represents the inserted field.
### insertImage(byte[] imageBytes) {#insertImage-byte}
```
public Shape insertImage(byte[] imageBytes)
```


Bir bayt dizisinden belgeye bir resim ekler. Resim satır içi ve %100 ölçekle eklenir.

 **Remarks:** 

Bu yöntem tarafından döndürülen [Shape](../../com.aspose.words/shape/) nesnesini kullanarak resim boyutunu, konumunu, yerleştirme yöntemini ve diğer ayarları değiştirebilirsiniz.

 **Examples:** 

Bir bayt dizisinden belgeye bir resim nasıl eklenir gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 byte[] imageByteArray = DocumentHelper.getBytesFromStream(new FileInputStream(getImageDir() + "Logo.jpg"));

 // Below are three ways of inserting an image from a byte array.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(imageByteArray);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(imageByteArray, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(imageByteArray, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromByteArray.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageBytes | byte[] | Resmi içeren bayt dizisi. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(byte[] imageBytes, double width, double height) {#insertImage-byte---double-double}
```
public Shape insertImage(byte[] imageBytes, double width, double height)
```


Belgeye bir bayt dizisinden satır içi bir görüntü ekler ve belirtilen boyuta ölçeklendirir.

 **Remarks:** 

Bu yöntem tarafından döndürülen [Shape](../../com.aspose.words/shape/) nesnesini kullanarak resim boyutunu, konumunu, yerleştirme yöntemini ve diğer ayarları değiştirebilirsiniz.

 **Examples:** 

Bir bayt dizisinden belgeye bir resim nasıl eklenir gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 byte[] imageByteArray = DocumentHelper.getBytesFromStream(new FileInputStream(getImageDir() + "Logo.jpg"));

 // Below are three ways of inserting an image from a byte array.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(imageByteArray);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(imageByteArray, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(imageByteArray, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromByteArray.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageBytes | byte[] | Resmi içeren bayt dizisi. |
| genişlik | double | Resmin nokta cinsinden genişliği. %100 ölçek isteniyorsa negatif veya sıfır değer verilebilir. |
| yükseklik | double | Resmin nokta cinsinden yüksekliği. %100 ölçek isteniyorsa negatif veya sıfır değer verilebilir. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-byte---int-double-int-double-double-double-int}
```
public Shape insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageBytes | byte[] |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| genişlik | double |  |
| yükseklik | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(BufferedImage image) {#insertImage-java.awt.image.BufferedImage}
```
public Shape insertImage(BufferedImage image)
```


Belgeye bir resim ekler. Belgeye bir java.awt.image.BufferedImage nesnesinden bir resim ekler. Resim satır içi ve %100 ölçekle eklenir.

 **Remarks:** 

Bu yöntem tarafından döndürülen [Shape](../../com.aspose.words/shape/) nesnesini kullanarak resim boyutunu, konumunu, yerleştirme yöntemini ve diğer ayarları değiştirebilirsiniz.

Aspose.Words, resmi PNG formatında ve varsayılan ayarlarla ekleyecektir. Başka bir formatta veya farklı ayarlarla bir BufferedImage eklemek istiyorsanız, resmi bir bayt dizisine kaydedip [insertImage(byte[])](../../com.aspose.words/documentbuilder/\#insertImage-byte) metodunu kullanmanız gerekir.

 **Examples:** 

Bir nesneden belgeye bir resim nasıl eklenir gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String imageFile = getImageDir() + "Logo.jpg";

 // Below are three ways of inserting an image from an Image object instance.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(imageFile);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(imageFile, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(imageFile, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromImageObject.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| görüntü | java.awt.image.BufferedImage | Belgeye eklenecek resim. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(BufferedImage image, double width, double height) {#insertImage-java.awt.image.BufferedImage-double-double}
```
public Shape insertImage(BufferedImage image, double width, double height)
```


Belgeye bir java.awt.image.BufferedImage nesnesinden satır içi bir görüntü ekler ve belirtilen boyuta ölçeklendirir.

 **Remarks:** 

Bu yöntem tarafından döndürülen [Shape](../../com.aspose.words/shape/) nesnesini kullanarak resim boyutunu, konumunu, yerleştirme yöntemini ve diğer ayarları değiştirebilirsiniz.

Aspose.Words, resmi PNG formatında ve varsayılan ayarlarla ekleyecektir. Başka bir formatta veya farklı ayarlarla bir BufferedImage eklemek istiyorsanız, resmi bir bayt dizisine kaydedip [insertImage(byte[])](../../com.aspose.words/documentbuilder/\#insertImage-byte) metodunu kullanmanız gerekir.

 **Examples:** 

Bir nesneden belgeye bir resim nasıl eklenir gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String imageFile = getImageDir() + "Logo.jpg";

 // Below are three ways of inserting an image from an Image object instance.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(imageFile);

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(imageFile, ConvertUtil.pixelToPoint(250.0), ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(imageFile, RelativeHorizontalPosition.MARGIN, 100.0, RelativeVerticalPosition.MARGIN,
         100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromImageObject.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| görüntü | java.awt.image.BufferedImage | Belgeye eklenecek resim. |
| genişlik | double | Resmin nokta cinsinden genişliği. %100 ölçek isteniyorsa negatif veya sıfır değer verilebilir. |
| yükseklik | double | Resmin nokta cinsinden yüksekliği. %100 ölçek isteniyorsa negatif veya sıfır değer verilebilir. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int}
```
public Shape insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| görüntü | java.awt.image.BufferedImage |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| genişlik | double |  |
| yükseklik | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(InputStream stream) {#insertImage-java.io.InputStream}
```
public Shape insertImage(InputStream stream)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(InputStream stream, double width, double height) {#insertImage-java.io.InputStream-double-double}
```
public Shape insertImage(InputStream stream, double width, double height)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| genişlik | double |  |
| yükseklik | double |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.io.InputStream-int-double-int-double-double-double-int}
```
public Shape insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| genişlik | double |  |
| yükseklik | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertImage(String fileName) {#insertImage-java.lang.String}
```
public Shape insertImage(String fileName)
```


Bir dosya veya URL'den belgeye bir resim ekler. Resim satır içi ve %100 ölçekle eklenir.

 **Remarks:** 

Bu aşırı yükleme, uzak bir URI belirttiğinizde resmi belgeye eklemeden önce otomatik olarak indirir.

Bu yöntem tarafından döndürülen [Shape](../../com.aspose.words/shape/) nesnesini kullanarak resim boyutunu, konumunu, yerleştirme yöntemini ve diğer ayarları değiştirebilirsiniz.

 **Examples:** 

Yerel dosya sisteminden bir belgeye resim eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three ways of inserting an image from a local system filename.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(getImageDir() + "Logo.jpg");

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(getImageDir() + "Transparent background logo.png", ConvertUtil.pixelToPoint(250.0),
         ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(getImageDir() + "Windows MetaFile.wmf", RelativeHorizontalPosition.MARGIN, 100.0,
         RelativeVerticalPosition.MARGIN, 100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromFilename.docx");
 
```

Hangi resmin ekleneceğini belirlemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertImage(getImageDir() + "Scalable Vector Graphics.svg");

 // Aspose.Words insert SVG image to the document as PNG with svgBlip extension
 // that contains the original vector SVG image representation.
 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

 // Aspose.Words insert SVG image to the document as PNG, just like Microsoft Word does for old format.
 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2003);

 // Aspose.Words insert SVG image to the document as EMF metafile to keep the image in vector representation.
 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
 
```

Belgeye gif resmi eklemenin nasıl yapılacağını gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();

 // We can insert gif image using path or bytes array.
 // It works only if DocumentBuilder optimized to Word version 2010 or higher.
 // Note, that access to the image bytes causes conversion Gif to Png.
 Shape gifImage = builder.insertImage(getImageDir() + "Graphics Interchange Format.gif");

 gifImage = builder.insertImage(DocumentHelper.getBytesFromStream(new FileInputStream(getImageDir() + "Graphics Interchange Format.gif")));

 builder.getDocument().save(getArtifactsDir() + "InsertGif.docx");
 
```

Belgeye bir şekil ve resim eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two locations where the document builder's "InsertShape" method
 // can source the image that the shape will display.
 // 1 -  Pass a local file system filename of an image file:
 builder.write("Image from local file: ");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.writeln();

 // 2 -  Pass a URL which points to an image.
 builder.write("Image from a URL: ");
 builder.insertImage(getImageUri().toURL().openStream());
 builder.writeln();

 doc.save(getArtifactsDir() + "Image.FromUrl.docx");
 
```

Yüzen bir görüntünün sayfanın ortasına nasıl ekleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a floating image that will appear behind the overlapping text and align it to the page's center.
 Shape shape = builder.insertImage(getImageDir() + "Logo.jpg");
 shape.setWrapType(WrapType.NONE);
 shape.setBehindText(true);
 shape.setRelativeHorizontalPosition(RelativeHorizontalPosition.PAGE);
 shape.setRelativeVerticalPosition(RelativeVerticalPosition.PAGE);
 shape.setHorizontalAlignment(HorizontalAlignment.CENTER);
 shape.setVerticalAlignment(VerticalAlignment.CENTER);

 doc.save(getArtifactsDir() + "Image.CreateFloatingPageCenter.docx");
 
```

WebP resmi eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertImage(getImageDir() + "WebP image.webp");

 doc.save(getArtifactsDir() + "Image.InsertWebpImage.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Resim içeren dosya. Herhangi geçerli yerel veya uzak URI olabilir. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(String fileName, double width, double height) {#insertImage-java.lang.String-double-double}
```
public Shape insertImage(String fileName, double width, double height)
```


Belgeye bir dosya veya URL'den satır içi bir görüntü ekler ve belirtilen boyuta ölçeklendirir.

 **Remarks:** 

Bu yöntem tarafından döndürülen [Shape](../../com.aspose.words/shape/) nesnesini kullanarak resim boyutunu, konumunu, yerleştirme yöntemini ve diğer ayarları değiştirebilirsiniz.

 **Examples:** 

Yerel dosya sisteminden bir belgeye resim eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are three ways of inserting an image from a local system filename.
 // 1 -  Inline shape with a default size based on the image's original dimensions:
 builder.insertImage(getImageDir() + "Logo.jpg");

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Inline shape with custom dimensions:
 builder.insertImage(getImageDir() + "Transparent background logo.png", ConvertUtil.pixelToPoint(250.0),
         ConvertUtil.pixelToPoint(144.0));

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 3 -  Floating shape with custom dimensions:
 builder.insertImage(getImageDir() + "Windows MetaFile.wmf", RelativeHorizontalPosition.MARGIN, 100.0,
         RelativeVerticalPosition.MARGIN, 100.0, 200.0, 100.0, WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilderImages.InsertImageFromFilename.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Resmi içeren dosya. |
| genişlik | double | Resmin nokta cinsinden genişliği. %100 ölçek isteniyorsa negatif veya sıfır değer verilebilir. |
| yükseklik | double | Resmin nokta cinsinden yüksekliği. %100 ölçek isteniyorsa negatif veya sıfır değer verilebilir. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.lang.String-int-double-int-double-double-double-int}
```
public Shape insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| genişlik | double |  |
| yükseklik | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertNode(Node node) {#insertNode-com.aspose.words.Node}
```
public void insertNode(Node node)
```


İmlecin önüne bir düğüm ekler.

 **Examples:** 

Bir belgeye bağlı bir görüntünün nasıl ekleneceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String imageFileName = getImageDir() + "Windows MetaFile.wmf";

 // Below are two ways of applying an image to a shape so that it can display it.
 // 1 -  Set the shape to contain the image.
 Shape shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setImage(imageFileName);

 builder.insertNode(shape);

 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx");

 // Every image that we store in shape will increase the size of our document.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Embedded.docx").length() > 70000);

 doc.getFirstSection().getBody().getFirstParagraph().removeAllChildren();

 // 2 -  Set the shape to link to an image file in the local file system.
 shape = new Shape(builder.getDocument(), ShapeType.IMAGE);
 shape.setWrapType(WrapType.INLINE);
 shape.getImageData().setSourceFullName(imageFileName);

 builder.insertNode(shape);
 doc.save(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx");

 // Linking to images will save space and result in a smaller document.
 // However, the document can only display the image correctly while
 // the image file is present at the location that the shape's "SourceFullName" property points to.
 Assert.assertTrue(new File(getArtifactsDir() + "Image.CreateLinkedImage.Linked.docx").length() < 10000);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) |  |

### insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation) {#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream}
```
public Shape insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| progId | java.lang.String |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation) {#insertOleObject-java.lang.String-boolean-boolean-java.io.InputStream}
```
public Shape insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String |  |
| isLinked | boolean |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation) {#insertOleObject-java.lang.String-java.lang.String-boolean-boolean-java.io.InputStream}
```
public Shape insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String |  |
| progId | java.lang.String |  |
| isLinked | boolean |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.io.InputStream-java.lang.String-java.lang.String-java.lang.String}
```
public Shape insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| progId | java.lang.String |  |
| iconFile | java.lang.String |  |
| iconCaption | java.lang.String |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.lang.String-boolean-java.lang.String-java.lang.String}
```
public Shape insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption)
```


Bir OLE nesnesini gömülü veya bağlantılı olarak belgeye simge olarak ekler. Simge dosyasını ve başlığını belirtmeye izin verir. OLE nesnesi türünü dosya uzantısını kullanarak algılar.

 **Examples:** 

Bir OLE nesnesini belgeye eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // OLE objects are links to files in our local file system that can be opened by other installed applications.
 // Double clicking these shapes will launch the application, and then use it to open the linked object.
 // There are three ways of using the InsertOleObject method to insert these shapes and configure their appearance.
 // If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
 // the icon according to the file extension and uses the filename for the icon caption.
 // 1 -  Image taken from the local file system:
 builder.insertOleObject(getMyDir() + "Spreadsheet.xlsx", false, false, new FileInputStream(getImageDir() + "Logo.jpg"));

 // If 'presentation' is omitted and 'asIcon' is set, this overloaded method selects
 // the icon according to 'progId' and uses the filename for the icon caption.
 // 2 -  Icon based on the application that will open the object:
 builder.insertOleObject(getMyDir() + "Spreadsheet.xlsx", "Excel.Sheet", false, true, new FileInputStream(getImageDir() + "Logo.jpg"));

 // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
 // the icon according to 'progId' and uses the predefined icon caption.
 // 3 -  Image icon that's 32 x 32 pixels or smaller from the local file system, with a custom caption:
 builder.insertOleObjectAsIcon(getMyDir() + "Presentation.pptx", false, getImageDir() + "Logo icon.ico",
         "Double click to view presentation!");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertOleObject.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Dosyanın tam yolu. |
| isLinked | boolean | Eğer  true  ise bağlantılı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| iconFile | java.lang.String | ICO dosyasının tam yolu. Değer  null  ise Aspose.Words önceden tanımlı bir resmi kullanacaktır. |
| iconCaption | java.lang.String | Simge başlığı. Değer  null  ise Aspose.Words dosya adını kullanacaktır. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - Shape node containing Ole object and inserted at the current Builder position.
### insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String}
```
public Shape insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)
```


Bir OLE nesnesini gömülü veya bağlantılı olarak belgeye simge olarak ekler. Simge dosyasını ve başlığını belirtmeye izin verir. OLE nesnesi türünü verilen progID parametresiyle algılar.

 **Examples:** 

Bir OLE nesnesini gömülü veya bağlantılı olarak belgeye simge olarak eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
 // the icon according to 'progId' and uses the filename for the icon caption.
 builder.insertOleObjectAsIcon(getMyDir() + "Presentation.pptx", "Package", false, getImageDir() + "Logo icon.ico", "My embedded file");

 builder.insertBreak(BreakType.LINE_BREAK);

 try (FileInputStream stream = new FileInputStream(getMyDir() + "Presentation.pptx")) {
     // If 'iconFile' and 'iconCaption' are omitted, this overloaded method selects
     // the icon according to the file extension and uses the filename for the icon caption.
     Shape shape = builder.insertOleObjectAsIcon(stream, "PowerPoint.Application", getImageDir() + "Logo icon.ico",
             "My embedded file stream");

     OlePackage setOlePackage = shape.getOleFormat().getOlePackage();
     setOlePackage.setFileName("Presentation.pptx");
     setOlePackage.setDisplayName("Presentation.pptx");
 }

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertOleObjectAsIcon.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Dosyanın tam yolu. |
| progId | java.lang.String | OLE nesnesinin ProgId'i. |
| isLinked | boolean | Eğer  true  ise bağlantılı OLE nesnesi eklenir, aksi takdirde gömülü OLE nesnesi eklenir. |
| iconFile | java.lang.String | ICO dosyasının tam yolu. Değer  null  ise Aspose.Words önceden tanımlı bir resmi kullanacaktır. |
| iconCaption | java.lang.String | Simge başlığı. Değer  null  ise Aspose.Words dosya adını kullanacaktır. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - Shape node containing Ole object and inserted at the current Builder position.
### insertOnlineVideo(String videoUrl, double width, double height) {#insertOnlineVideo-java.lang.String-double-double}
```
public Shape insertOnlineVideo(String videoUrl, double width, double height)
```


Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçeklendirir.

 **Remarks:** 

Bu yöntem tarafından döndürülen [Shape](../../com.aspose.words/shape/) nesnesini kullanarak resim boyutunu, konumunu, yerleştirme yöntemini ve diğer ayarları değiştirebilirsiniz.

Aşağıdaki kaynaklardan çevrimiçi video ekleme desteklenir:

 *  https://www.youtube.com/
 *  https://vimeo.com/

Çevrimiçi videonuz doğru görüntülenmiyorsa, özel gömülü html kodu kabul eden [insertOnlineVideo(java.lang.String, java.lang.String, byte[], double, double)](../../com.aspose.words/documentbuilder/\#insertOnlineVideo-java.lang.String--java.lang.String--byte----double--double) yöntemini kullanın.

Video gömme kodu sağlayıcılar arasında değişebilir, ayrıntılar için tercih ettiğiniz ilgili sağlayıcıya başvurun.

 **Examples:** 

Bir URL kullanarak belgeye çevrimiçi video eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertOnlineVideo("https://youtu.be/g1N9ke8Prmk", 360.0, 270.0);

 // We can watch the video from Microsoft Word by clicking on the shape.
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertVideoWithUrl.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| videoUrl | java.lang.String | Videonun URL'si. |
| genişlik | double | Resmin nokta cinsinden genişliği. %100 ölçek isteniyorsa negatif veya sıfır değer verilebilir. |
| yükseklik | double | Resmin nokta cinsinden yüksekliği. %100 ölçek isteniyorsa negatif veya sıfır değer verilebilir. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int}
```
public Shape insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| videoUrl | java.lang.String |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| genişlik | double |  |
| yükseklik | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double}
```
public Shape insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)
```


Belgeye çevrimiçi bir video nesnesi ekler ve belirtilen boyuta ölçeklendirir.

 **Remarks:** 

Bu yöntem tarafından döndürülen [Shape](../../com.aspose.words/shape/) nesnesini kullanarak resim boyutunu, konumunu, yerleştirme yöntemini ve diğer ayarları değiştirebilirsiniz.

 **Examples:** 

Özel bir küçük resimle bir belgeye çevrimiçi video eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 String videoUrl = "https://vimeo.com/52477838";
 String videoEmbedCode = "";

 byte[] thumbnailImageBytes = IOUtils.toByteArray(getImageUri().toURL().openStream());

 BufferedImage image = ImageIO.read(new ByteArrayInputStream(thumbnailImageBytes));

 // Below are two ways of creating a shape with a custom thumbnail, which links to an online video
 // that will play when we click on the shape in Microsoft Word.
 // 1 -  Insert an inline shape at the builder's node insertion cursor:
 builder.insertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.getWidth(), image.getHeight());

 builder.insertBreak(BreakType.PAGE_BREAK);

 // 2 -  Insert a floating shape:
 double left = builder.getPageSetup().getRightMargin() - image.getWidth();
 double top = builder.getPageSetup().getBottomMargin() - image.getHeight();

 builder.insertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
         RelativeHorizontalPosition.RIGHT_MARGIN, left, RelativeVerticalPosition.BOTTOM_MARGIN, top,
         image.getWidth(), image.getHeight(), WrapType.SQUARE);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| videoUrl | java.lang.String | Videonun URL'si. |
| videoEmbedCode | java.lang.String | Videonun gömme kodu. |
| thumbnailImageBytes | byte[] | Küçük resim görüntüsü baytları. |
| genişlik | double | Resmin nokta cinsinden genişliği. %100 ölçek isteniyorsa negatif veya sıfır değer verilebilir. |
| yükseklik | double | Resmin nokta cinsinden yüksekliği. %100 ölçek isteniyorsa negatif veya sıfır değer verilebilir. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The image node that was just inserted.
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int}
```
public Shape insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| videoUrl | java.lang.String |  |
| videoEmbedCode | java.lang.String |  |
| thumbnailImageBytes | byte[] |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| genişlik | double |  |
| yükseklik | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertParagraph() {#insertParagraph}
```
public Paragraph insertParagraph()
```


Belgeye bir paragraf sonu ekler.

 **Remarks:** 

Geçerli paragraf biçimlendirmesi, [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) özelliği tarafından belirtilmiştir ve kullanılır.

Geçerli paragrafı ikiye böler. Paragraf eklendikten sonra imleç yeni paragrafın başına yerleştirilir.

Geçerli imleç konumunda paragraf sonu eklemek mümkün değilse bir istisna fırlatılır.

 **Examples:** 

Belgeye bir paragraf eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Font font = builder.getFont();
 font.setSize(16.0);
 font.setBold(true);
 font.setColor(Color.BLUE);
 font.setName("Arial");
 font.setUnderline(Underline.DASH);

 ParagraphFormat paragraphFormat = builder.getParagraphFormat();
 paragraphFormat.setFirstLineIndent(8.0);
 paragraphFormat.setAlignment(ParagraphAlignment.JUSTIFY);
 paragraphFormat.setAddSpaceBetweenFarEastAndAlpha(true);
 paragraphFormat.setAddSpaceBetweenFarEastAndDigit(true);
 paragraphFormat.setKeepTogether(true);

 // The "Writeln" method ends the paragraph after appending text
 // and then starts a new line, adding a new paragraph.
 builder.writeln("Hello world!");

 Assert.assertTrue(builder.getCurrentParagraph().isEndOfDocument());
 
```

**Returns:**
[Paragraph](../../com.aspose.words/paragraph/) - The paragraph node that was just inserted. It is the same node as [getCurrentParagraph()](../../com.aspose.words/documentbuilder/\#getCurrentParagraph).
### insertShape(int shapeType, double width, double height) {#insertShape-int-double-double}
```
public Shape insertShape(int shapeType, double width, double height)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapeType | int |  |
| genişlik | double |  |
| yükseklik | double |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertShape-int-int-double-int-double-double-double-int}
```
public Shape insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| shapeType | int |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| genişlik | double |  |
| yükseklik | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertSignatureLine(SignatureLineOptions signatureLineOptions) {#insertSignatureLine-com.aspose.words.SignatureLineOptions}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions)
```


Geçerli konuma bir imza satırı ekler.

 **Examples:** 

Kişisel bir sertifika ve imza satırıyla bir belgeyi nasıl imzalayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 SignatureLineOptions signatureLineOptions = new SignatureLineOptions();
 signatureLineOptions.setSigner("vderyushev");
 signatureLineOptions.setSignerTitle("QA");
 signatureLineOptions.setEmail("vderyushev@aspose.com");
 signatureLineOptions.setShowDate(true);
 signatureLineOptions.setDefaultInstructions(false);
 signatureLineOptions.setInstructions("Please sign here.");
 signatureLineOptions.setAllowComments(true);

 SignatureLine signatureLine = builder.insertSignatureLine(signatureLineOptions).getSignatureLine();
 signatureLine.setProviderId(UUID.fromString("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2"));

 Assert.assertFalse(signatureLine.isSigned());
 Assert.assertFalse(signatureLine.isValid());

 doc.save(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx");

 Date currentDate = new Date();

 SignOptions signOptions = new SignOptions();
 signOptions.setSignatureLineId(signatureLine.getId());
 signOptions.setProviderId(signatureLine.getProviderId());
 signOptions.setComments("Document was signed by vderyushev");
 signOptions.setSignTime(currentDate);

 CertificateHolder certHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 DigitalSignatureUtil.sign(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.docx",
         getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

 // Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
 // indicating that the signature line contains a signature.
 doc = new Document(getArtifactsDir() + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 signatureLine = shape.getSignatureLine();

 Assert.assertTrue(signatureLine.isSigned());
 Assert.assertTrue(signatureLine.isValid());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions/) | İmza satırı oluşturma parametrelerini saklayan nesne. |

**Returns:**
[Shape](../../com.aspose.words/shape/) - The signature line node that was just inserted.
### insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType) {#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions/) |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| wrapType | int |  |

**Returns:**
[Shape](../../com.aspose.words/shape/)
### insertStructuredDocumentTag(int type) {#insertStructuredDocumentTag-int}
```
public StructuredDocumentTag insertStructuredDocumentTag(int type)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tip | int |  |

**Returns:**
[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/)
### insertStyleSeparator() {#insertStyleSeparator}
```
public void insertStyleSeparator()
```


Belgeye stil ayırıcı ekler.

 **Remarks:** 

Bu yöntem, bir metin satırının iki farklı kısmına farklı paragraf stilleri uygulamaya izin verir.

 **Examples:** 

Stil ayırıcılarıyla çalışmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Each paragraph can only have one style.
 // The InsertStyleSeparator method allows us to work around this limitation.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.write("This text is in a Heading style. ");
 builder.insertStyleSeparator();

 Style paraStyle = builder.getDocument().getStyles().add(StyleType.PARAGRAPH, "MyParaStyle");
 paraStyle.getFont().setBold(false);
 paraStyle.getFont().setSize(8.0);
 paraStyle.getFont().setName("Arial");

 builder.getParagraphFormat().setStyleName(paraStyle.getName());
 builder.write("This text is in a custom style. ");

 // Calling the InsertStyleSeparator method creates another paragraph,
 // which can have a different style to the previous. There will be no break between paragraphs.
 // The text in the output document will look like one paragraph with two styles.
 Assert.assertEquals(2, doc.getFirstSection().getBody().getParagraphs().getCount());
 Assert.assertEquals("Heading 1", doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle().getName());
 Assert.assertEquals("MyParaStyle", doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle().getName());

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertStyleSeparator.docx");
 
```

### insertTableOfContents(String switches) {#insertTableOfContents-java.lang.String}
```
public Field insertTableOfContents(String switches)
```


Belgeye bir TOC (içindekiler tablosu) alanı ekler.

 **Remarks:** 

Bu yöntem, mevcut konumda belgeye bir DİZİN (içindekiler tablosu) alanı ekler.

Word belgesindeki bir içindekiler tablosu çeşitli yollarla oluşturulabilir ve çeşitli seçeneklerle biçimlendirilebilir. Tablonun Microsoft Word tarafından nasıl oluşturulduğu ve görüntülendiği, alan anahtarları tarafından kontrol edilir.

Anahtarları belirtmenin en kolay yolu, Insert->Reference->Index and Tables menüsünü kullanarak bir Word belgesine içindekiler tablosu eklemek ve yapılandırmaktır; ardından alan kodlarının görüntülenmesini açarak anahtarları görebilirsiniz. Microsoft Word'de alan kodlarının görüntülenmesini açıp kapatmak için Alt+F9 tuşuna basabilirsiniz.

Örneğin, bir içindekiler tablosu oluşturduktan sonra belgeye aşağıdaki alan eklenir: **\{ TOC \\o "1-3" \\h \\z \}**. **\\o "1-3" \\h \\z** ifadesini kopyalayabilir ve anahtar parametresi olarak kullanabilirsiniz.

Şunu unutmayın: [insertTableOfContents(java.lang.String)](../../com.aspose.words/documentbuilder/\#insertTableOfContents-java.lang.String) yalnızca bir DİZİN alanı ekleyecek, ancak içindekiler tablosunu gerçekten oluşturmayacaktır. İçindekiler tablosu, alan güncellendiğinde Microsoft Word tarafından oluşturulur.

Bu yöntemi kullanarak bir içindekiler tablosu eklerseniz ve ardından dosyayı Microsoft Word'de açarsanız, DİZİN alanı henüz güncellenmediği için içindekiler tablosunu görmezsiniz.

Microsoft Word'de, bir belge açıldığında alanlar otomatik olarak güncellenmez, ancak F9 tuşuna basarak istediğiniz zaman alanları güncelleyebilirsiniz.

 **Examples:** 

Başlık stillerini giriş olarak kullanarak bir belgeye İçindekiler Tablosu (TOC) nasıl eklenir gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents for the first page of the document.
 // Configure the table to pick up paragraphs with headings of levels 1 to 3.
 // Also, set its entries to be hyperlinks that will take us
 // to the location of the heading when left-clicked in Microsoft Word.
 builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Populate the table of contents by adding paragraphs with heading styles.
 // Each such heading with a level between 1 and 3 will create an entry in the table.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 2");
 builder.writeln("Heading 3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);
 builder.writeln("Heading 3.1.1");
 builder.writeln("Heading 3.1.2");
 builder.writeln("Heading 3.1.3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);
 builder.writeln("Heading 3.1.3.1");
 builder.writeln("Heading 3.1.3.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.2");
 builder.writeln("Heading 3.3");

 // A table of contents is a field of a type that needs to be updated to show an up-to-date result.
 doc.updateFields();
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertToc.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| anahtarlar | java.lang.String | DİZİN alanı anahtarları. |

**Returns:**
[Field](../../com.aspose.words/field/)
### insertTextInput(String name, int type, String format, String fieldValue, int maxLength) {#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int}
```
public FormField insertTextInput(String name, int type, String format, String fieldValue, int maxLength)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String |  |
| tip | int |  |
| biçim | java.lang.String |  |
| fieldValue | java.lang.String |  |
| maxLength | int |  |

**Returns:**
[FormField](../../com.aspose.words/formfield/)
### isAtEndOfParagraph() {#isAtEndOfParagraph}
```
public boolean isAtEndOfParagraph()
```


İmleç geçerli paragrafın sonunda ise  true  döndürür.

 **Examples:** 

Bir belge oluşturucunun imlecini belgede farklı düğümlere taşımayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
boolean -  true  eğer imleç geçerli paragrafın sonunda ise.
### isAtEndOfStructuredDocumentTag() {#isAtEndOfStructuredDocumentTag}
```
public boolean isAtEndOfStructuredDocumentTag()
```


İmleç yapılandırılmış belge etiketinin sonunda ise **true** döndürür.

 **Examples:** 

DocumentBuilder'ın imlecini yapılandırılmış belge etiketi içinde taşımayı gösterir.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Returns:**
boolean - **true** eğer imleç yapılandırılmış belge etiketinin sonunda ise.
### isAtStartOfParagraph() {#isAtStartOfParagraph}
```
public boolean isAtStartOfParagraph()
```


İmleç geçerli paragrafın başında ise (imleçten önce metin yok)  true  döndürür.

 **Examples:** 

Bir belge oluşturucunun imlecini belgede farklı düğümlere taşımayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Returns:**
boolean -  true  eğer imleç geçerli paragrafın başında ise (imleçten önce metin yok).
### moveTo(Node node) {#moveTo-com.aspose.words.Node}
```
public void moveTo(Node node)
```


İmleci satır içi bir düğüme ya da bir paragrafın sonuna taşır.

 **Remarks:** 

*node* bir satır içi düğüm olduğunda, imleç bu düğüme taşınır ve sonraki içerik o düğümün önüne eklenir.

*node* bir [Paragraph](../../com.aspose.words/paragraph/) olduğunda, imleç paragrafın sonuna taşınır ve sonraki içerik paragraf sonu kırılmasının hemen önüne eklenir.

*node* bir blok düzeyinde düğüm ancak bir [Paragraph](../../com.aspose.words/paragraph/) değilse, imleç blok düzeyindeki düğümdeki ilk paragrafın sonuna taşınır ve sonraki içerik paragraf sonu kırılmasının hemen önüne eklenir.

 **Examples:** 

Bir belge oluşturucunun imlecini belgede farklı düğümlere taşımayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

Bir DocumentBuilder'ın imleç konumunun belirli bir düğüme nasıl taşınacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Run 1. ");

 // The document builder has a cursor, which acts as the part of the document
 // where the builder appends new nodes when we use its document construction methods.
 // This cursor functions in the same way as Microsoft Word's blinking cursor,
 // and it also always ends up immediately after any node that the builder just inserted.
 // To append content to a different part of the document,
 // we can move the cursor to a different node with the "MoveTo" method.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0));
 // The cursor is now in front of the node that we moved it to.
 // Adding a second run will insert it in front of the first run.
 builder.writeln("Run 2. ");

 Assert.assertEquals("Run 2. \rRun 1.", doc.getText().trim());

 // Move the cursor to the end of the document to continue appending text to the end as before.
 builder.moveTo(doc.getLastSection().getBody().getLastParagraph());
 builder.writeln("Run 3. ");

 Assert.assertEquals("Run 2. \rRun 1. \rRun 3.", doc.getText().trim());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node/) | Düğüm bir paragraf veya bir paragrafın doğrudan çocuğu olmalıdır. |

### moveToBookmark(String bookmarkName) {#moveToBookmark-java.lang.String}
```
public boolean moveToBookmark(String bookmarkName)
```


İmleci bir yer imine taşır.

 **Remarks:** 

İmleci belirtilen adla işaretçinin başlangıcının hemen sonrasındaki konuma taşır.

Karşılaştırma büyük/küçük harfe duyarlı değildir. İşaretçi bulunamazsa,  false  döndürülür ve imleç taşınmaz.

Yeni metin eklemek, işaretçinin mevcut metnini değiştirmez.

Belgedeki bazı işaretçilerin form alanlarına atandığını unutmayın. Böyle bir işaretçiye gidip metin eklemek, metni form alanı koduna ekler. Bu, form alanını geçersiz kılmasa da, eklenen metin alan kodunun bir parçası haline geldiği için görünmez.

 **Examples:** 

Bir belge oluşturucunun imlecini belgede farklı düğümlere taşımayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| bookmarkName | java.lang.String | İmlecin taşınacağı işaretçinin adı. |

**Returns:**
boolean -  true  işaretçi bulunursa;  false  aksi takdirde.
### moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter) {#moveToBookmark-java.lang.String-boolean-boolean}
```
public boolean moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)
```


İmleci daha yüksek hassasiyetle bir yer imine taşır.

 **Remarks:** 

İmleci işaretçinin başlangıcı ya da sonundan önce ya da sonrasına taşır.

İstenen konum satır içi seviyede değilse, bir sonraki paragrafa taşır.

Karşılaştırma büyük/küçük harfe duyarlı değildir. İşaretçi bulunamazsa,  false  döndürülür ve imleç taşınmaz.

 **Examples:** 

Bir document builder'ın düğüm ekleme noktası imlecinin bir işaretçiye nasıl taşınacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A valid bookmark consists of a BookmarkStart node, a BookmarkEnd node with a
 // matching bookmark name somewhere afterward, and contents enclosed by those nodes.
 builder.startBookmark("MyBookmark");
 builder.write("Hello world! ");
 builder.endBookmark("MyBookmark");

 // There are 4 ways of moving a document builder's cursor to a bookmark.
 // If we are between the BookmarkStart and BookmarkEnd nodes, the cursor will be inside the bookmark.
 // This means that any text added by the builder will become a part of the bookmark.
 // 1 -  Outside of the bookmark, in front of the BookmarkStart node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", true, false));
 builder.write("1. ");

 Assert.assertEquals("Hello world! ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. Hello world!", doc.getText().trim());

 // 2 -  Inside the bookmark, right after the BookmarkStart node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", true, true));
 builder.write("2. ");

 Assert.assertEquals("2. Hello world! ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. 2. Hello world!", doc.getText().trim());

 // 2 -  Inside the bookmark, right in front of the BookmarkEnd node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", false, false));
 builder.write("3. ");

 Assert.assertEquals("2. Hello world! 3. ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. 2. Hello world! 3.", doc.getText().trim());

 // 4 -  Outside of the bookmark, after the BookmarkEnd node:
 Assert.assertTrue(builder.moveToBookmark("MyBookmark", false, true));
 builder.write("4.");

 Assert.assertEquals("2. Hello world! 3. ", doc.getRange().getBookmarks().get("MyBookmark").getText());
 Assert.assertEquals("1. 2. Hello world! 3. 4.", doc.getText().trim());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| bookmarkName | java.lang.String | İmlecin taşınacağı işaretçinin adı. |
| isStart | boolean | true olduğunda, imleci işaretçinin başlangıcına taşır. false olduğunda, imleci işaretçinin sonuna taşır. |
| isAfter | boolean | true olduğunda, imleci işaretçinin başlangıç ya da bitiş konumundan sonrasına taşır. false olduğunda, imleci işaretçinin başlangıç ya da bitiş konumundan öncesine taşır. |

**Returns:**
boolean -  true  işaretçi bulunursa;  false  aksi takdirde.
### moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex) {#moveToCell-int-int-int-int}
```
public void moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```


İmleci geçerli bölümdeki bir tablo hücresine taşır.

 **Remarks:** 

Gezinme, geçerli bölümün geçerli hikayesi içinde gerçekleştirilir.

Dizin parametreleri için, dizin 0'a eşit veya büyük olduğunda, 0 ilk öğe olmak üzere baştan bir dizin belirtir. Dizin 0'dan küçük olduğunda, -1 son öğe olmak üzere sondan bir dizin belirtir.

 **Examples:** 

Bir document builder'ın imlecinin bir tablo hücresine nasıl taşınacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create an empty 2x2 table.
 builder.startTable();
 builder.insertCell();
 builder.insertCell();
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 // Because we have ended the table with the EndTable method,
 // the document builder's cursor is currently outside the table.
 // This cursor has the same function as Microsoft Word's blinking text cursor.
 // It can also be moved to a different location in the document using the builder's MoveTo methods.
 // We can move the cursor back inside the table to a specific cell.
 builder.moveToCell(0, 1, 1, 0);
 builder.write("Column 2, cell 2.");

 doc.save(getArtifactsDir() + "DocumentBuilder.MoveToCell.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableIndex | int | Taşınacak tablonun indeksi. |
| rowIndex | int | Tablodaki satırın dizini. |
| columnIndex | int | Tablodaki sütunun indeksi. |
| characterIndex | int | Hücre içindeki karakterin indeksi. Negatif bir değer, hücrenin sonundan bir konum belirtmenizi sağlar. Hücrenin sonuna gitmek için -1 kullanın. |

### moveToDocumentEnd() {#moveToDocumentEnd}
```
public void moveToDocumentEnd()
```


İmleci belgenin sonuna taşır.

 **Examples:** 

Bir belge oluşturucunun imlecini belgede farklı düğümlere taşımayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

### moveToDocumentStart() {#moveToDocumentStart}
```
public void moveToDocumentStart()
```


İmleci belgenin başına taşır.

 **Examples:** 

Bir belge oluşturucunun imlecini belgede farklı düğümlere taşımayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a valid bookmark, an entity that consists of nodes enclosed by a bookmark start node,
 // and a bookmark end node.
 builder.startBookmark("MyBookmark");
 builder.write("Bookmark contents.");
 builder.endBookmark("MyBookmark");

 NodeCollection firstParagraphNodes = doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(NodeType.BOOKMARK_START, firstParagraphNodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.RUN, firstParagraphNodes.get(1).getNodeType());
 Assert.assertEquals("Bookmark contents.", firstParagraphNodes.get(1).getText().trim());
 Assert.assertEquals(NodeType.BOOKMARK_END, firstParagraphNodes.get(2).getNodeType());

 // The document builder's cursor is always ahead of the node that we last added with it.
 // If the builder's cursor is at the end of the document, its current node will be null.
 // The previous node is the bookmark end node that we last added.
 // Adding new nodes with the builder will append them to the last node.
 Assert.assertNull(builder.getCurrentNode());

 // If we wish to edit a different part of the document with the builder,
 // we will need to bring its cursor to the node we wish to edit.
 builder.moveToBookmark("MyBookmark");

 // Moving it to a bookmark will move it to the first node within the bookmark start and end nodes, the enclosed run.
 Assert.assertEquals(firstParagraphNodes.get(1), builder.getCurrentNode());

 // We can also move the cursor to an individual node like this.
 builder.moveTo(doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.ANY, false).get(0));

 Assert.assertEquals(NodeType.BOOKMARK_START, builder.getCurrentNode().getNodeType());
 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph(), builder.getCurrentParagraph());
 Assert.assertTrue(builder.isAtStartOfParagraph());

 // We can use specific methods to move to the start/end of a document.
 builder.moveToDocumentEnd();

 Assert.assertTrue(builder.isAtEndOfParagraph());

 builder.moveToDocumentStart();

 Assert.assertTrue(builder.isAtStartOfParagraph());
 
```

### moveToField(Field field, boolean isAfter) {#moveToField-com.aspose.words.Field-boolean}
```
public void moveToField(Field field, boolean isAfter)
```


İmleci belgede bir alana taşır.

 **Examples:** 

Bir belge oluşturucusunun düğüm ekleme noktası imlecini belirli bir alana nasıl taşıyacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a field using the DocumentBuilder and add a run of text after it.
 Field field = builder.insertField(" AUTHOR \"John Doe\" ");

 // The builder's cursor is currently at end of the document.
 Assert.assertNull(builder.getCurrentNode());

 // Move the cursor to the field while specifying whether to place that cursor before or after the field.
 builder.moveToField(field, moveCursorToAfterTheField);

 // Note that the cursor is outside of the field in both cases.
 // This means that we cannot edit the field using the builder like this.
 // To edit a field, we can use the builder's MoveTo method on a field's FieldStart
 // or FieldSeparator node to place the cursor inside.
 if (moveCursorToAfterTheField) {
     Assert.assertNull(builder.getCurrentNode());
     builder.write(" Text immediately after the field.");

     Assert.assertEquals("AUTHOR \"John Doe\" John Doe Text immediately after the field.",
             doc.getText().trim());
 } else {
     Assert.assertEquals(field.getStart(), builder.getCurrentNode());
     builder.write("Text immediately before the field. ");

     Assert.assertEquals("Text immediately before the field.  AUTHOR \"John Doe\" John Doe",
             doc.getText().trim());
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field/) | İmlecin taşınacağı alan. |
| isAfter | boolean | true olduğunda, imleci alanın sonundan sonra konumlandırır. false olduğunda, imleci alanın başlangıcından önce konumlandırır. |

### moveToHeaderFooter(int headerFooterType) {#moveToHeaderFooter-int}
```
public void moveToHeaderFooter(int headerFooterType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| headerFooterType | int |  |

### moveToMergeField(String fieldName) {#moveToMergeField-java.lang.String}
```
public boolean moveToMergeField(String fieldName)
```


İmleci belirtilen birleştirme alanına taşır. İmleci belirtilen birleştirme alanının hemen ötesine konumlandırır ve birleştirme alanını kaldırır.

 **Remarks:** 

Bu yöntemin, imleci taşıdıktan sonra birleştirme alanını belgelerden sildiğine dikkat edin.

 **Examples:** 

Posta birleştirme yerine bir belge oluşturucu kullanarak MERGEFIELD'leri veri ile doldurmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

Posta birleştirme sırasında bir belgeye onay kutusu form alanları eklemenin nasıl yapılacağını gösterir.

```

 public void insertCheckBox() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.startTable();
     builder.insertCell();
     builder.insertField(" MERGEFIELD  TableStart:StudentCourse ");
     builder.insertCell();
     builder.insertField(" MERGEFIELD  CourseName ");
     builder.insertCell();
     builder.insertField(" MERGEFIELD  TableEnd:StudentCourse ");
     builder.endTable();

     // Add a handler for the MergeField event
     doc.getMailMerge().setFieldMergingCallback(new HandleMergeFieldInsertCheckBox());

     // Execute mail merge with regions
     DataTable dataTable = getStudentCourseDataTable();
     doc.getMailMerge().executeWithRegions(dataTable);

     // Save resulting document with a new name
     doc.save(getArtifactsDir() + "MailMergeEvent.InsertCheckBox.docx");
 }

 private class HandleMergeFieldInsertCheckBox implements IFieldMergingCallback {
     // This is called for each merge field in the document
     // when Document.MailMerge.ExecuteWithRegions is called.
     public void fieldMerging(final FieldMergingArgs args) throws Exception {
         if (args.getDocumentFieldName().equals("CourseName")) {
             // The name of the table that we are merging can be found here
             Assert.assertEquals(args.getTableName(), "StudentCourse");

             // Insert the checkbox for this merge field, using DocumentBuilder
             DocumentBuilder builder = new DocumentBuilder(args.getDocument());
             builder.moveToMergeField(args.getFieldName());
             builder.insertCheckBox(args.getDocumentFieldName() + mCheckBoxCount, false, 0);
             // Get the actual value of the field
             String fieldValue = args.getFieldValue().toString();

             // In this case, for every record index 'n', the corresponding field value is "Course n"
             Assert.assertEquals(args.getRecordIndex(), Character.getNumericValue(fieldValue.charAt(7)));

             builder.write(fieldValue);
             mCheckBoxCount++;
         }
     }

     public void imageFieldMerging(final ImageFieldMergingArgs args) {
         // Do nothing
     }

     // Counter for CheckBox name generation.
     private int mCheckBoxCount;
 }

 // Create DataTable and fill it with data.
 // In real life this DataTable should be filled from a database.
 private static DataTable getStudentCourseDataTable() throws Exception {
     DataTable dataTable = new DataTable("StudentCourse");
     dataTable.getColumns().add("CourseName");
     for (int i = 0; i < 10; i++) {
         DataRow datarow = dataTable.newRow();
         dataTable.getRows().add(datarow);
         datarow.set(0, "Course " + i);
     }
     return dataTable;
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldName | java.lang.String | Posta birleştirme alanının büyük/küçük harfe duyarsız adı. |

**Returns:**
boolean - merge alanı bulundu ve imleç taşındıysa true; aksi takdirde false.
### moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField) {#moveToMergeField-java.lang.String-boolean-boolean}
```
public boolean moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)
```


Birleştirme alanını belirtilen birleştirme alanına taşır.

 **Examples:** 

Alanları eklemenin ve belge oluşturucunun imlecini onlara taşımanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField("MERGEFIELD MyMergeField1 \\* MERGEFORMAT");
 builder.insertField("MERGEFIELD MyMergeField2 \\* MERGEFORMAT");

 // Move the cursor to the first MERGEFIELD.
 builder.moveToMergeField("MyMergeField1", true, false);

 // Note that the cursor is placed immediately after the first MERGEFIELD, and before the second.
 Assert.assertEquals(doc.getRange().getFields().get(1).getStart(), builder.getCurrentNode());
 Assert.assertEquals(doc.getRange().getFields().get(0).getEnd(), builder.getCurrentNode().getPreviousSibling());

 // If we wish to edit the field's field code or contents using the builder,
 // its cursor would need to be inside a field.
 // To place it inside a field, we would need to call the document builder's MoveTo method
 // and pass the field's start or separator node as an argument.
 builder.write(" Text between our merge fields. ");

 doc.save(getArtifactsDir() + "DocumentBuilder.MergeFields.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldName | java.lang.String | Posta birleştirme alanının büyük/küçük harfe duyarsız adı. |
| isAfter | boolean | true olduğunda, imleci alanın sonundan sonra konumlandırır. false olduğunda, imleci alanın başlangıcından önce konumlandırır. |
| isDeleteField | boolean | true olduğunda, birleştirme alanını siler. |

**Returns:**
boolean - merge alanı bulundu ve imleç taşındıysa true; aksi takdirde false.
### moveToParagraph(int paragraphIndex, int characterIndex) {#moveToParagraph-int-int}
```
public void moveToParagraph(int paragraphIndex, int characterIndex)
```


İmleci geçerli bölümdeki bir paragrafına taşır.

 **Remarks:** 

Gezinme, geçerli bölümün geçerli hikayesi içinde gerçekleştirilir. Yani, imleci ilk bölümün birincil başlığına taşıdıysanız, paragraphIndex o bölümün başlığı içindeki paragrafın indeksini belirtir.

paragraphIndex 0'a eşit veya büyük olduğunda, bölümenin başından bir indeks belirtir; 0 ilk paragraftır. paragraphIndex 0'dan küçük olduğunda, bölümenin sonundan bir indeks belirtir; -1 son paragraftır.

 **Examples:** 

Bir oluşturucunun imleç konumunu belirli bir paragrafa nasıl taşıyacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(22, paragraphs.getCount());

 // Create document builder to edit the document. The builder's cursor,
 // which is the point where it will insert new nodes when we call its document construction methods,
 // is currently at the beginning of the document.
 DocumentBuilder builder = new DocumentBuilder(doc);

 Assert.assertEquals(0, paragraphs.indexOf(builder.getCurrentParagraph()));

 // Move that cursor to a different paragraph will place that cursor in front of that paragraph.
 builder.moveToParagraph(2, 0);
 // Any new content that we add will be inserted at that point.
 builder.writeln("This is a new third paragraph. ");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| paragraphIndex | int | Taşınacak paragrafın indeksi. |
| characterIndex | int | Paragraf içindeki karakterin indeksi. Negatif bir değer, paragrafın sonundan bir konum belirtmenizi sağlar. Paragrafın sonuna gitmek için -1 kullanın. |

### moveToSection(int sectionIndex) {#moveToSection-int}
```
public void moveToSection(int sectionIndex)
```


İmleci belirtilen bölümdeki gövdenin başına taşır.

 **Remarks:** 

sectionIndex 0'a eşit veya büyük olduğunda, belgenin başından bir indeks belirtir; 0 ilk bölümdür. sectionIndex 0'dan küçük olduğunda, belgenin sonundan bir indeks belirtir; -1 son bölümdür.

İmleç, belirtilen bölümün [Body](../../com.aspose.words/body/) içindeki ilk paragrafına taşınır.

 **Examples:** 

DocumentBuilder kullanarak bir belgede üstbilgi ve altbilgi nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sectionIndex | int | Taşınacak bölümün indeksi. |

### moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex) {#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int}
```
public void moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)
```


İmleci yapılandırılmış belge etiketine taşır.

 **Examples:** 

DocumentBuilder'ın imlecini yapılandırılmış belge etiketi içinde taşımayı gösterir.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| structuredDocumentTag | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/) | Taşınacak yapılandırılmış belge etiketi. |
| characterIndex | int | Yapılandırılmış belge etiketi içindeki karakterin indeksi. Negatif bir değer, etiketin sonundan bir konum belirtmenizi sağlar. Etiketin sonuna gitmek için -1 kullanın. Etiket blok seviyesindeyse ve imleci son paragrafının sonuna taşımak istiyorsanız, -2 belirtin. |

### moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex) {#moveToStructuredDocumentTag-int-int}
```
public void moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```


İmleci geçerli bölümdeki bir yapılandırılmış belge etiketine taşır.

 **Remarks:** 

Gezinme, geçerli bölümün geçerli hikayesi içinde gerçekleştirilir. Yani, imleci ilk bölümün birincil başlığına taşıdıysanız, structuredDocumentTagIndex o bölümün başlığı içindeki yapılandırılmış belge etiketinin indeksini belirtir.

structuredDocumentTagIndex 0'a eşit veya büyük olduğunda, bölümün başından bir indeks belirtir; 0 ilk yapılandırılmış belge etiketidir. structuredDocumentTagIndex 0'dan küçük olduğunda, bölümün sonundan bir indeks belirtir; -1 son yapılandırılmış belge etiketidir.

 **Examples:** 

DocumentBuilder'ın imlecini yapılandırılmış belge etiketi içinde taşımayı gösterir.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 // There is a several ways to move the cursor:
 // 1 -  Move to the first character of structured document tag by index.
 builder.moveToStructuredDocumentTag(1, 1);

 // 2 -  Move to the first character of structured document tag by object.
 StructuredDocumentTag tag = (StructuredDocumentTag)doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 2, true);
 builder.moveToStructuredDocumentTag(tag, 1);
 builder.write(" New text.");

 Assert.assertEquals("R New text.ichText", tag.getText().trim());

 // 3 -  Move to the end of the second structured document tag.
 builder.moveToStructuredDocumentTag(1, -1);
 Assert.assertTrue(builder.isAtEndOfStructuredDocumentTag());

 // Get currently selected structured document tag.
 builder.getCurrentStructuredDocumentTag().setColor(Color.GREEN);

 doc.save(getArtifactsDir() + "Document.MoveToStructuredDocumentTag.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| structuredDocumentTagIndex | int | Taşınacak yapılandırılmış belge etiketinin indeksi. |
| characterIndex | int | Yapılandırılmış belge etiketi içindeki karakterin indeksi. Negatif bir değer, etiketin sonundan bir konum belirtmenizi sağlar. Etiketin sonuna gitmek için -1 kullanın. Etiket blok seviyesindeyse ve imleci son paragrafının sonuna taşımak istiyorsanız, -2 belirtin. |

### popFont() {#popFont}
```
public void popFont()
```


Yığına daha önce kaydedilen karakter biçimlendirmesini alır.

 **Examples:** 

Bir DocumentBuilder'ın biçimlendirme yığını nasıl kullanılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set up font formatting, then write the text that goes before the hyperlink.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(24.0);
 builder.write("To visit Google, hold Ctrl and click ");

 // Preserve our current formatting configuration on the stack.
 builder.pushFont();

 // Alter the builder's current formatting by applying a new style.
 builder.getFont().setStyleIdentifier(StyleIdentifier.HYPERLINK);
 builder.insertHyperlink("here", "http://www.google.com", false);

 Assert.assertEquals(Color.BLUE.getRGB(), builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.SINGLE, builder.getFont().getUnderline());

 // Restore the font formatting that we saved earlier and remove the element from the stack.
 builder.popFont();

 Assert.assertEquals(0, builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.NONE, builder.getFont().getUnderline());

 builder.write(". We hope you enjoyed the example.");

 doc.save(getArtifactsDir() + "DocumentBuilder.PushPopFont.docx");
 
```

### pushFont() {#pushFont}
```
public void pushFont()
```


Geçerli karakter biçimlendirmesini yığına kaydeder.

 **Examples:** 

Bir DocumentBuilder'ın biçimlendirme yığını nasıl kullanılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set up font formatting, then write the text that goes before the hyperlink.
 builder.getFont().setName("Arial");
 builder.getFont().setSize(24.0);
 builder.write("To visit Google, hold Ctrl and click ");

 // Preserve our current formatting configuration on the stack.
 builder.pushFont();

 // Alter the builder's current formatting by applying a new style.
 builder.getFont().setStyleIdentifier(StyleIdentifier.HYPERLINK);
 builder.insertHyperlink("here", "http://www.google.com", false);

 Assert.assertEquals(Color.BLUE.getRGB(), builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.SINGLE, builder.getFont().getUnderline());

 // Restore the font formatting that we saved earlier and remove the element from the stack.
 builder.popFont();

 Assert.assertEquals(0, builder.getFont().getColor().getRGB());
 Assert.assertEquals(Underline.NONE, builder.getFont().getUnderline());

 builder.write(". We hope you enjoyed the example.");

 doc.save(getArtifactsDir() + "DocumentBuilder.PushPopFont.docx");
 
```

### removeParaAttr(int key) {#removeParaAttr-int}
```
public void removeParaAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |

### resetToDefaultAttrs() {#resetToDefaultAttrs}
```
public void resetToDefaultAttrs()
```




### setBold(boolean value) {#setBold-boolean}
```
public void setBold(boolean value)
```


Yazı tipi kalın olarak biçimlendirilmişse True.

 **Examples:** 

Posta birleştirme yerine bir belge oluşturucu kullanarak MERGEFIELD'leri veri ile doldurmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object}
```
public void setCellAttr(int key, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

### setDocument(Document value) {#setDocument-com.aspose.words.Document}
```
public void setDocument(Document value)
```


Bu nesnenin bağlı olduğu [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) nesnesini ayarlar.

 **Examples:** 

Bir belgede bölümlere sayfa ayarı seçeneklerini uygulama ve geri alma işlemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [Document](../../com.aspose.words/document/) | Bu nesnenin bağlı olduğu [getDocument()](../../com.aspose.words/documentbuilder/\#getDocument) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder/\#setDocument-com.aspose.words.Document) nesnesi. |

### setItalic(boolean value) {#setItalic-boolean}
```
public void setItalic(boolean value)
```


Yazı tipi italik olarak biçimlendirilmişse doğrudur.

 **Examples:** 

Posta birleştirme yerine bir belge oluşturucu kullanarak MERGEFIELD'leri veri ile doldurmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some MERGEFIELDS, which accept data from columns of the same name in a data source during a mail merge,
 // and then fill them manually.
 builder.insertField(" MERGEFIELD Chairman ");
 builder.insertField(" MERGEFIELD ChiefFinancialOfficer ");
 builder.insertField(" MERGEFIELD ChiefTechnologyOfficer ");

 builder.moveToMergeField("Chairman");
 builder.setBold(true);
 builder.writeln("John Doe");

 builder.moveToMergeField("ChiefFinancialOfficer");
 builder.setItalic(true);
 builder.writeln("Jane Doe");

 builder.moveToMergeField("ChiefTechnologyOfficer");
 builder.setItalic(true);
 builder.writeln("John Bloggs");

 doc.save(getArtifactsDir() + "DocumentBuilder.FillMergeFields.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object}
```
public void setRowAttr(int key, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | int |  |
| değer | java.lang.Object |  |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int fontAttr, Object value)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontAttr | int |  |
| değer | java.lang.Object |  |

### setUnderline(int value) {#setUnderline-int}
```
public void setUnderline(int value)
```


Geçerli yazı tipi için alt çizgi tipini alır/ayarlar.

 **Examples:** 

Bir belge oluşturucu tarafından eklenen metni biçimlendirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.setUnderline(Underline.DASH);
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setSize(32.0);

 // The builder applies formatting to its current paragraph and any new text added by it afterward.
 builder.writeln("Large, blue, and underlined text.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertUnderline.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer, [Underline](../../com.aspose.words/underline/) sabitlerinden biri olmalıdır. |

### startBookmark(String bookmarkName) {#startBookmark-java.lang.String}
```
public BookmarkStart startBookmark(String bookmarkName)
```


Belgedeki geçerli konumu bir yer imi başlangıcı olarak işaretler.

 **Remarks:** 

Bir belgede yer imleri çakışabilir ve herhangi bir aralığı kapsayabilir. Geçerli bir yer imi oluşturmak için aynı bookmarkName parametresiyle hem [startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startBookmark-java.lang.String) hem de [endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endBookmark-java.lang.String) metodlarını çağırmanız gerekir.

Kötü biçimlendirilmiş yer imleri veya aynı ada sahip yer imleri belge kaydedildiğinde yok sayılacaktır.

 **Examples:** 

Bir yer imi oluşturmanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A valid bookmark needs to have document body text enclosed by
 // BookmarkStart and BookmarkEnd nodes created with a matching bookmark name.
 builder.startBookmark("MyBookmark");
 builder.writeln("Hello world!");
 builder.endBookmark("MyBookmark");

 Assert.assertEquals(1, doc.getRange().getBookmarks().getCount());
 Assert.assertEquals("MyBookmark", doc.getRange().getBookmarks().get(0).getName());
 Assert.assertEquals("Hello world!", doc.getRange().getBookmarks().get(0).getText().trim());
 
```

Yerel bir yer imine referans veren bir köprü eklemenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startBookmark("Bookmark1");
 builder.write("Bookmarked text. ");
 builder.endBookmark("Bookmark1");
 builder.writeln("Text outside of the bookmark.");

 // Insert a HYPERLINK field that links to the bookmark. We can pass field switches
 // to the "InsertHyperlink" method as part of the argument containing the referenced bookmark's name.
 builder.getFont().setColor(Color.BLUE);
 builder.getFont().setUnderline(Underline.SINGLE);
 FieldHyperlink hyperlink = (FieldHyperlink)builder.insertHyperlink("Link to Bookmark1", "Bookmark1", true);
 hyperlink.setScreenTip("Hyperlink Tip");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| bookmarkName | java.lang.String | Yer iminin adı. |

**Returns:**
[BookmarkStart](../../com.aspose.words/bookmarkstart/) - The bookmark start node that was just created.
### startColumnBookmark(String bookmarkName) {#startColumnBookmark-java.lang.String}
```
public BookmarkStart startColumnBookmark(String bookmarkName)
```


Belgedeki mevcut konumu bir sütun yer imi başlangıcı olarak işaretler. Konum bir tablo hücresinde olmalıdır.

 **Remarks:** 

Bir sütun yer imi, satır aralığında bir veya daha fazla sütunu kapsar. Geçerli bir yer imi oluşturmak için aynı bookmarkName parametresiyle hem [startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#startColumnBookmark-java.lang.String) hem de [endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder/\#endColumnBookmark-java.lang.String) metodlarını çağırmanız gerekir.

Kötü biçimlendirilmiş yer imleri veya aynı ada sahip yer imleri belge kaydedildiğinde yok sayılacaktır.

Eklenen [BookmarkStart](../../com.aspose.words/bookmarkstart/) düğümünün gerçek konumu, mevcut belge oluşturucu konumundan farklı olabilir.

 **Examples:** 

Bir sütun yer işareti oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 builder.insertCell();
 // Cells 1,2,4,5 will be bookmarked.
 builder.startColumnBookmark("MyBookmark_1");
 // Badly formed bookmarks or bookmarks with duplicate names will be ignored when the document is saved.
 builder.startColumnBookmark("MyBookmark_1");
 builder.startColumnBookmark("BadStartBookmark");
 builder.write("Cell 1");

 builder.insertCell();
 builder.write("Cell 2");

 builder.insertCell();
 builder.write("Cell 3");

 builder.endRow();

 builder.insertCell();
 builder.write("Cell 4");

 builder.insertCell();
 builder.write("Cell 5");
 builder.endColumnBookmark("MyBookmark_1");
 builder.endColumnBookmark("MyBookmark_1");

 builder.insertCell();
 builder.write("Cell 6");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "Bookmarks.CreateColumnBookmark.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| bookmarkName | java.lang.String | Yer iminin adı. |

**Returns:**
[BookmarkStart](../../com.aspose.words/bookmarkstart/) - The bookmark start node that was just created.
### startEditableRange() {#startEditableRange}
```
public EditableRangeStart startEditableRange()
```


Belge içinde geçerli konumu düzenlenebilir bir aralık başlangıcı olarak işaretler.

 **Remarks:** 

Bir belgede düzenlenebilir aralık çakışabilir ve herhangi bir aralığı kapsayabilir. Geçerli bir düzenlenebilir aralık oluşturmak için hem [startEditableRange()](../../com.aspose.words/documentbuilder/\#startEditableRange) hem de [endEditableRange()](../../com.aspose.words/documentbuilder/\#endEditableRange) ya da [endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder/\#endEditableRange-com.aspose.words.EditableRangeStart) yöntemlerini çağırmanız gerekir.

Kötü biçimlendirilmiş düzenlenebilir aralık, belge kaydedildiğinde yok sayılacaktır.

 **Examples:** 

Düzenlenebilir bir aralıkla nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only," +
         " we cannot edit this paragraph without the password.");

 // Editable ranges allow us to leave parts of protected documents open for editing.
 EditableRangeStart editableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph is inside an editable range, and can be edited.");
 EditableRangeEnd editableRangeEnd = builder.endEditableRange();

 // A well-formed editable range has a start node, and end node.
 // These nodes have matching IDs and encompass editable nodes.
 EditableRange editableRange = editableRangeStart.getEditableRange();

 Assert.assertEquals(editableRangeStart.getId(), editableRange.getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getId());

 // Different parts of the editable range link to each other.
 Assert.assertEquals(editableRangeStart.getId(), editableRange.getEditableRangeStart().getId());
 Assert.assertEquals(editableRangeStart.getId(), editableRangeEnd.getEditableRangeStart().getId());
 Assert.assertEquals(editableRange.getId(), editableRangeStart.getEditableRange().getId());
 Assert.assertEquals(editableRangeEnd.getId(), editableRange.getEditableRangeEnd().getId());

 // We can access the node types of each part like this. The editable range itself is not a node,
 // but an entity which consists of a start, an end, and their enclosed contents.
 Assert.assertEquals(NodeType.EDITABLE_RANGE_START, editableRangeStart.getNodeType());
 Assert.assertEquals(NodeType.EDITABLE_RANGE_END, editableRangeEnd.getNodeType());

 builder.writeln("This paragraph is outside the editable range, and cannot be edited.");

 doc.save(getArtifactsDir() + "EditableRange.CreateAndRemove.docx");

 // Remove an editable range. All the nodes that were inside the range will remain intact.
 editableRange.remove();
 
```

İç içe düzenlenebilir aralıkların nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "MyPassword");

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! Since we have set the document's protection level to read-only, " +
         "we cannot edit this paragraph without the password.");

 // Create two nested editable ranges.
 EditableRangeStart outerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 EditableRangeStart innerEditableRangeStart = builder.startEditableRange();
 builder.writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

 // Currently, the document builder's node insertion cursor is in more than one ongoing editable range.
 // When we want to end an editable range in this situation,
 // we need to specify which of the ranges we wish to end by passing its EditableRangeStart node.
 builder.endEditableRange(innerEditableRangeStart);

 builder.writeln("This paragraph inside the outer editable range and can be edited.");

 builder.endEditableRange(outerEditableRangeStart);

 builder.writeln("This paragraph is outside any editable ranges, and cannot be edited.");

 // If a region of text has two overlapping editable ranges with specified groups,
 // the combined group of users excluded by both groups are prevented from editing it.
 outerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.EVERYONE);
 innerEditableRangeStart.getEditableRange().setEditorGroup(EditorType.CONTRIBUTORS);

 doc.save(getArtifactsDir() + "EditableRange.Nested.docx");
 
```

**Returns:**
[EditableRangeStart](../../com.aspose.words/editablerangestart/) - The editable range start node that was just created.
### startTable() {#startTable}
```
public Table startTable()
```


Belge içinde bir tablo başlatır.

 **Remarks:** 

Bir sonraki çağrılacak yöntem [insertCell()](../../com.aspose.words/documentbuilder/\#insertCell).

Bu yöntem, bir hücre içinde çağrıldığında iç içe bir tablo başlatır.

 **Examples:** 

Özel kenarlıklarla bir tablo oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Biçimlendirilmiş 2x2 bir tablo nasıl oluşturulur gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

Bir belge oluşturucu ile hücreleri biçimlendirmeyi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Insert a second cell, and then configure cell text padding options.
 // The builder will apply these settings at its current cell, and any new cells creates afterwards.
 builder.insertCell();

 CellFormat cellFormat = builder.getCellFormat();
 cellFormat.setWidth(250.0);
 cellFormat.setLeftPadding(30.0);
 cellFormat.setRightPadding(30.0);
 cellFormat.setTopPadding(30.0);
 cellFormat.setBottomPadding(30.0);

 builder.write("Row 1, cell 2.");
 builder.endRow();
 builder.endTable();

 // The first cell was unaffected by the padding reconfiguration, and still holds the default values.
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getWidth());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getLeftPadding());
 Assert.assertEquals(5.4d, table.getFirstRow().getCells().get(0).getCellFormat().getRightPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getTopPadding());
 Assert.assertEquals(0.0d, table.getFirstRow().getCells().get(0).getCellFormat().getBottomPadding());

 Assert.assertEquals(250.0d, table.getFirstRow().getCells().get(1).getCellFormat().getWidth());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getLeftPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getRightPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getTopPadding());
 Assert.assertEquals(30.0d, table.getFirstRow().getCells().get(1).getCellFormat().getBottomPadding());

 // The first cell will still grow in the output document to match the size of its neighboring cell.
 doc.save(getArtifactsDir() + "DocumentBuilder.SetCellFormatting.docx");
 
```

**Returns:**
[Table](../../com.aspose.words/table/) - The table node that was just created.
### write(String text) {#write-java.lang.String}
```
public void write(String text)
```


Geçerli ekleme konumunda bir dizeyi belgeye ekler.

 **Remarks:** 

[getFont()](../../com.aspose.words/documentbuilder/\#getFont) özelliği tarafından belirtilen mevcut yazı tipi biçimlendirmesi kullanılır.

 **Examples:** 

Bir dizeyi kenarlıkla çevreleyerek belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().getBorder().setColor(Color.GREEN);
 builder.getFont().getBorder().setLineWidth(2.5);
 builder.getFont().getBorder().setLineStyle(LineStyle.DASH_DOT_STROKER);

 builder.write("Text surrounded by green border.");

 doc.save(getArtifactsDir() + "Border.FontBorder.docx");
 
```

Özel kenarlıklarla bir tablo oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.startTable();

 // Setting table formatting options for a document builder
 // will apply them to every row and cell that we add with it.
 builder.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 builder.getCellFormat().clearFormatting();
 builder.getCellFormat().setWidth(150.0);
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.getCellFormat().setWrapText(false);
 builder.getCellFormat().setFitText(true);

 builder.getRowFormat().clearFormatting();
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getRowFormat().setHeight(50.0);
 builder.getRowFormat().getBorders().setLineStyle(LineStyle.ENGRAVE_3_D);
 builder.getRowFormat().getBorders().setColor(Color.ORANGE);

 builder.insertCell();
 builder.write("Row 1, Col 1");

 builder.insertCell();
 builder.write("Row 1, Col 2");
 builder.endRow();

 // Changing the formatting will apply it to the current cell,
 // and any new cells that we create with the builder afterward.
 // This will not affect the cells that we have added previously.
 builder.getCellFormat().getShading().clearFormatting();

 builder.insertCell();
 builder.write("Row 2, Col 1");

 builder.insertCell();
 builder.write("Row 2, Col 2");

 builder.endRow();

 // Increase row height to fit the vertical text.
 builder.insertCell();
 builder.getRowFormat().setHeight(150.0);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 3, Col 1");

 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 3, Col 2");

 builder.endRow();
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTable.docx");
 
```

Bir belge oluşturucusunu kullanarak tablo oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Start the table, then populate the first row with two cells.
 builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1.");
 builder.insertCell();
 builder.write("Row 1, Cell 2.");

 // Call the builder's "EndRow" method to start a new row.
 builder.endRow();
 builder.insertCell();
 builder.write("Row 2, Cell 1.");
 builder.insertCell();
 builder.write("Row 2, Cell 2.");
 builder.endTable();

 doc.save(getArtifactsDir() + "DocumentBuilder.CreateTable.docx");
 
```

Biçimlendirilmiş 2x2 bir tablo nasıl oluşturulur gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| metin | java.lang.String | Belgeye eklenecek dize. |

### writeln() {#writeln}
```
public void writeln()
```


Belgeye bir paragraf sonu ekler.

 **Remarks:** 

[insertParagraph()](../../com.aspose.words/documentbuilder/\#insertParagraph) çağrılır.

 **Examples:** 

DocumentBuilder kullanarak bir belgede üstbilgi ve altbilgi nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

### writeln(String text) {#writeln-java.lang.String}
```
public void writeln(String text)
```


Belgeye bir dize ve bir paragraf sonu ekler.

 **Remarks:** 

[getFont()](../../com.aspose.words/documentbuilder/\#getFont) ve [getParagraphFormat()](../../com.aspose.words/documentbuilder/\#getParagraphFormat) özellikleri tarafından belirtilen mevcut yazı tipi ve paragraf biçimlendirmesi kullanılır.

 **Examples:** 

Biçimlendirilmiş 2x2 bir tablo nasıl oluşturulur gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.getCellFormat().setVerticalAlignment(CellVerticalAlignment.CENTER);
 builder.write("Row 1, cell 1.");
 builder.insertCell();
 builder.write("Row 1, cell 2.");
 builder.endRow();

 // While building the table, the document builder will apply its current RowFormat/CellFormat property values
 // to the current row/cell that its cursor is in and any new rows/cells as it creates them.
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(0).getCellFormat().getVerticalAlignment());
 Assert.assertEquals(CellVerticalAlignment.CENTER, table.getRows().get(0).getCells().get(1).getCellFormat().getVerticalAlignment());

 builder.insertCell();
 builder.getRowFormat().setHeight(100.0);
 builder.getRowFormat().setHeightRule(HeightRule.EXACTLY);
 builder.getCellFormat().setOrientation(TextOrientation.UPWARD);
 builder.write("Row 2, cell 1.");
 builder.insertCell();
 builder.getCellFormat().setOrientation(TextOrientation.DOWNWARD);
 builder.write("Row 2, cell 2.");
 builder.endRow();
 builder.endTable();

 // Previously added rows and cells are not retroactively affected by changes to the builder's formatting.
 Assert.assertEquals(0.0, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());
 Assert.assertEquals(100.0, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());
 Assert.assertEquals(TextOrientation.UPWARD, table.getRows().get(1).getCells().get(0).getCellFormat().getOrientation());
 Assert.assertEquals(TextOrientation.DOWNWARD, table.getRows().get(1).getCells().get(1).getCellFormat().getOrientation());

 doc.save(getArtifactsDir() + "DocumentBuilder.BuildTable.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| metin | java.lang.String | Belgeye eklenecek dize. |

