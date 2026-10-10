---
title: "ImportFormatOptions"
linktitle: "ImportFormatOptions"
second_title: "Aspose.Words für Java"
description: "Ermöglicht die Angabe verschiedener Importoptionen zur Formatierung der Ausgabe in Java."
type: docs
weight: 401
url: /de/java/com.aspose.words/importformatoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatOptions
```

Ermöglicht das Angeben verschiedener Importoptionen zur Formatierung der Ausgabe.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Specify Load Options ][Specify Load Options].

 **Examples:** 

Zeigt, wie doppelte Formatvorlagen beim Einfügen von Dokumenten aufgelöst werden können.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAdjustSentenceAndWordSpacing()](#getAdjustSentenceAndWordSpacing) | Gibt einen booleschen Wert zurück, der angibt, ob Satz- und Wortabstände automatisch angepasst werden sollen. |
| [getAppendDocumentWithNewPage()](#getAppendDocumentWithNewPage) | Gibt einen booleschen Wert zurück, der angibt, ob beim Aufruf von **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** der Typ des zuerst importierten Abschnitts zwangsweise zu [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) geändert werden soll. |
| [getForceCopyStyles()](#getForceCopyStyles) | Gibt einen booleschen Wert zurück, der angibt, ob widersprüchliche Formatvorlagen im Modus [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) kopiert werden sollen. |
| [getIgnoreHeaderFooter()](#getIgnoreHeaderFooter) | Gibt einen booleschen Wert zurück, der angibt, dass die Quellformatierung von Kopf-/Fußzeileninhalten ignoriert wird, wenn der Modus [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) verwendet wird. |
| [getIgnoreTextBoxes()](#getIgnoreTextBoxes) | Gibt einen booleschen Wert zurück, der angibt, dass die Quellformatierung des Inhalts von Textfeldern ignoriert wird, wenn der Modus [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) verwendet wird. |
| [getKeepSourceNumbering()](#getKeepSourceNumbering) | Gibt einen booleschen Wert zurück, der angibt, wie die Nummerierung importiert wird, wenn sie in Quell- und Zieldokumenten kollidiert. |
| [getMergePastedLists()](#getMergePastedLists) | Gibt einen booleschen Wert zurück, der angibt, ob eingefügte Listen mit umgebenden Listen zusammengeführt werden. |
| [getResolveThemeColors()](#getResolveThemeColors) | Gibt einen booleschen Wert zurück, der angibt, ob die Themenfarben der Formen zwangsweise aufgelöst werden sollen. |
| [getSmartStyleBehavior()](#getSmartStyleBehavior) | Gibt einen booleschen Wert zurück, der angibt, wie Stile importiert werden, wenn sie in Quell- und Zieldokumenten gleiche Namen haben. |
| [setAdjustSentenceAndWordSpacing(boolean value)](#setAdjustSentenceAndWordSpacing-boolean) | Legt einen booleschen Wert fest, der angibt, ob Satz‑ und Wortabstände automatisch angepasst werden sollen. |
| [setAppendDocumentWithNewPage(boolean value)](#setAppendDocumentWithNewPage-boolean) | Legt einen booleschen Wert fest, der angibt, ob der Typ des zuerst importierten Abschnitts zwangsweise in [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) geändert werden soll, wenn die Methode **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** aufgerufen wird. |
| [setForceCopyStyles(boolean value)](#setForceCopyStyles-boolean) | Legt einen booleschen Wert fest, der angibt, ob widersprüchliche Stile im Modus [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) kopiert werden sollen. |
| [setIgnoreHeaderFooter(boolean value)](#setIgnoreHeaderFooter-boolean) | Legt einen booleschen Wert fest, der angibt, dass die Quellformatierung des Inhalts von Kopf‑/Fußzeilen ignoriert wird, wenn der Modus [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) verwendet wird. |
| [setIgnoreTextBoxes(boolean value)](#setIgnoreTextBoxes-boolean) | Legt einen booleschen Wert fest, der angibt, dass die Quellformatierung des Inhalts von Textfeldern ignoriert wird, wenn der Modus [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) verwendet wird. |
| [setKeepSourceNumbering(boolean value)](#setKeepSourceNumbering-boolean) | Legt einen booleschen Wert fest, der angibt, wie die Nummerierung importiert wird, wenn sie in Quell- und Zieldokumenten kollidiert. |
| [setMergePastedLists(boolean value)](#setMergePastedLists-boolean) | Legt einen booleschen Wert fest, der angibt, ob eingefügte Listen mit umgebenden Listen zusammengeführt werden. |
| [setResolveThemeColors(boolean value)](#setResolveThemeColors-boolean) | Legt einen booleschen Wert fest, der angibt, ob die Themenfarben der Formen zwangsweise aufgelöst werden sollen. |
| [setSmartStyleBehavior(boolean value)](#setSmartStyleBehavior-boolean) | Legt einen booleschen Wert fest, der angibt, wie Stile importiert werden, wenn sie in Quell- und Zieldokumenten gleiche Namen haben. |
### getAdjustSentenceAndWordSpacing() {#getAdjustSentenceAndWordSpacing}
```
public boolean getAdjustSentenceAndWordSpacing()
```


Gibt einen booleschen Wert zurück, der angibt, ob Satz‑ und Wortabstände automatisch angepasst werden sollen. Der Standardwert ist false.

 **Examples:** 

Zeigt, wie Satz‑ und Wortabstände automatisch angepasst werden können.

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
boolesch - Ein boolescher Wert, der angibt, ob Satz‑ und Wortabstände automatisch angepasst werden sollen.
### getAppendDocumentWithNewPage() {#getAppendDocumentWithNewPage}
```
public boolean getAppendDocumentWithNewPage()
```


Gibt einen booleschen Wert zurück, der angibt, ob beim Aufruf von **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** der Typ des zuerst importierten Abschnitts zwangsweise zu [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) geändert werden soll.

Der Standardwert ist  true .

 **Remarks:** 

Bitte beachten Sie, dass diese Option nur für die Methode **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** relevant ist und keine Wirkung auf andere importbezogene Methoden hat.

 **Examples:** 

Zeigt, wie der ursprüngliche Abschnittstyp beibehalten wird.

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
boolesch - Ein boolescher Wert, der angibt, ob der Typ des zuerst importierten Abschnitts zwangsweise in [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) geändert werden soll, wenn die Methode **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** aufgerufen wird.
### getForceCopyStyles() {#getForceCopyStyles}
```
public boolean getForceCopyStyles()
```


Gibt einen booleschen Wert zurück, der angibt, ob Konfliktstile im [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING)-Modus kopiert werden sollen. Der Standardwert ist false.

 **Remarks:** 

Standardmäßig, wenn ein passender Stil bereits in einem Zieldokument existiert, wird die Formatierung des Quellstils in direkte Knoteneigenschaften expandiert und der Stil dieses Knotens auf den Standard zurückgesetzt.

Wenn diese Option auf true gesetzt ist, wird der Quellstil zwangsweise in das Zieldokument mit einem eindeutigen Namen kopiert und auf den importierten Knoten angewendet.

Hinweis: In diesem Fall ist nicht garantiert, dass die Formatierung des importierten Knotens im Zieldokument erhalten bleibt.

 **Examples:** 

Zeigt, wie Quellstile mit eindeutigen Namen zwangsweise kopiert werden.

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
boolean - Ein boolescher Wert, der angibt, ob Konfliktstile im [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING)-Modus kopiert werden sollen.
### getIgnoreHeaderFooter() {#getIgnoreHeaderFooter}
```
public boolean getIgnoreHeaderFooter()
```


Gibt einen booleschen Wert zurück, der angibt, dass die Quellformatierung des Inhalts von Kopf‑ und Fußzeilen ignoriert wird, wenn der [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING)-Modus verwendet wird. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie das Ignorieren oder Nicht‑Ignorieren der Quellformatierung des Inhalts von Kopf‑ und Fußzeilen angegeben wird.

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
boolean - Ein boolescher Wert, der angibt, dass die Quellformatierung des Inhalts von Kopf‑ und Fußzeilen ignoriert wird, wenn der [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING)-Modus verwendet wird.
### getIgnoreTextBoxes() {#getIgnoreTextBoxes}
```
public boolean getIgnoreTextBoxes()
```


Gibt einen booleschen Wert zurück, der angibt, dass die Quellformatierung des Inhalts von Textfeldern ignoriert wird, wenn der [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING)-Modus verwendet wird. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie die Formatierung von Textfeldern beim Anhängen eines Dokuments verwaltet wird.

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
boolean - Ein boolescher Wert, der angibt, dass die Quellformatierung des Inhalts von Textfeldern ignoriert wird, wenn der [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING)-Modus verwendet wird.
### getKeepSourceNumbering() {#getKeepSourceNumbering}
```
public boolean getKeepSourceNumbering()
```


Gibt einen booleschen Wert zurück, der angibt, wie die Nummerierung importiert wird, wenn sie in Quell‑ und Zieldokumenten kollidiert. Der Standardwert ist false.

 **Examples:** 

Zeigt, wie ein Dokument mit nummerierten Listen importiert wird.

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

Zeigt, wie ein Konflikt beim Importieren von Dokumenten gelöst wird, die Listen mit derselben Listendefinitions‑Kennung besitzen.

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

Zeigt, wie Listennummerierungskonflikte in Quell‑ und Zieldokumenten gelöst werden.

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
boolean - Ein boolescher Wert, der angibt, wie die Nummerierung importiert wird, wenn sie in Quell‑ und Zieldokumenten kollidiert.
### getMergePastedLists() {#getMergePastedLists}
```
public boolean getMergePastedLists()
```


Gibt einen booleschen Wert zurück, der angibt, ob eingefügte Listen mit umgebenden Listen zusammengeführt werden. Der Standardwert ist false.

 **Examples:** 

Zeigt, wie Listen aus einem Dokument zusammengeführt werden.

```

 Document srcDoc = new Document(getMyDir() + "List item.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setMergePastedLists(true); }

 // Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 dstDoc.save(getArtifactsDir() + "Document.MergePastedLists.docx");
 
```

**Returns:**
boolean - Ein boolescher Wert, der angibt, ob eingefügte Listen mit umgebenden Listen zusammengeführt werden.
### getResolveThemeColors() {#getResolveThemeColors}
```
public boolean getResolveThemeColors()
```


Gibt einen booleschen Wert zurück, der angibt, ob die Themenfarben der Formen zwangsweise aufgelöst werden sollen. Der Standardwert ist false.

 **Remarks:** 

Bitte beachten Sie, dass diese Option nur für den [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING)-Modus relevant ist.

Normalerweise löst Aspose.Words keine Quell‑Themenfarben auf, wenn beim Importieren von Stilen diese erhalten bleiben können, ohne Formatierungsattribute in direkte zu expandieren. In diesem Fall können jedoch die tatsächlichen Farben der importierten Formen von denen im Originaldokument abweichen. Der Grund dafür sind die unterschiedlichen Themenfarben in den Quell‑ und Zieldokumenten. Das Setzen dieser Option auf  true  zwingt die Auflösung der Quell‑Formen‑Themenfarben und bewahrt somit die tatsächliche Farbe der Formen, die sie im Quelldokument haben.

 **Examples:** 

Zeigt, wie ein Knoten mit Auflösung der Quell‑Themenfarben von Formen importiert wird.

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
boolean – Ein boolescher Wert, der angibt, ob die Themenfarben der Formen zwangsweise aufgelöst werden sollen.
### getSmartStyleBehavior() {#getSmartStyleBehavior}
```
public boolean getSmartStyleBehavior()
```


Gibt einen booleschen Wert zurück, der angibt, wie Stile importiert werden, wenn sie in Quell‑ und Zieldokumenten gleiche Namen haben. Der Standardwert ist  false .

 **Remarks:** 

Wenn diese Option **aktiviert** ist, wird der Quellstil in direkte Attribute im Zieldokument expandiert, falls der Importmodus [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) verwendet wird.

Wenn diese Option **deaktiviert** ist, wird der Quellstil nur expandiert, wenn er nummeriert ist. Vorhandene Zielattribute werden nicht überschrieben, einschließlich Listen.

 **Examples:** 

Zeigt, wie doppelte Formatvorlagen beim Einfügen von Dokumenten aufgelöst werden können.

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
boolean – Ein boolescher Wert, der angibt, wie Stile importiert werden, wenn sie in Quell‑ und Zieldokumenten gleiche Namen haben.
### setAdjustSentenceAndWordSpacing(boolean value) {#setAdjustSentenceAndWordSpacing-boolean}
```
public void setAdjustSentenceAndWordSpacing(boolean value)
```


Setzt einen booleschen Wert, der angibt, ob Satz‑ und Wortabstände automatisch angepasst werden sollen. Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie Satz‑ und Wortabstände automatisch angepasst werden können.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der angibt, ob Satz‑ und Wortabstände automatisch angepasst werden sollen. |

### setAppendDocumentWithNewPage(boolean value) {#setAppendDocumentWithNewPage-boolean}
```
public void setAppendDocumentWithNewPage(boolean value)
```


Legt einen booleschen Wert fest, der angibt, ob der Typ des zuerst importierten Abschnitts zwangsweise in [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) geändert werden soll, wenn die Methode **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** aufgerufen wird.

Der Standardwert ist  true .

 **Remarks:** 

Bitte beachten Sie, dass diese Option nur für die Methode **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** relevant ist und keine Wirkung auf andere importbezogene Methoden hat.

 **Examples:** 

Zeigt, wie der ursprüngliche Abschnittstyp beibehalten wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | boolean | Ein boolescher Wert, der angibt, ob beim Aufruf von **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** der Typ des zuerst importierten Abschnitts zwangsweise in [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) geändert werden soll. |

### setForceCopyStyles(boolean value) {#setForceCopyStyles-boolean}
```
public void setForceCopyStyles(boolean value)
```


Setzt einen booleschen Wert, der angibt, ob konfliktierende Stile im Modus [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) kopiert werden sollen. Der Standardwert ist  false .

 **Remarks:** 

Standardmäßig, wenn ein passender Stil bereits in einem Zieldokument existiert, wird die Formatierung des Quellstils in direkte Knoteneigenschaften expandiert und der Stil dieses Knotens auf den Standard zurückgesetzt.

Wenn diese Option auf true gesetzt ist, wird der Quellstil zwangsweise in das Zieldokument mit einem eindeutigen Namen kopiert und auf den importierten Knoten angewendet.

Hinweis: In diesem Fall ist nicht garantiert, dass die Formatierung des importierten Knotens im Zieldokument erhalten bleibt.

 **Examples:** 

Zeigt, wie Quellstile mit eindeutigen Namen zwangsweise kopiert werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | boolean | Ein boolescher Wert, der angibt, ob konfliktierende Stile im Modus [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) kopiert werden sollen. |

### setIgnoreHeaderFooter(boolean value) {#setIgnoreHeaderFooter-boolean}
```
public void setIgnoreHeaderFooter(boolean value)
```


Setzt einen booleschen Wert, der festlegt, dass die Quellformatierung von Kopf‑/Fußzeilen‑Inhalten ignoriert wird, wenn der Modus [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) verwendet wird. Der Standardwert ist  true .

 **Examples:** 

Zeigt, wie das Ignorieren oder Nicht‑Ignorieren der Quellformatierung des Inhalts von Kopf‑ und Fußzeilen angegeben wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | boolean | Ein boolescher Wert, der festlegt, dass die Quellformatierung von Kopf‑/Fußzeilen‑Inhalten ignoriert wird, wenn der Modus [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) verwendet wird. |

### setIgnoreTextBoxes(boolean value) {#setIgnoreTextBoxes-boolean}
```
public void setIgnoreTextBoxes(boolean value)
```


Legt einen booleschen Wert fest, der angibt, dass die Quellformatierung des Inhalts von Textfeldern ignoriert wird, wenn der Modus [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) verwendet wird. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie die Formatierung von Textfeldern beim Anhängen eines Dokuments verwaltet wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | boolean | Ein boolescher Wert, der angibt, dass die Quellformatierung des Inhalts von Textfeldern ignoriert wird, wenn der Modus [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) verwendet wird. |

### setKeepSourceNumbering(boolean value) {#setKeepSourceNumbering-boolean}
```
public void setKeepSourceNumbering(boolean value)
```


Legt einen booleschen Wert fest, der angibt, wie die Nummerierung importiert wird, wenn sie in Quell- und Zieldokumenten kollidiert. Der Standardwert ist false.

 **Examples:** 

Zeigt, wie ein Dokument mit nummerierten Listen importiert wird.

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

Zeigt, wie ein Konflikt beim Importieren von Dokumenten gelöst wird, die Listen mit derselben Listendefinitions‑Kennung besitzen.

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

Zeigt, wie Listennummerierungskonflikte in Quell‑ und Zieldokumenten gelöst werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der angibt, wie die Nummerierung importiert wird, wenn sie in Quell- und Zieldokumenten kollidiert. |

### setMergePastedLists(boolean value) {#setMergePastedLists-boolean}
```
public void setMergePastedLists(boolean value)
```


Legt einen booleschen Wert fest, der angibt, ob eingefügte Listen mit umgebenden Listen zusammengeführt werden. Der Standardwert ist false.

 **Examples:** 

Zeigt, wie Listen aus einem Dokument zusammengeführt werden.

```

 Document srcDoc = new Document(getMyDir() + "List item.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setMergePastedLists(true); }

 // Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 dstDoc.save(getArtifactsDir() + "Document.MergePastedLists.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der angibt, ob eingefügte Listen mit umgebenden Listen zusammengeführt werden. |

### setResolveThemeColors(boolean value) {#setResolveThemeColors-boolean}
```
public void setResolveThemeColors(boolean value)
```


Legt einen booleschen Wert fest, der angibt, ob die Themenfarben der Formen zwangsweise aufgelöst werden sollen. Der Standardwert ist false.

 **Remarks:** 

Bitte beachten Sie, dass diese Option nur für den [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING)-Modus relevant ist.

Normalerweise löst Aspose.Words keine Quell‑Themenfarben auf, wenn beim Importieren von Stilen diese erhalten bleiben können, ohne Formatierungsattribute in direkte zu expandieren. In diesem Fall können jedoch die tatsächlichen Farben der importierten Formen von denen im Originaldokument abweichen. Der Grund dafür sind die unterschiedlichen Themenfarben in den Quell‑ und Zieldokumenten. Das Setzen dieser Option auf  true  zwingt die Auflösung der Quell‑Formen‑Themenfarben und bewahrt somit die tatsächliche Farbe der Formen, die sie im Quelldokument haben.

 **Examples:** 

Zeigt, wie ein Knoten mit Auflösung der Quell‑Themenfarben von Formen importiert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der angibt, ob die Themenfarben der Formen zwangsweise aufgelöst werden sollen. |

### setSmartStyleBehavior(boolean value) {#setSmartStyleBehavior-boolean}
```
public void setSmartStyleBehavior(boolean value)
```


Legt einen booleschen Wert fest, der angibt, wie Stile importiert werden, wenn sie in Quell- und Zieldokumenten gleiche Namen haben. Der Standardwert ist false.

 **Remarks:** 

Wenn diese Option **aktiviert** ist, wird der Quellstil in direkte Attribute im Zieldokument expandiert, falls der Importmodus [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) verwendet wird.

Wenn diese Option **deaktiviert** ist, wird der Quellstil nur expandiert, wenn er nummeriert ist. Vorhandene Zielattribute werden nicht überschrieben, einschließlich Listen.

 **Examples:** 

Zeigt, wie doppelte Formatvorlagen beim Einfügen von Dokumenten aufgelöst werden können.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der angibt, wie Stile importiert werden, wenn sie in Quell- und Zieldokumenten gleiche Namen haben. |

