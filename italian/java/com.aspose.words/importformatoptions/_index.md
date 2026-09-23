---
title: "ImportFormatOptions"
linktitle: "ImportFormatOptions"
second_title: "Aspose.Words per Java"
description: "Consente di specificare varie opzioni di importazione per formattare l'output in Java."
type: docs
weight: 401
url: /it/java/com.aspose.words/importformatoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatOptions
```

Consente di specificare varie opzioni di importazione per formattare l'output.

Per saperne di più, visita l'articolo di documentazione [ Specify Load Options ][Specify Load Options].

 **Examples:** 

Mostra come risolvere gli stili duplicati durante l'inserimento dei documenti.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getAdjustSentenceAndWordSpacing()](#getAdjustSentenceAndWordSpacing) | Restituisce un valore booleano che specifica se regolare automaticamente la spaziatura di frasi e parole. |
| [getAppendDocumentWithNewPage()](#getAppendDocumentWithNewPage) | Restituisce un valore booleano che indica se modificare forzatamente il tipo della prima sezione importata in [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) quando si chiama **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**. |
| [getForceCopyStyles()](#getForceCopyStyles) | Restituisce un valore booleano che indica se copiare gli stili in conflitto in modalità [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |
| [getIgnoreHeaderFooter()](#getIgnoreHeaderFooter) | Restituisce un valore booleano che specifica che la formattazione di origine del contenuto intestazioni/piè di pagina viene ignorata se viene utilizzata la modalità [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |
| [getIgnoreTextBoxes()](#getIgnoreTextBoxes) | Restituisce un valore booleano che specifica che la formattazione di origine del contenuto delle caselle di testo viene ignorata se viene utilizzata la modalità [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |
| [getKeepSourceNumbering()](#getKeepSourceNumbering) | Restituisce un valore booleano che specifica come la numerazione verrà importata quando entra in conflitto nei documenti di origine e destinazione. |
| [getMergePastedLists()](#getMergePastedLists) | Restituisce un valore booleano che specifica se le liste incollate verranno unite alle liste circostanti. |
| [getResolveThemeColors()](#getResolveThemeColors) | Restituisce un valore booleano che specifica se risolvere forzatamente i colori tema delle forme. |
| [getSmartStyleBehavior()](#getSmartStyleBehavior) | Restituisce un valore booleano che specifica come gli stili verranno importati quando hanno lo stesso nome nei documenti di origine e destinazione. |
| [setAdjustSentenceAndWordSpacing(boolean value)](#setAdjustSentenceAndWordSpacing-boolean) | Imposta un valore booleano che specifica se regolare automaticamente la spaziatura di frasi e parole. |
| [setAppendDocumentWithNewPage(boolean value)](#setAppendDocumentWithNewPage-boolean) | Imposta un valore booleano che indica se cambiare il tipo della prima sezione importata in [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) forzatamente quando si chiama **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**. |
| [setForceCopyStyles(boolean value)](#setForceCopyStyles-boolean) | Imposta un valore booleano che indica se copiare gli stili in conflitto in modalità [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |
| [setIgnoreHeaderFooter(boolean value)](#setIgnoreHeaderFooter-boolean) | Imposta un valore booleano che specifica che la formattazione di origine del contenuto di intestazioni/piè di pagina viene ignorata se viene utilizzata la modalità [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |
| [setIgnoreTextBoxes(boolean value)](#setIgnoreTextBoxes-boolean) | Imposta un valore booleano che specifica che la formattazione di origine del contenuto delle caselle di testo viene ignorata se viene utilizzata la modalità [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |
| [setKeepSourceNumbering(boolean value)](#setKeepSourceNumbering-boolean) | Imposta un valore booleano che specifica come la numerazione verrà importata quando entra in conflitto nei documenti di origine e destinazione. |
| [setMergePastedLists(boolean value)](#setMergePastedLists-boolean) | Imposta un valore booleano che specifica se le liste incollate verranno unite alle liste circostanti. |
| [setResolveThemeColors(boolean value)](#setResolveThemeColors-boolean) | Imposta un valore booleano che specifica se risolvere forzatamente i colori tema delle forme. |
| [setSmartStyleBehavior(boolean value)](#setSmartStyleBehavior-boolean) | Imposta un valore booleano che specifica come gli stili verranno importati quando hanno lo stesso nome nei documenti di origine e destinazione. |
### getAdjustSentenceAndWordSpacing() {#getAdjustSentenceAndWordSpacing}
```
public boolean getAdjustSentenceAndWordSpacing()
```


Restituisce un valore booleano che specifica se regolare automaticamente la spaziatura di frasi e parole. Il valore predefinito è false.

 **Examples:** 

Mostra come regolare automaticamente la spaziatura di frasi e parole.

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
boolean - Un valore booleano che specifica se regolare automaticamente la spaziatura di frasi e parole.
### getAppendDocumentWithNewPage() {#getAppendDocumentWithNewPage}
```
public boolean getAppendDocumentWithNewPage()
```


Restituisce un valore booleano che indica se modificare forzatamente il tipo della prima sezione importata in [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) quando si chiama **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**.

Il valore predefinito è  true .

 **Remarks:** 

Si prega di notare che questa opzione è rilevante solo per il metodo **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** e non ha effetto su altri metodi correlati all'importazione.

 **Examples:** 

Mostra come preservare il tipo di sezione originale.

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
boolean - Un valore booleano che indica se cambiare il tipo della prima sezione importata in [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) forzatamente quando si chiama **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**.
### getForceCopyStyles() {#getForceCopyStyles}
```
public boolean getForceCopyStyles()
```


Restituisce un valore booleano che indica se copiare gli stili in conflitto in modalità [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). Il valore predefinito è false.

 **Remarks:** 

Per impostazione predefinita, se uno stile corrispondente esiste già in un documento di destinazione, la formattazione dello stile di origine viene espansa in attributi di nodo diretti e lo stile di questo nodo viene ripristinato al valore predefinito.

Quando questa opzione è impostata su true, lo stile di origine verrà copiato forzatamente nel documento di destinazione con un nome univoco e applicato al nodo importato.

Nota, in questo caso non è garantito che la formattazione del nodo importato nel documento di destinazione venga preservata.

 **Examples:** 

Mostra come copiare forzatamente gli stili di origine con nomi univoci.

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
boolean - Un valore booleano che indica se copiare gli stili in conflitto in modalità [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).
### getIgnoreHeaderFooter() {#getIgnoreHeaderFooter}
```
public boolean getIgnoreHeaderFooter()
```


Restituisce un valore booleano che specifica che la formattazione di origine del contenuto di intestazioni/piè di pagina viene ignorata se viene utilizzata la modalità [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). Il valore predefinito è true.

 **Examples:** 

Mostra come specificare l'ignorare o meno la formattazione di origine del contenuto di intestazioni/piè di pagina.

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
boolean - Un valore booleano che specifica che la formattazione di origine del contenuto di intestazioni/piè di pagina è ignorata se viene utilizzata la modalità [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).
### getIgnoreTextBoxes() {#getIgnoreTextBoxes}
```
public boolean getIgnoreTextBoxes()
```


Restituisce un valore booleano che specifica che la formattazione di origine del contenuto delle caselle di testo è ignorata se [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) è usata. Il valore predefinito è  true .

 **Examples:** 

Mostra come gestire la formattazione delle caselle di testo durante l'aggiunta di un documento.

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
boolean - Un valore booleano che specifica che la formattazione di origine del contenuto delle caselle di testo è ignorata se [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) è usata.
### getKeepSourceNumbering() {#getKeepSourceNumbering}
```
public boolean getKeepSourceNumbering()
```


Restituisce un valore booleano che specifica come la numerazione sarà importata quando entra in conflitto nei documenti di origine e destinazione. Il valore predefinito è  false .

 **Examples:** 

Mostra come importare un documento con elenchi numerati.

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

Mostra come risolvere un conflitto durante l'importazione di documenti che contengono elenchi con lo stesso identificatore di definizione dell'elenco.

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

Mostra come risolvere i conflitti di numerazione degli elenchi nei documenti di origine e destinazione.

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
boolean - Un valore booleano che specifica come la numerazione sarà importata quando entra in conflitto nei documenti di origine e destinazione.
### getMergePastedLists() {#getMergePastedLists}
```
public boolean getMergePastedLists()
```


Restituisce un valore booleano che specifica se gli elenchi incollati saranno uniti agli elenchi circostanti. Il valore predefinito è  false .

 **Examples:** 

Mostra come unire gli elenchi da un documento.

```

 Document srcDoc = new Document(getMyDir() + "List item.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setMergePastedLists(true); }

 // Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 dstDoc.save(getArtifactsDir() + "Document.MergePastedLists.docx");
 
```

**Returns:**
boolean - Un valore booleano che specifica se gli elenchi incollati saranno uniti agli elenchi circostanti.
### getResolveThemeColors() {#getResolveThemeColors}
```
public boolean getResolveThemeColors()
```


Restituisce un valore booleano che specifica se risolvere forzatamente i colori tematici delle forme. Il valore predefinito è  false .

 **Remarks:** 

Si prega di notare che questa opzione è rilevante solo per la modalità [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).

Normalmente, Aspose.Words non risolve i colori tematici di origine quando le impostazioni di stile importate possono essere preservate senza espandere gli attributi di formattazione in quelli diretti. Tuttavia, in questo caso i colori effettivi delle forme importate possono differire da quelli presenti nel documento originale. Il motivo è la differenza dei colori tematici nei documenti di origine e destinazione. Impostare questa opzione su  true  forza la risoluzione dei colori tematici delle forme di origine e quindi preserva il colore reale delle forme presenti nel documento di origine.

 **Examples:** 

Mostra come importare un nodo risolvendo i colori tematici di origine delle forme.

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
boolean - Un valore booleano che specifica se risolvere forzatamente i colori tematici delle forme.
### getSmartStyleBehavior() {#getSmartStyleBehavior}
```
public boolean getSmartStyleBehavior()
```


Restituisce un valore booleano che specifica come gli stili saranno importati quando hanno lo stesso nome nei documenti di origine e destinazione. Il valore predefinito è  false .

 **Remarks:** 

Quando questa opzione è **enabled**, lo stile di origine verrà espanso in attributi diretti all'interno di un documento di destinazione, se viene utilizzata la modalità di importazione [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).

Quando questa opzione è **disabled**, lo stile di origine verrà espanso solo se è numerato. Gli attributi di destinazione esistenti non saranno sovrascritti, inclusi gli elenchi.

 **Examples:** 

Mostra come risolvere gli stili duplicati durante l'inserimento dei documenti.

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
boolean - Un valore booleano che specifica come gli stili saranno importati quando hanno lo stesso nome nei documenti di origine e destinazione.
### setAdjustSentenceAndWordSpacing(boolean value) {#setAdjustSentenceAndWordSpacing-boolean}
```
public void setAdjustSentenceAndWordSpacing(boolean value)
```


Imposta un valore booleano che specifica se regolare automaticamente la spaziatura di frasi e parole. Il valore predefinito è  false .

 **Examples:** 

Mostra come regolare automaticamente la spaziatura di frasi e parole.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore booleano che specifica se regolare automaticamente la spaziatura di frasi e parole. |

### setAppendDocumentWithNewPage(boolean value) {#setAppendDocumentWithNewPage-boolean}
```
public void setAppendDocumentWithNewPage(boolean value)
```


Imposta un valore booleano che indica se cambiare il tipo della prima sezione importata in [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) forzatamente quando si chiama **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**.

Il valore predefinito è  true .

 **Remarks:** 

Si prega di notare che questa opzione è rilevante solo per il metodo **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** e non ha effetto su altri metodi correlati all'importazione.

 **Examples:** 

Mostra come preservare il tipo di sezione originale.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | boolean | Un valore booleano che indica se modificare il tipo della prima sezione importata in [SectionStart.NEW_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) forzatamente quando si chiama **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**. |

### setForceCopyStyles(boolean value) {#setForceCopyStyles-boolean}
```
public void setForceCopyStyles(boolean value)
```


Imposta un valore booleano che indica se copiare gli stili in conflitto in modalità [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) . Il valore predefinito è false .

 **Remarks:** 

Per impostazione predefinita, se uno stile corrispondente esiste già in un documento di destinazione, la formattazione dello stile di origine viene espansa in attributi di nodo diretti e lo stile di questo nodo viene ripristinato al valore predefinito.

Quando questa opzione è impostata su true, lo stile di origine verrà copiato forzatamente nel documento di destinazione con un nome univoco e applicato al nodo importato.

Nota, in questo caso non è garantito che la formattazione del nodo importato nel documento di destinazione venga preservata.

 **Examples:** 

Mostra come copiare forzatamente gli stili di origine con nomi univoci.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | boolean | Un valore booleano che indica se copiare gli stili in conflitto in modalità [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) . |

### setIgnoreHeaderFooter(boolean value) {#setIgnoreHeaderFooter-boolean}
```
public void setIgnoreHeaderFooter(boolean value)
```


Imposta un valore booleano che specifica che la formattazione di origine del contenuto di intestazioni/piè di pagina viene ignorata se la modalità [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) è usata. Il valore predefinito è true .

 **Examples:** 

Mostra come specificare l'ignorare o meno la formattazione di origine del contenuto di intestazioni/piè di pagina.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | boolean | Un valore booleano che specifica che la formattazione di origine del contenuto di intestazioni/piè di pagina viene ignorata se la modalità [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) è usata. |

### setIgnoreTextBoxes(boolean value) {#setIgnoreTextBoxes-boolean}
```
public void setIgnoreTextBoxes(boolean value)
```


Imposta un valore booleano che specifica che la formattazione di origine del contenuto di caselle di testo viene ignorata se la modalità [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) è usata. Il valore predefinito è true .

 **Examples:** 

Mostra come gestire la formattazione delle caselle di testo durante l'aggiunta di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | boolean | Un valore booleano che specifica che la formattazione di origine del contenuto di caselle di testo viene ignorata se la modalità [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) è usata. |

### setKeepSourceNumbering(boolean value) {#setKeepSourceNumbering-boolean}
```
public void setKeepSourceNumbering(boolean value)
```


Imposta un valore booleano che specifica come la numerazione verrà importata quando entra in conflitto nei documenti di origine e destinazione. Il valore predefinito è false .

 **Examples:** 

Mostra come importare un documento con elenchi numerati.

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

Mostra come risolvere un conflitto durante l'importazione di documenti che contengono elenchi con lo stesso identificatore di definizione dell'elenco.

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

Mostra come risolvere i conflitti di numerazione degli elenchi nei documenti di origine e destinazione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore booleano che specifica come la numerazione verrà importata quando entra in conflitto nei documenti di origine e destinazione. |

### setMergePastedLists(boolean value) {#setMergePastedLists-boolean}
```
public void setMergePastedLists(boolean value)
```


Imposta un valore booleano che specifica se gli elenchi incollati saranno uniti agli elenchi circostanti. Il valore predefinito è false .

 **Examples:** 

Mostra come unire gli elenchi da un documento.

```

 Document srcDoc = new Document(getMyDir() + "List item.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setMergePastedLists(true); }

 // Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 dstDoc.save(getArtifactsDir() + "Document.MergePastedLists.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore booleano che specifica se gli elenchi incollati saranno uniti agli elenchi circostanti. |

### setResolveThemeColors(boolean value) {#setResolveThemeColors-boolean}
```
public void setResolveThemeColors(boolean value)
```


Imposta un valore booleano che specifica se risolvere forzatamente i colori tema delle forme. Il valore predefinito è false .

 **Remarks:** 

Si prega di notare che questa opzione è rilevante solo per la modalità [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).

Normalmente, Aspose.Words non risolve i colori tematici di origine quando le impostazioni di stile importate possono essere preservate senza espandere gli attributi di formattazione in quelli diretti. Tuttavia, in questo caso i colori effettivi delle forme importate possono differire da quelli presenti nel documento originale. Il motivo è la differenza dei colori tematici nei documenti di origine e destinazione. Impostare questa opzione su  true  forza la risoluzione dei colori tematici delle forme di origine e quindi preserva il colore reale delle forme presenti nel documento di origine.

 **Examples:** 

Mostra come importare un nodo risolvendo i colori tematici di origine delle forme.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore booleano che specifica se risolvere forzatamente i colori tema delle forme. |

### setSmartStyleBehavior(boolean value) {#setSmartStyleBehavior-boolean}
```
public void setSmartStyleBehavior(boolean value)
```


Imposta un valore booleano che specifica come gli stili saranno importati quando hanno lo stesso nome nei documenti di origine e destinazione. Il valore predefinito è false .

 **Remarks:** 

Quando questa opzione è **enabled**, lo stile di origine verrà espanso in attributi diretti all'interno di un documento di destinazione, se viene utilizzata la modalità di importazione [ImportFormatMode.KEEP_SOURCE_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).

Quando questa opzione è **disabled**, lo stile di origine verrà espanso solo se è numerato. Gli attributi di destinazione esistenti non saranno sovrascritti, inclusi gli elenchi.

 **Examples:** 

Mostra come risolvere gli stili duplicati durante l'inserimento dei documenti.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore booleano che specifica come gli stili saranno importati quando hanno lo stesso nome nei documenti di origine e destinazione. |

