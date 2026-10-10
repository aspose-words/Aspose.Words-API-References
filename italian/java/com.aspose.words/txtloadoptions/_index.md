---
title: "TxtLoadOptions"
linktitle: "TxtLoadOptions"
second_title: "Aspose.Words per Java"
description: "Consente di specificare opzioni aggiuntive durante il caricamento del documento LoadFormat.TEXT in un oggetto Document in Java."
type: docs
weight: 693
url: /it/java/com.aspose.words/txtloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions/)
```
public class TxtLoadOptions extends LoadOptions
```

Consente di specificare opzioni aggiuntive durante il caricamento del documento [LoadFormat.TEXT](../../com.aspose.words/loadformat/\#TEXT) in un oggetto [Document](../../com.aspose.words/document/).

Per saperne di più, visita l'articolo di documentazione [ Specify Load Options ][Specify Load Options].

 **Examples:** 

Mostra come leggere e visualizzare i collegamenti ipertestuali.

```

 final String INPUT_TEXT = "Some links in TXT:\n" +
         "https://www.aspose.com/\n" +
         "https://docs.aspose.com/words/net/\n";

 try (ByteArrayInputStream stream = new ByteArrayInputStream(INPUT_TEXT.getBytes(StandardCharsets.US_ASCII)))
 {
     // Load document with hyperlinks.
     TxtLoadOptions loadOptions = new TxtLoadOptions();
     loadOptions.setDetectHyperlinks(true);
     Document doc = new Document(stream, loadOptions);

     // Print hyperlinks text.
     for (Field field : doc.getRange().getFields())
         System.out.println(field.getResult());

     Assert.assertEquals(doc.getRange().getFields().get(0).getResult().trim(), "https://www.aspose.com/");
     Assert.assertEquals(doc.getRange().getFields().get(1).getResult().trim(), "https://docs.aspose.com/words/net/");
 }
 
```


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## Costruttori

| Costruttore | Descrizione |
| --- | --- |
| [TxtLoadOptions()](#TxtLoadOptions) | Inizializza una nuova istanza di questa classe con i valori predefiniti. |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| [getAutoNumberingDetection()](#getAutoNumberingDetection) | Restituisce un valore booleano che indica se la rilevazione automatica della numerazione verrà eseguita durante il caricamento di un documento. |
| [getBaseUri()](#getBaseUri) | Ottiene la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando necessario. |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng) | Ottiene se convertire le immagini metafile ( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) nel formato immagine **F:Aspose.FileFormat.Png**. |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath) | Ottiene se convertire le forme con EquationXML in oggetti Office Math. |
| [getDetectHyperlinks()](#getDetectHyperlinks) | Specifica se rilevare i collegamenti ipertestuali nel testo. |
| [getDetectNumberingWithWhitespaces()](#getDetectNumberingWithWhitespaces) | Consente di specificare come gli elementi di elenco numerato vengono riconosciuti quando il documento è importato da un formato di testo semplice. |
| [getDocumentDirection()](#getDocumentDirection) | Restituisce la direzione del documento. |
| [getEncoding()](#getEncoding) | Ottiene la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. |
| [getFontSettings()](#getFontSettings) | Consente di specificare le impostazioni dei caratteri del documento. |
| [getIgnoreOleData()](#getIgnoreOleData) | Specifica se ignorare i dati OLE. |
| [getLanguagePreferences()](#getLanguagePreferences) | Ottiene le preferenze linguistiche che verranno utilizzate durante il caricamento del documento. |
| [getLeadingSpacesOptions()](#getLeadingSpacesOptions) | Restituisce l'opzione preferita per la gestione degli spazi iniziali. |
| [getLoadFormat()](#getLoadFormat) | Specifica il formato del documento da caricare. |
| [getMswVersion()](#getMswVersion) | Consente di specificare che il processo di caricamento del documento deve corrispondere a una versione specifica di MS Word. |
| [getPassword()](#getPassword) | Ottiene la password per aprire un documento crittografato. |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField) | Ottiene se preservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. |
| [getProgressCallback()](#getProgressCallback) | Chiamato durante il caricamento di un documento e accetta dati sul progresso del caricamento. |
| [getRecoveryMode()](#getRecoveryMode) | Definisce come il documento deve essere gestito se si verificano errori durante il caricamento. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback) | Consente di controllare come le risorse esterne (immagini, fogli di stile) vengono caricate quando un documento è importato da HTML, MHTML. |
| [getTempFolder()](#getTempFolder) | Consente di utilizzare file temporanei durante la lettura del documento. |
| [getTrailingSpacesOptions()](#getTrailingSpacesOptions) | Restituisce l'opzione preferita per la gestione degli spazi finali. |
| [getUpdateDirtyFields()](#getUpdateDirtyFields) | Specifica se aggiornare i campi con l'attributo  dirty  . |
| [getUseSystemLcid()](#getUseSystemLcid) | Restituisce se utilizzare il valore LCID ottenuto dal registro di Windows per determinare i margini predefiniti dell'impostazione pagina. |
| [getWarningCallback()](#getWarningCallback) | Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe comportare una perdita di fedeltà dei dati o della formattazione. |
| [setAutoNumberingDetection(boolean value)](#setAutoNumberingDetection-boolean) | Imposta un valore booleano che indica se la rilevazione automatica della numerazione verrà eseguita durante il caricamento di un documento. |
| [setBaseUri(String value)](#setBaseUri-java.lang.String) | Imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando necessario. |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean) | Imposta se convertire le immagini metafile( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) nel formato immagine **F:Aspose.FileFormat.Png**. |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean) | Imposta se convertire le forme con EquationXML in oggetti Office Math. |
| [setDetectHyperlinks(boolean value)](#setDetectHyperlinks-boolean) | Specifica se rilevare i collegamenti ipertestuali nel testo. |
| [setDetectNumberingWithWhitespaces(boolean value)](#setDetectNumberingWithWhitespaces-boolean) | Consente di specificare come gli elementi di elenco numerato vengono riconosciuti quando il documento è importato da un formato di testo semplice. |
| [setDocumentDirection(int value)](#setDocumentDirection-int) | Imposta la direzione del documento. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) | Imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Consente di specificare le impostazioni dei caratteri del documento. |
| [setIgnoreOleData(boolean value)](#setIgnoreOleData-boolean) | Specifica se ignorare i dati OLE. |
| [setLeadingSpacesOptions(int value)](#setLeadingSpacesOptions-int) | Imposta l'opzione preferita per la gestione degli spazi iniziali. |
| [setLoadFormat(int value)](#setLoadFormat-int) | Specifica il formato del documento da caricare. |
| [setMswVersion(int value)](#setMswVersion-int) | Consente di specificare che il processo di caricamento del documento deve corrispondere a una versione specifica di MS Word. |
| [setPassword(String value)](#setPassword-java.lang.String) | Imposta la password per aprire un documento crittografato. |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean) | Imposta se preservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback) | Chiamato durante il caricamento di un documento e accetta dati sul progresso del caricamento. |
| [setRecoveryMode(int value)](#setRecoveryMode-int) | Definisce come il documento deve essere gestito se si verificano errori durante il caricamento. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback) | Consente di controllare come le risorse esterne (immagini, fogli di stile) vengono caricate quando un documento è importato da HTML, MHTML. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Consente di utilizzare file temporanei durante la lettura del documento. |
| [setTrailingSpacesOptions(int value)](#setTrailingSpacesOptions-int) | Imposta l'opzione preferita per la gestione degli spazi finali. |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean) | Specifica se aggiornare i campi con l'attributo  dirty  . |
| [setUseSystemLcid(boolean value)](#setUseSystemLcid-boolean) | Imposta se utilizzare il valore LCID ottenuto dal registro di Windows per determinare i margini predefiniti dell'impostazione pagina. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe comportare una perdita di fedeltà dei dati o della formattazione. |
### TxtLoadOptions() {#TxtLoadOptions}
```
public TxtLoadOptions()
```


Inizializza una nuova istanza di questa classe con i valori predefiniti.

 **Examples:** 

Mostra come leggere e visualizzare i collegamenti ipertestuali.

```

 final String INPUT_TEXT = "Some links in TXT:\n" +
         "https://www.aspose.com/\n" +
         "https://docs.aspose.com/words/net/\n";

 try (ByteArrayInputStream stream = new ByteArrayInputStream(INPUT_TEXT.getBytes(StandardCharsets.US_ASCII)))
 {
     // Load document with hyperlinks.
     TxtLoadOptions loadOptions = new TxtLoadOptions();
     loadOptions.setDetectHyperlinks(true);
     Document doc = new Document(stream, loadOptions);

     // Print hyperlinks text.
     for (Field field : doc.getRange().getFields())
         System.out.println(field.getResult());

     Assert.assertEquals(doc.getRange().getFields().get(0).getResult().trim(), "https://www.aspose.com/");
     Assert.assertEquals(doc.getRange().getFields().get(1).getResult().trim(), "https://docs.aspose.com/words/net/");
 }
 
```

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determina se l'oggetto specificato è uguale in valore all'oggetto corrente.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getAutoNumberingDetection() {#getAutoNumberingDetection}
```
public boolean getAutoNumberingDetection()
```


Restituisce un valore booleano che indica se la rilevazione automatica della numerazione verrà eseguita durante il caricamento di un documento. Il valore predefinito è  true .

 **Examples:** 

Mostra come disabilitare il rilevamento automatico della numerazione.

```

 TxtLoadOptions options = new TxtLoadOptions(); { options.setAutoNumberingDetection(false); }
 Document doc = new Document(getMyDir() + "Number detection.txt", options);
 
```

**Returns:**
boolean - Un valore booleano che indica se il rilevamento automatico della numerazione verrà eseguito durante il caricamento di un documento.
### getBaseUri() {#getBaseUri}
```
public String getBaseUri()
```


Restituisce la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando necessario. Può essere  null  o una stringa vuota. Il valore predefinito è  null .

 **Remarks:** 

Questa proprietà viene utilizzata per risolvere gli URI relativi in assoluti nei seguenti casi:

1.  Quando si carica un documento HTML da uno stream e il documento contiene immagini con URI relativi e non ha un URI di base specificato nell'elemento BASE HTML.
2.  Quando si salva un documento in PDF e altri formati, per recuperare le immagini collegate tramite URI relativi in modo che le immagini possano essere salvate nel documento di output.

 **Examples:** 

Mostra come aprire un documento HTML con immagini da uno stream utilizzando un URI di base.

```

 InputStream stream = new FileInputStream(getMyDir() + "Document.html");
 try  {
     // Pass the URI of the base folder while loading it
     // so that any images with relative URIs in the HTML document can be found.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setBaseUri(getImageDir());

     Document doc = new Document(stream, loadOptions);

     // Verify that the first shape of the document contains a valid image.
     Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

     Assert.assertTrue(shape.isImage());
     Assert.assertNotNull(shape.getImageData().getImageBytes());
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getWidth()), 0.01);
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getHeight()), 0.01);
 } finally {
     if (stream != null) stream.close();
 }
 
```

**Returns:**
java.lang.String - La stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando necessario.
### getConvertMetafilesToPng() {#getConvertMetafilesToPng}
```
public boolean getConvertMetafilesToPng()
```


Ottiene se convertire le immagini metafile ( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) nel formato immagine **F:Aspose.FileFormat.Png**.

 **Remarks:** 

I metafili ( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) sono un formato immagine non compresso e a volte richiedono troppa RAM per contenere e elaborare il documento. Questa opzione consente di convertire tutte le immagini metafile in **F:Aspose.FileFormat.Png** durante il caricamento del documento. Nota: la conversione di grafica vettoriale in raster diminuisce la qualità delle immagini.

 **Examples:** 

Mostra come convertire WMF/EMF in PNG durante il caricamento del documento.

```

 Document doc = new Document();

 Shape shape = new Shape(doc, ShapeType.IMAGE);
 shape.getImageData().setImage(getImageDir() + "Windows MetaFile.wmf");
 shape.setWidth(100.0);
 shape.setHeight(100.0);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(shape);

 doc.save(getArtifactsDir() + "Image.CreateImageDirectly.docx");

 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.WMF, shape);

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setConvertMetafilesToPng(true);

 doc = new Document(getArtifactsDir() + "Image.CreateImageDirectly.docx", loadOptions);
 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.PNG, shape);
 
```

**Returns:**
boolean - Indica se convertire le immagini metafile ( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) nel formato immagine **F:Aspose.FileFormat.Png**.
### getConvertShapeToOfficeMath() {#getConvertShapeToOfficeMath}
```
public boolean getConvertShapeToOfficeMath()
```


Ottiene se convertire le forme con EquationXML in oggetti Office Math.

 **Examples:** 

Mostra come convertire le forme EquationXML in oggetti Office Math.

```

 LoadOptions loadOptions = new LoadOptions();

 // Use this flag to specify whether to convert the shapes with EquationXML attributes
 // to Office Math objects and then load the document.
 loadOptions.setConvertShapeToOfficeMath(isConvertShapeToOfficeMath);

 Document doc = new Document(getMyDir() + "Math shapes.docx", loadOptions);

 if (isConvertShapeToOfficeMath) {
     Assert.assertEquals(16, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(34, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 } else {
     Assert.assertEquals(24, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(0, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 }
 
```

**Returns:**
boolean - Indica se convertire le forme con EquationXML in oggetti Office Math.
### getDetectHyperlinks() {#getDetectHyperlinks}
```
public boolean getDetectHyperlinks()
```


Specifica se rilevare i collegamenti ipertestuali nel testo. Il valore predefinito è false.

 **Examples:** 

Mostra come leggere e visualizzare i collegamenti ipertestuali.

```

 final String INPUT_TEXT = "Some links in TXT:\n" +
         "https://www.aspose.com/\n" +
         "https://docs.aspose.com/words/net/\n";

 try (ByteArrayInputStream stream = new ByteArrayInputStream(INPUT_TEXT.getBytes(StandardCharsets.US_ASCII)))
 {
     // Load document with hyperlinks.
     TxtLoadOptions loadOptions = new TxtLoadOptions();
     loadOptions.setDetectHyperlinks(true);
     Document doc = new Document(stream, loadOptions);

     // Print hyperlinks text.
     for (Field field : doc.getRange().getFields())
         System.out.println(field.getResult());

     Assert.assertEquals(doc.getRange().getFields().get(0).getResult().trim(), "https://www.aspose.com/");
     Assert.assertEquals(doc.getRange().getFields().get(1).getResult().trim(), "https://docs.aspose.com/words/net/");
 }
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getDetectNumberingWithWhitespaces() {#getDetectNumberingWithWhitespaces}
```
public boolean getDetectNumberingWithWhitespaces()
```


Consente di specificare come vengono riconosciuti gli elementi di elenchi numerati quando il documento è importato da formato di testo semplice. Il valore predefinito è true.

 **Remarks:** 

Se questa opzione è impostata su false, l'algoritmo di riconoscimento degli elenchi rileva i paragrafi di elenco quando i numeri degli elenchi terminano con un punto, una parentesi chiusa o simboli di elenco puntato (come \"\\\\u2022\", \"\\*\", \"-\" o \"o\").

Se questa opzione è impostata su true, gli spazi bianchi sono anche usati come delimitatori dei numeri di elenco: l'algoritmo di riconoscimento degli elenchi per la numerazione in stile arabo (1., 1.1.2.) utilizza sia gli spazi bianchi sia il punto (\".\") come simboli.

 **Examples:** 

Mostra come rilevare gli elenchi durante il caricamento di documenti di testo semplice.

```

 // Create a plaintext document in a string with four separate parts that we may interpret as lists,
 // with different delimiters. Upon loading the plaintext document into a "Document" object,
 // Aspose.Words will always detect the first three lists and will add a "List" object
 // for each to the document's "Lists" property.
 final String TEXT_DOC = "Full stop delimiters:\n" +
         "1. First list item 1\n" +
         "2. First list item 2\n" +
         "3. First list item 3\n\n" +
         "Right bracket delimiters:\n" +
         "1) Second list item 1\n" +
         "2) Second list item 2\n" +
         "3) Second list item 3\n\n" +
         "Bullet delimiters:\n" +
         "\u2022 Third list item 1\n" +
         "\u2022 Third list item 2\n" +
         "\u2022 Third list item 3\n\n" +
         "Whitespace delimiters:\n" +
         "1 Fourth list item 1\n" +
         "2 Fourth list item 2\n" +
         "3 Fourth list item 3";

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DetectNumberingWithWhitespaces" property to "true" to detect numbered items
 // with whitespace delimiters, such as the fourth list in our document, as lists.
 // This may also falsely detect paragraphs that begin with numbers as lists.
 // Set the "DetectNumberingWithWhitespaces" property to "false"
 // to not create lists from numbered items with whitespace delimiters.
 loadOptions.setDetectNumberingWithWhitespaces(detectNumberingWithWhitespaces);

 Document doc = new Document(new ByteArrayInputStream(TEXT_DOC.getBytes()), loadOptions);

 List paragraphList = Arrays.stream(doc.getFirstSection().getBody().getParagraphs().toArray())
         .filter(Paragraph.class::isInstance)
         .map(Paragraph.class::cast)
         .collect(Collectors.toList());

 if (detectNumberingWithWhitespaces) {
     Assert.assertEquals(4, doc.getLists().getCount());
     Assert.assertTrue(IterableUtils.matchesAny(paragraphList, s -> s.getText().contains("Fourth list") && s.isListItem()));
 } else {
     Assert.assertEquals(3, doc.getLists().getCount());
     Assert.assertFalse(IterableUtils.matchesAny(paragraphList, s -> s.getText().contains("Fourth list") && s.isListItem()));
 }
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getDocumentDirection() {#getDocumentDirection}
```
public int getDocumentDirection()
```


Ottiene la direzione del documento. Il valore predefinito è [DocumentDirection.LEFT\_TO\_RIGHT](../../com.aspose.words/documentdirection/\#LEFT-TO-RIGHT).

 **Examples:** 

Mostra come rilevare la direzione del testo di un documento di testo semplice.

```

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
 // the direction of every paragraph of text that Aspose.Words loads from plaintext.
 // Each paragraph's "Bidi" property will store its direction.
 loadOptions.setDocumentDirection(DocumentDirection.AUTO);

 // Detect Hebrew text as right-to-left.
 Document doc = new Document(getMyDir() + "Hebrew text.txt", loadOptions);

 Assert.assertTrue(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());

 // Detect English text as right-to-left.
 doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertFalse(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());
 
```

**Returns:**
int - Una direzione del documento. Il valore restituito è una delle costanti di [DocumentDirection](../../com.aspose.words/documentdirection/).
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


Restituisce la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere  null . Il valore predefinito è  null .

 **Remarks:** 

Questa proprietà viene utilizzata solo durante il caricamento di documenti HTML, TXT o CHM.

Se la codifica non è specificata all'interno del documento e questa proprietà è  null , il sistema proverà a rilevare automaticamente la codifica.

 **Examples:** 

Mostra come impostare la codifica con cui aprire un documento.

```

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setEncoding(StandardCharsets.US_ASCII);
 }

 // Load the document while passing the LoadOptions object, then verify the document's contents.
 Document doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertTrue(doc.toString(SaveFormat.TEXT).contains("This is a sample text in English."));
 
```

**Returns:**
java.nio.charset.Charset - La codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Consente di specificare le impostazioni dei caratteri del documento.

 **Remarks:** 

Durante il caricamento di alcuni formati, Aspose.Words potrebbe dover risolvere i font. Ad esempio, durante il caricamento di documenti HTML Aspose.Words può risolvere i font per eseguire il fallback dei font.

Se impostato su  null , verranno utilizzate le impostazioni predefinite dei font statici [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance).

Il valore predefinito è  null .

 **Examples:** 

Mostra come designare i sostituti dei caratteri durante il caricamento.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(new FontSettings());

 // Set a font substitution rule for a LoadOptions object.
 // If the document we are loading uses a font which we do not have,
 // this rule will substitute the unavailable font with one that does exist.
 // In this case, all uses of the "MissingFont" will convert to "Comic Sans MS".
 TableSubstitutionRule substitutionRule = loadOptions.getFontSettings().getSubstitutionSettings().getTableSubstitution();
 substitutionRule.addSubstitutes("MissingFont", "Comic Sans MS");

 Document doc = new Document(getMyDir() + "Missing font.html", loadOptions);

 // At this point such text will still be in "MissingFont".
 // Font substitution will take place when we render the document.
 Assert.assertEquals("MissingFont", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getFont().getName());

 doc.save(getArtifactsDir() + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
 
```

Mostra come applicare le impostazioni di sostituzione dei caratteri durante il caricamento di un documento.

```

 // Create a FontSettings object that will substitute the "Times New Roman" font
 // with the font "Arvo" from our "MyFonts" folder.
 FontSettings fontSettings = new FontSettings();
 fontSettings.setFontsFolder(getFontsDir(), false);
 fontSettings.getSubstitutionSettings().getTableSubstitution().addSubstitutes("Times New Roman", "Arvo");

 // Set that FontSettings object as a property of a newly created LoadOptions object.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(fontSettings);

 // Load the document, then render it as a PDF with the font substitution.
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.FontSettings.pdf");
 
```

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getIgnoreOleData() {#getIgnoreOleData}
```
public boolean getIgnoreOleData()
```


Specifica se ignorare i dati OLE.

 **Remarks:** 

Ignorare i dati OLE può ridurre il consumo di memoria e aumentare le prestazioni senza perdita di dati nel caso in cui il formato di destinazione non supporti oggetti OLE.

Il valore predefinito è  false .

 **Examples:** 

Mostra come ignorare i dati OLE durante il caricamento.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getLanguagePreferences() {#getLanguagePreferences}
```
public LanguagePreferences getLanguagePreferences()
```


Ottiene le preferenze linguistiche che verranno utilizzate durante il caricamento del documento.

 **Examples:** 

Mostra come applicare le preferenze di lingua durante il caricamento di un documento.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.getLanguagePreferences().addEditingLanguage(EditingLanguage.JAPANESE);

 Document doc = new Document(getMyDir() + "No default editing language.docx", loadOptions);

 int localeIdFarEast = doc.getStyles().getDefaultFont().getLocaleIdFarEast();
 System.out.println(localeIdFarEast == EditingLanguage.JAPANESE
         ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
         : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
 
```

**Returns:**
[LanguagePreferences](../../com.aspose.words/languagepreferences/) - Language preferences that will be used when document is loading.
### getLeadingSpacesOptions() {#getLeadingSpacesOptions}
```
public int getLeadingSpacesOptions()
```


Ottiene l'opzione preferita per la gestione degli spazi iniziali. Il valore predefinito è [TxtLeadingSpacesOptions.CONVERT\_TO\_INDENT](../../com.aspose.words/txtleadingspacesoptions/\#CONVERT-TO-INDENT).

 **Examples:** 

Mostra come eliminare gli spazi bianchi durante il caricamento di documenti di testo semplice.

```

 String textDoc = "      Line 1 \n" +
         "    Line 2   \n" +
         " Line 3       ";

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the start of every line.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.ConvertToIndent"
 // to remove all whitespace characters from the start of every line,
 // and then apply a left first line indent to the paragraph to simulate the effect of the whitespaces.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Trim"
 // to remove all whitespace characters from every line's start.
 loadOptions.setLeadingSpacesOptions(txtLeadingSpacesOptions);

 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the end of every line.
 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Trim" to
 // remove all whitespace characters from the end of every line.
 loadOptions.setTrailingSpacesOptions(txtTrailingSpacesOptions);

 Document doc = new Document(new ByteArrayInputStream(textDoc.getBytes()), loadOptions);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 switch (txtLeadingSpacesOptions) {
     case TxtLeadingSpacesOptions.CONVERT_TO_INDENT:
         Assert.assertEquals(37.8d, paragraphs.get(0).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(25.2d, paragraphs.get(1).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(6.3d, paragraphs.get(2).getParagraphFormat().getFirstLineIndent());

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
     case TxtLeadingSpacesOptions.PRESERVE:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("      Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("    Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith(" Line 3"));
         break;
     case TxtLeadingSpacesOptions.TRIM:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
 }

 switch (txtTrailingSpacesOptions) {
     case TxtTrailingSpacesOptions.PRESERVE:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1 \r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2   \r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3       \f"));
         break;
     case TxtTrailingSpacesOptions.TRIM:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1\r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2\r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3\f"));
         break;
 }
 
```

**Returns:**
int - Opzione preferita per la gestione degli spazi iniziali. Il valore restituito è una delle costanti di [TxtLeadingSpacesOptions](../../com.aspose.words/txtleadingspacesoptions/).
### getLoadFormat() {#getLoadFormat}
```
public int getLoadFormat()
```


Specifica il formato del documento da caricare. Il valore predefinito è [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO).

 **Remarks:** 

Si consiglia di specificare il valore [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) e lasciare che Aspose.Words rilevi automaticamente il formato del file. Se conosci il formato del documento che stai per caricare, puoi specificarlo esplicitamente e questo ridurrà leggermente il tempo di caricamento eliminando l'overhead associato al rilevamento automatico del formato. Se specifichi un formato di caricamento esplicito e risulta errato, verrà invocata la rilevazione automatica e verrà effettuato un secondo tentativo di caricamento del file.

 **Examples:** 

Mostra come specificare un URI di base quando si apre un documento html.

```

 // Suppose we want to load an .html document that contains an image linked by a relative URI
 // while the image is in a different location. In that case, we will need to resolve the relative URI into an absolute one.
 // We can provide a base URI using an HtmlLoadOptions object.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.HTML, "", getImageDir());

 Assert.assertEquals(LoadFormat.HTML, loadOptions.getLoadFormat());

 Document doc = new Document(getMyDir() + "Missing image.html", loadOptions);

 // While the image was broken in the input .html, our custom base URI helped us repair the link.
 Shape imageShape = (Shape) doc.getChildNodes(NodeType.SHAPE, true).get(0);
 Assert.assertTrue(imageShape.isImage());

 // This output document will display the image that was missing.
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BaseUri.docx");
 
```

**Returns:**
int - Il valore  int  corrispondente. Il valore restituito è una delle costanti [LoadFormat](../../com.aspose.words/loadformat/).
### getMswVersion() {#getMswVersion}
```
public int getMswVersion()
```


Consente di specificare che il processo di caricamento del documento debba corrispondere a una versione specifica di MS Word. Il valore predefinito è [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019).

 **Remarks:** 

Versioni diverse di Word possono gestire alcuni aspetti del contenuto e della formattazione del documento in modo leggermente diverso durante il processo di caricamento, il che può comportare piccole differenze nel Document Object Model.

 **Examples:** 

Mostra come emulare la procedura di caricamento di una specifica versione di Microsoft Word durante il caricamento del documento.

```

 // By default, Aspose.Words load documents according to Microsoft Word 2019 specification.
 LoadOptions loadOptions = new LoadOptions();

 Assert.assertEquals(MsWordVersion.WORD_2019, loadOptions.getMswVersion());

 // This document is missing the default paragraph formatting style.
 // This default style will be regenerated when we load the document either with Microsoft Word or Aspose.Words.
 loadOptions.setMswVersion(MsWordVersion.WORD_2007);
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 // The style's line spacing will have this value when loaded by Microsoft Word 2007 specification.
 Assert.assertEquals(12.95d, doc.getStyles().getDefaultParagraphFormat().getLineSpacing(), 0.01d);
 
```

**Returns:**
int - Il valore  int  corrispondente. Il valore restituito è una delle costanti [MsWordVersion](../../com.aspose.words/mswordversion/).
### getPassword() {#getPassword}
```
public String getPassword()
```


Ottiene la password per aprire un documento crittografato. Può essere  null  o una stringa vuota. Il valore predefinito è  null .

 **Remarks:** 

È necessario conoscere la password per aprire un documento crittografato. Se il documento non è crittografato, impostare questo valore su  null  o una stringa vuota.

 **Examples:** 

Mostra come firmare un file di documento crittografato.

```

 // Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a comment, date, and decryption password which will be applied with our new digital signature.
 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("Comment");
     signOptions.setSignTime(new Date());
     signOptions.setDecryptionPassword("docPassword");
 }

 // Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
 String inputFileName = getMyDir() + "Encrypted.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.DecryptionPassword.docx";

 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Returns:**
java.lang.String - La password per aprire un documento crittografato.
### getPreserveIncludePictureField() {#getPreserveIncludePictureField}
```
public boolean getPreserveIncludePictureField()
```


Restituisce se preservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è false.

 **Remarks:** 

Per impostazione predefinita, il campo INCLUDEPICTURE viene convertito in un oggetto forma. È possibile sovrascrivere questo comportamento se è necessario preservare il campo, ad esempio, se si desidera aggiornarlo programmaticamente. Tuttavia, si noti che questo approccio non è comune per Aspose.Words. Usalo a tuo rischio.

Uno dei possibili casi d'uso può essere l'utilizzo di un MERGEFIELD come campo figlio per modificare dinamicamente il percorso di origine dell'immagine. In questo caso è necessario che il campo INCLUDEPICTURE sia preservato nel modello.

 **Examples:** 

Mostra come preservare o scartare i campi INCLUDEPICTURE durante il caricamento di un documento.

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

**Returns:**
boolean - Indica se preservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word.
### getProgressCallback() {#getProgressCallback}
```
public IDocumentLoadingCallback getProgressCallback()
```


Chiamato durante il caricamento di un documento e accetta dati sul progresso del caricamento.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

Mostra come notificare l'utente se il caricamento del documento ha superato il tempo di caricamento previsto.

```

 public void progressCallback() throws Exception
 {
     LoadingProgressCallback progressCallback = new LoadingProgressCallback();

     LoadOptions loadOptions = new LoadOptions(); { loadOptions.setProgressCallback(progressCallback); }

     try
     {
         new Document(getMyDir() + "Big document.docx", loadOptions);
     }
     catch (IllegalStateException exception)
     {
         System.out.println(exception.getMessage());
         // Handle loading duration issue.
     }
 }

 /// 
 /// Cancel a document loading after the "MaxDuration" seconds.
 /// 
 public static class LoadingProgressCallback implements IDocumentLoadingCallback
 {
     /// 
     /// Ctr.
     /// 
     public LoadingProgressCallback()
     {
         mLoadingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document loading.
     /// 
     /// Loading arguments.
     public void notify(DocumentLoadingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mLoadingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document loading is started.
     /// 
     private Date mLoadingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.5;
 }
 
```

**Returns:**
[IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) - The corresponding [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) value.
### getRecoveryMode() {#getRecoveryMode}
```
public int getRecoveryMode()
```


Definisce come il documento deve essere gestito se si verificano errori durante il caricamento. Utilizza questa proprietà per specificare se il sistema deve tentare di recuperare il documento o seguire un altro comportamento definito. Il valore predefinito è [DocumentRecoveryMode.TRY\_RECOVER](../../com.aspose.words/documentrecoverymode/\#TRY-RECOVER).

 **Examples:** 

Mostra come provare a recuperare un documento se si sono verificati errori durante il caricamento.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Returns:**
int - Il valore int corrispondente. Il valore restituito è una delle costanti [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/).
### getResourceLoadingCallback() {#getResourceLoadingCallback}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Consente di controllare come le risorse esterne (immagini, fogli di stile) vengono caricate quando un documento è importato da HTML, MHTML.

 **Examples:** 

Mostra come gestire le risorse esterne durante il caricamento dei documenti Html.

```

 public void loadOptionsCallback() throws Exception {
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setResourceLoadingCallback(new HtmlLinkedResourceLoadingCallback());

     // When we load the document, our callback will handle linked resources such as CSS stylesheets and images.
     Document doc = new Document(getMyDir() + "Images.html", loadOptions);
     doc.save(getArtifactsDir() + "LoadOptions.LoadOptionsCallback.pdf");
 }

 /// 
 /// Prints the filenames of all external stylesheets and substitutes all images of a loaded html document.
 /// 
 private static class HtmlLinkedResourceLoadingCallback implements IResourceLoadingCallback {
     public int resourceLoading(ResourceLoadingArgs args) throws IOException {
         switch (args.getResourceType()) {
             case ResourceType.CSS_STYLE_SHEET:
                 System.out.println(MessageFormat.format("External CSS Stylesheet found upon loading: {0}", args.getOriginalUri()));
                 return ResourceLoadingAction.DEFAULT;
             case ResourceType.IMAGE:
                 System.out.println(MessageFormat.format("External Image found upon loading: {0}", args.getOriginalUri()));

                 final String newImageFilename = "Logo.jpg";
                 System.out.println(MessageFormat.format("\tImage will be substituted with: {0}", newImageFilename));

                 byte[] imageBytes = FileUtils.readFileToByteArray(new File(getImageDir() + newImageFilename));
                 args.setData(imageBytes);

                 return ResourceLoadingAction.USER_PROVIDED;
         }

         return ResourceLoadingAction.DEFAULT;
     }
 }
 
```

**Returns:**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) - The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) value.
### getTempFolder() {#getTempFolder}
```
public String getTempFolder()
```


Consente di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita questa proprietà è null e non vengono utilizzati file temporanei.

 **Remarks:** 

La cartella deve esistere ed essere scrivibile, altrimenti verrà generata un'eccezione.

Aspose.Words elimina automaticamente tutti i file temporanei al termine della lettura.

 **Examples:** 

Mostra come caricare un documento utilizzando file temporanei.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

Mostra come utilizzare il disco rigido invece della memoria durante il caricamento di un documento.

```

 // When we load a document, various elements are temporarily stored in memory as the save operation occurs.
 // We can use this option to use a temporary folder in the local file system instead,
 // which will reduce our application's memory overhead.
 LoadOptions options = new LoadOptions();
 options.setTempFolder(getArtifactsDir() + "TempFiles");

 // The specified temporary folder must exist in the local file system before the load operation.
 Files.createDirectory(Paths.get(options.getTempFolder()));

 Document doc = new Document(getMyDir() + "Document.docx", options);

 // The folder will persist with no residual contents from the load operation.
 Assert.assertTrue(DocumentHelper.directoryGetFiles(options.getTempFolder(), "*.*").size() == 0);
 
```

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getTrailingSpacesOptions() {#getTrailingSpacesOptions}
```
public int getTrailingSpacesOptions()
```


Ottiene l'opzione preferita per la gestione degli spazi finali. Il valore predefinito è [TxtTrailingSpacesOptions.TRIM](../../com.aspose.words/txttrailingspacesoptions/\#TRIM).

 **Examples:** 

Mostra come eliminare gli spazi bianchi durante il caricamento di documenti di testo semplice.

```

 String textDoc = "      Line 1 \n" +
         "    Line 2   \n" +
         " Line 3       ";

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the start of every line.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.ConvertToIndent"
 // to remove all whitespace characters from the start of every line,
 // and then apply a left first line indent to the paragraph to simulate the effect of the whitespaces.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Trim"
 // to remove all whitespace characters from every line's start.
 loadOptions.setLeadingSpacesOptions(txtLeadingSpacesOptions);

 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the end of every line.
 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Trim" to
 // remove all whitespace characters from the end of every line.
 loadOptions.setTrailingSpacesOptions(txtTrailingSpacesOptions);

 Document doc = new Document(new ByteArrayInputStream(textDoc.getBytes()), loadOptions);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 switch (txtLeadingSpacesOptions) {
     case TxtLeadingSpacesOptions.CONVERT_TO_INDENT:
         Assert.assertEquals(37.8d, paragraphs.get(0).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(25.2d, paragraphs.get(1).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(6.3d, paragraphs.get(2).getParagraphFormat().getFirstLineIndent());

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
     case TxtLeadingSpacesOptions.PRESERVE:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("      Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("    Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith(" Line 3"));
         break;
     case TxtLeadingSpacesOptions.TRIM:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
 }

 switch (txtTrailingSpacesOptions) {
     case TxtTrailingSpacesOptions.PRESERVE:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1 \r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2   \r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3       \f"));
         break;
     case TxtTrailingSpacesOptions.TRIM:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1\r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2\r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3\f"));
         break;
 }
 
```

**Returns:**
int - Opzione preferita per la gestione degli spazi finali. Il valore restituito è una delle costanti di [TxtTrailingSpacesOptions](../../com.aspose.words/txttrailingspacesoptions/).
### getUpdateDirtyFields() {#getUpdateDirtyFields}
```
public boolean getUpdateDirtyFields()
```


Specifica se aggiornare i campi con l'attributo  dirty  .

 **Examples:** 

Mostra come utilizzare la proprietà speciale per aggiornare il risultato del campo.

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
boolean - Il valore booleano corrispondente.
### getUseSystemLcid() {#getUseSystemLcid}
```
public boolean getUseSystemLcid()
```


Restituisce se utilizzare il valore LCID ottenuto dal registro di Windows per determinare i margini predefiniti dell'impostazione pagina.

 **Remarks:** 

Se impostato su true, viene emulato il comportamento di MS Word che prende il valore LCID dal registro di Windows.

Il valore predefinito è  false .

**Returns:**
boolean - Indica se utilizzare il valore LCID ottenuto dal registro di Windows per determinare i margini predefiniti della configurazione di pagina.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe comportare una perdita di fedeltà dei dati o della formattazione.

 **Examples:** 

Mostra come stampare e memorizzare gli avvisi che si verificano durante il caricamento del documento.

```

 public void loadOptionsWarningCallback() throws Exception {
     // Create a new LoadOptions object and set its WarningCallback attribute
     // as an instance of our IWarningCallback implementation.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setWarningCallback(new DocumentLoadingWarningCallback());

     // Our callback will print all warnings that come up during the load operation.
     Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

     ArrayList warnings = ((DocumentLoadingWarningCallback)loadOptions.getWarningCallback()).getWarnings();
     Assert.assertEquals(2, warnings.size());
 }

 /// 
 /// IWarningCallback that prints warnings and their details as they arise during document loading.
 /// 
 private static class DocumentLoadingWarningCallback implements IWarningCallback {
     public void warning(WarningInfo info) {
         System.out.println(MessageFormat.format("Warning: {0}", info.getWarningType()));
         System.out.println(MessageFormat.format("\tSource: {0}", info.getSource()));
         System.out.println(MessageFormat.format("\tDescription: {0}", info.getDescription()));
         mWarnings.add(info);
     }

     public ArrayList getWarnings() {
         return mWarnings;
     }

     private final  ArrayList mWarnings = new ArrayList();
 }
 
```

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### setAutoNumberingDetection(boolean value) {#setAutoNumberingDetection-boolean}
```
public void setAutoNumberingDetection(boolean value)
```


Imposta un valore booleano che indica se il rilevamento automatico della numerazione verrà eseguito durante il caricamento di un documento. Il valore predefinito è true.

 **Examples:** 

Mostra come disabilitare il rilevamento automatico della numerazione.

```

 TxtLoadOptions options = new TxtLoadOptions(); { options.setAutoNumberingDetection(false); }
 Document doc = new Document(getMyDir() + "Number detection.txt", options);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Un valore booleano che indica se il rilevamento automatico della numerazione verrà eseguito durante il caricamento di un documento. |

### setBaseUri(String value) {#setBaseUri-java.lang.String}
```
public void setBaseUri(String value)
```


Imposta la stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando necessario. Può essere null o una stringa vuota. Il valore predefinito è null.

 **Remarks:** 

Questa proprietà viene utilizzata per risolvere gli URI relativi in assoluti nei seguenti casi:

1.  Quando si carica un documento HTML da uno stream e il documento contiene immagini con URI relativi e non ha un URI di base specificato nell'elemento BASE HTML.
2.  Quando si salva un documento in PDF e altri formati, per recuperare le immagini collegate tramite URI relativi in modo che le immagini possano essere salvate nel documento di output.

 **Examples:** 

Mostra come aprire un documento HTML con immagini da uno stream utilizzando un URI di base.

```

 InputStream stream = new FileInputStream(getMyDir() + "Document.html");
 try  {
     // Pass the URI of the base folder while loading it
     // so that any images with relative URIs in the HTML document can be found.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setBaseUri(getImageDir());

     Document doc = new Document(stream, loadOptions);

     // Verify that the first shape of the document contains a valid image.
     Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

     Assert.assertTrue(shape.isImage());
     Assert.assertNotNull(shape.getImageData().getImageBytes());
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getWidth()), 0.01);
     Assert.assertEquals(32.0, ConvertUtil.pointToPixel(shape.getHeight()), 0.01);
 } finally {
     if (stream != null) stream.close();
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | La stringa che verrà utilizzata per risolvere gli URI relativi trovati nel documento in URI assoluti quando necessario. |

### setConvertMetafilesToPng(boolean value) {#setConvertMetafilesToPng-boolean}
```
public void setConvertMetafilesToPng(boolean value)
```


Imposta se convertire le immagini metafile( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) nel formato immagine **F:Aspose.FileFormat.Png**.

 **Remarks:** 

I metafili ( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) sono un formato immagine non compresso e a volte richiedono troppa RAM per contenere e elaborare il documento. Questa opzione consente di convertire tutte le immagini metafile in **F:Aspose.FileFormat.Png** durante il caricamento del documento. Nota: la conversione di grafica vettoriale in raster diminuisce la qualità delle immagini.

 **Examples:** 

Mostra come convertire WMF/EMF in PNG durante il caricamento del documento.

```

 Document doc = new Document();

 Shape shape = new Shape(doc, ShapeType.IMAGE);
 shape.getImageData().setImage(getImageDir() + "Windows MetaFile.wmf");
 shape.setWidth(100.0);
 shape.setHeight(100.0);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(shape);

 doc.save(getArtifactsDir() + "Image.CreateImageDirectly.docx");

 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.WMF, shape);

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setConvertMetafilesToPng(true);

 doc = new Document(getArtifactsDir() + "Image.CreateImageDirectly.docx", loadOptions);
 shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);

 TestUtil.verifyImageInShape(1600, 1600, ImageType.PNG, shape);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Indica se convertire le immagini metafile (**F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) nel formato immagine **F:Aspose.FileFormat.Png**. |

### setConvertShapeToOfficeMath(boolean value) {#setConvertShapeToOfficeMath-boolean}
```
public void setConvertShapeToOfficeMath(boolean value)
```


Imposta se convertire le forme con EquationXML in oggetti Office Math.

 **Examples:** 

Mostra come convertire le forme EquationXML in oggetti Office Math.

```

 LoadOptions loadOptions = new LoadOptions();

 // Use this flag to specify whether to convert the shapes with EquationXML attributes
 // to Office Math objects and then load the document.
 loadOptions.setConvertShapeToOfficeMath(isConvertShapeToOfficeMath);

 Document doc = new Document(getMyDir() + "Math shapes.docx", loadOptions);

 if (isConvertShapeToOfficeMath) {
     Assert.assertEquals(16, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(34, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 } else {
     Assert.assertEquals(24, doc.getChildNodes(NodeType.SHAPE, true).getCount());
     Assert.assertEquals(0, doc.getChildNodes(NodeType.OFFICE_MATH, true).getCount());
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Indica se convertire le forme con EquationXML in oggetti Office Math. |

### setDetectHyperlinks(boolean value) {#setDetectHyperlinks-boolean}
```
public void setDetectHyperlinks(boolean value)
```


Specifica se rilevare i collegamenti ipertestuali nel testo. Il valore predefinito è false.

 **Examples:** 

Mostra come leggere e visualizzare i collegamenti ipertestuali.

```

 final String INPUT_TEXT = "Some links in TXT:\n" +
         "https://www.aspose.com/\n" +
         "https://docs.aspose.com/words/net/\n";

 try (ByteArrayInputStream stream = new ByteArrayInputStream(INPUT_TEXT.getBytes(StandardCharsets.US_ASCII)))
 {
     // Load document with hyperlinks.
     TxtLoadOptions loadOptions = new TxtLoadOptions();
     loadOptions.setDetectHyperlinks(true);
     Document doc = new Document(stream, loadOptions);

     // Print hyperlinks text.
     for (Field field : doc.getRange().getFields())
         System.out.println(field.getResult());

     Assert.assertEquals(doc.getRange().getFields().get(0).getResult().trim(), "https://www.aspose.com/");
     Assert.assertEquals(doc.getRange().getFields().get(1).getResult().trim(), "https://docs.aspose.com/words/net/");
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setDetectNumberingWithWhitespaces(boolean value) {#setDetectNumberingWithWhitespaces-boolean}
```
public void setDetectNumberingWithWhitespaces(boolean value)
```


Consente di specificare come vengono riconosciuti gli elementi di elenchi numerati quando il documento è importato da formato di testo semplice. Il valore predefinito è true.

 **Remarks:** 

Se questa opzione è impostata su false, l'algoritmo di riconoscimento degli elenchi rileva i paragrafi di elenco quando i numeri degli elenchi terminano con un punto, una parentesi chiusa o simboli di elenco puntato (come \"\\\\u2022\", \"\\*\", \"-\" o \"o\").

Se questa opzione è impostata su true, gli spazi bianchi sono anche usati come delimitatori dei numeri di elenco: l'algoritmo di riconoscimento degli elenchi per la numerazione in stile arabo (1., 1.1.2.) utilizza sia gli spazi bianchi sia il punto (\".\") come simboli.

 **Examples:** 

Mostra come rilevare gli elenchi durante il caricamento di documenti di testo semplice.

```

 // Create a plaintext document in a string with four separate parts that we may interpret as lists,
 // with different delimiters. Upon loading the plaintext document into a "Document" object,
 // Aspose.Words will always detect the first three lists and will add a "List" object
 // for each to the document's "Lists" property.
 final String TEXT_DOC = "Full stop delimiters:\n" +
         "1. First list item 1\n" +
         "2. First list item 2\n" +
         "3. First list item 3\n\n" +
         "Right bracket delimiters:\n" +
         "1) Second list item 1\n" +
         "2) Second list item 2\n" +
         "3) Second list item 3\n\n" +
         "Bullet delimiters:\n" +
         "\u2022 Third list item 1\n" +
         "\u2022 Third list item 2\n" +
         "\u2022 Third list item 3\n\n" +
         "Whitespace delimiters:\n" +
         "1 Fourth list item 1\n" +
         "2 Fourth list item 2\n" +
         "3 Fourth list item 3";

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DetectNumberingWithWhitespaces" property to "true" to detect numbered items
 // with whitespace delimiters, such as the fourth list in our document, as lists.
 // This may also falsely detect paragraphs that begin with numbers as lists.
 // Set the "DetectNumberingWithWhitespaces" property to "false"
 // to not create lists from numbered items with whitespace delimiters.
 loadOptions.setDetectNumberingWithWhitespaces(detectNumberingWithWhitespaces);

 Document doc = new Document(new ByteArrayInputStream(TEXT_DOC.getBytes()), loadOptions);

 List paragraphList = Arrays.stream(doc.getFirstSection().getBody().getParagraphs().toArray())
         .filter(Paragraph.class::isInstance)
         .map(Paragraph.class::cast)
         .collect(Collectors.toList());

 if (detectNumberingWithWhitespaces) {
     Assert.assertEquals(4, doc.getLists().getCount());
     Assert.assertTrue(IterableUtils.matchesAny(paragraphList, s -> s.getText().contains("Fourth list") && s.isListItem()));
 } else {
     Assert.assertEquals(3, doc.getLists().getCount());
     Assert.assertFalse(IterableUtils.matchesAny(paragraphList, s -> s.getText().contains("Fourth list") && s.isListItem()));
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setDocumentDirection(int value) {#setDocumentDirection-int}
```
public void setDocumentDirection(int value)
```


Imposta la direzione del documento. Il valore predefinito è [DocumentDirection.LEFT\_TO\_RIGHT](../../com.aspose.words/documentdirection/\#LEFT-TO-RIGHT).

 **Examples:** 

Mostra come rilevare la direzione del testo di un documento di testo semplice.

```

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
 // the direction of every paragraph of text that Aspose.Words loads from plaintext.
 // Each paragraph's "Bidi" property will store its direction.
 loadOptions.setDocumentDirection(DocumentDirection.AUTO);

 // Detect Hebrew text as right-to-left.
 Document doc = new Document(getMyDir() + "Hebrew text.txt", loadOptions);

 Assert.assertTrue(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());

 // Detect English text as right-to-left.
 doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertFalse(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Una direzione del documento. Il valore deve essere una delle costanti di [DocumentDirection](../../com.aspose.words/documentdirection/). |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset}
```
public void setEncoding(Charset value)
```


Imposta la codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. Può essere null. Il valore predefinito è null.

 **Remarks:** 

Questa proprietà viene utilizzata solo durante il caricamento di documenti HTML, TXT o CHM.

Se la codifica non è specificata all'interno del documento e questa proprietà è  null , il sistema proverà a rilevare automaticamente la codifica.

 **Examples:** 

Mostra come impostare la codifica con cui aprire un documento.

```

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setEncoding(StandardCharsets.US_ASCII);
 }

 // Load the document while passing the LoadOptions object, then verify the document's contents.
 Document doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertTrue(doc.toString(SaveFormat.TEXT).contains("This is a sample text in English."));
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.nio.charset.Charset | La codifica che verrà utilizzata per caricare un documento HTML, TXT o CHM se la codifica non è specificata all'interno del documento. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Consente di specificare le impostazioni dei caratteri del documento.

 **Remarks:** 

Durante il caricamento di alcuni formati, Aspose.Words potrebbe dover risolvere i font. Ad esempio, durante il caricamento di documenti HTML Aspose.Words può risolvere i font per eseguire il fallback dei font.

Se impostato su  null , verranno utilizzate le impostazioni predefinite dei font statici [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance).

Il valore predefinito è  null .

 **Examples:** 

Mostra come designare i sostituti dei caratteri durante il caricamento.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(new FontSettings());

 // Set a font substitution rule for a LoadOptions object.
 // If the document we are loading uses a font which we do not have,
 // this rule will substitute the unavailable font with one that does exist.
 // In this case, all uses of the "MissingFont" will convert to "Comic Sans MS".
 TableSubstitutionRule substitutionRule = loadOptions.getFontSettings().getSubstitutionSettings().getTableSubstitution();
 substitutionRule.addSubstitutes("MissingFont", "Comic Sans MS");

 Document doc = new Document(getMyDir() + "Missing font.html", loadOptions);

 // At this point such text will still be in "MissingFont".
 // Font substitution will take place when we render the document.
 Assert.assertEquals("MissingFont", doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getFont().getName());

 doc.save(getArtifactsDir() + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
 
```

Mostra come applicare le impostazioni di sostituzione dei caratteri durante il caricamento di un documento.

```

 // Create a FontSettings object that will substitute the "Times New Roman" font
 // with the font "Arvo" from our "MyFonts" folder.
 FontSettings fontSettings = new FontSettings();
 fontSettings.setFontsFolder(getFontsDir(), false);
 fontSettings.getSubstitutionSettings().getTableSubstitution().addSubstitutes("Times New Roman", "Arvo");

 // Set that FontSettings object as a property of a newly created LoadOptions object.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setFontSettings(fontSettings);

 // Load the document, then render it as a PDF with the font substitution.
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.FontSettings.pdf");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | Il valore corrispondente di [FontSettings](../../com.aspose.words/fontsettings/). |

### setIgnoreOleData(boolean value) {#setIgnoreOleData-boolean}
```
public void setIgnoreOleData(boolean value)
```


Specifica se ignorare i dati OLE.

 **Remarks:** 

Ignorare i dati OLE può ridurre il consumo di memoria e aumentare le prestazioni senza perdita di dati nel caso in cui il formato di destinazione non supporti oggetti OLE.

Il valore predefinito è  false .

 **Examples:** 

Mostra come ignorare i dati OLE durante il caricamento.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setLeadingSpacesOptions(int value) {#setLeadingSpacesOptions-int}
```
public void setLeadingSpacesOptions(int value)
```


Imposta l'opzione preferita per la gestione degli spazi iniziali. Il valore predefinito è [TxtLeadingSpacesOptions.CONVERT\_TO\_INDENT](../../com.aspose.words/txtleadingspacesoptions/\#CONVERT-TO-INDENT).

 **Examples:** 

Mostra come eliminare gli spazi bianchi durante il caricamento di documenti di testo semplice.

```

 String textDoc = "      Line 1 \n" +
         "    Line 2   \n" +
         " Line 3       ";

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the start of every line.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.ConvertToIndent"
 // to remove all whitespace characters from the start of every line,
 // and then apply a left first line indent to the paragraph to simulate the effect of the whitespaces.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Trim"
 // to remove all whitespace characters from every line's start.
 loadOptions.setLeadingSpacesOptions(txtLeadingSpacesOptions);

 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the end of every line.
 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Trim" to
 // remove all whitespace characters from the end of every line.
 loadOptions.setTrailingSpacesOptions(txtTrailingSpacesOptions);

 Document doc = new Document(new ByteArrayInputStream(textDoc.getBytes()), loadOptions);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 switch (txtLeadingSpacesOptions) {
     case TxtLeadingSpacesOptions.CONVERT_TO_INDENT:
         Assert.assertEquals(37.8d, paragraphs.get(0).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(25.2d, paragraphs.get(1).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(6.3d, paragraphs.get(2).getParagraphFormat().getFirstLineIndent());

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
     case TxtLeadingSpacesOptions.PRESERVE:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("      Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("    Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith(" Line 3"));
         break;
     case TxtLeadingSpacesOptions.TRIM:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
 }

 switch (txtTrailingSpacesOptions) {
     case TxtTrailingSpacesOptions.PRESERVE:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1 \r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2   \r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3       \f"));
         break;
     case TxtTrailingSpacesOptions.TRIM:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1\r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2\r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3\f"));
         break;
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Opzione preferita per la gestione degli spazi iniziali. Il valore deve essere una delle costanti di [TxtLeadingSpacesOptions](../../com.aspose.words/txtleadingspacesoptions/). |

### setLoadFormat(int value) {#setLoadFormat-int}
```
public void setLoadFormat(int value)
```


Specifica il formato del documento da caricare. Il valore predefinito è [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO).

 **Remarks:** 

Si consiglia di specificare il valore [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) e lasciare che Aspose.Words rilevi automaticamente il formato del file. Se conosci il formato del documento che stai per caricare, puoi specificarlo esplicitamente e questo ridurrà leggermente il tempo di caricamento eliminando l'overhead associato al rilevamento automatico del formato. Se specifichi un formato di caricamento esplicito e risulta errato, verrà invocata la rilevazione automatica e verrà effettuato un secondo tentativo di caricamento del file.

 **Examples:** 

Mostra come specificare un URI di base quando si apre un documento html.

```

 // Suppose we want to load an .html document that contains an image linked by a relative URI
 // while the image is in a different location. In that case, we will need to resolve the relative URI into an absolute one.
 // We can provide a base URI using an HtmlLoadOptions object.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.HTML, "", getImageDir());

 Assert.assertEquals(LoadFormat.HTML, loadOptions.getLoadFormat());

 Document doc = new Document(getMyDir() + "Missing image.html", loadOptions);

 // While the image was broken in the input .html, our custom base URI helped us repair the link.
 Shape imageShape = (Shape) doc.getChildNodes(NodeType.SHAPE, true).get(0);
 Assert.assertTrue(imageShape.isImage());

 // This output document will display the image that was missing.
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BaseUri.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [LoadFormat](../../com.aspose.words/loadformat/). |

### setMswVersion(int value) {#setMswVersion-int}
```
public void setMswVersion(int value)
```


Consente di specificare che il processo di caricamento del documento debba corrispondere a una versione specifica di MS Word. Il valore predefinito è [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019).

 **Remarks:** 

Versioni diverse di Word possono gestire alcuni aspetti del contenuto e della formattazione del documento in modo leggermente diverso durante il processo di caricamento, il che può comportare piccole differenze nel Document Object Model.

 **Examples:** 

Mostra come emulare la procedura di caricamento di una specifica versione di Microsoft Word durante il caricamento del documento.

```

 // By default, Aspose.Words load documents according to Microsoft Word 2019 specification.
 LoadOptions loadOptions = new LoadOptions();

 Assert.assertEquals(MsWordVersion.WORD_2019, loadOptions.getMswVersion());

 // This document is missing the default paragraph formatting style.
 // This default style will be regenerated when we load the document either with Microsoft Word or Aspose.Words.
 loadOptions.setMswVersion(MsWordVersion.WORD_2007);
 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

 // The style's line spacing will have this value when loaded by Microsoft Word 2007 specification.
 Assert.assertEquals(12.95d, doc.getStyles().getDefaultParagraphFormat().getLineSpacing(), 0.01d);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [MsWordVersion](../../com.aspose.words/mswordversion/). |

### setPassword(String value) {#setPassword-java.lang.String}
```
public void setPassword(String value)
```


Imposta la password per aprire un documento crittografato. Può essere null o una stringa vuota. Il valore predefinito è null.

 **Remarks:** 

È necessario conoscere la password per aprire un documento crittografato. Se il documento non è crittografato, impostare questo valore su  null  o una stringa vuota.

 **Examples:** 

Mostra come firmare un file di documento crittografato.

```

 // Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 // Create a comment, date, and decryption password which will be applied with our new digital signature.
 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("Comment");
     signOptions.setSignTime(new Date());
     signOptions.setDecryptionPassword("docPassword");
 }

 // Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
 String inputFileName = getMyDir() + "Encrypted.docx";
 String outputFileName = getArtifactsDir() + "DigitalSignatureUtil.DecryptionPassword.docx";

 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | La password per aprire un documento crittografato. |

### setPreserveIncludePictureField(boolean value) {#setPreserveIncludePictureField-boolean}
```
public void setPreserveIncludePictureField(boolean value)
```


Imposta se conservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è false.

 **Remarks:** 

Per impostazione predefinita, il campo INCLUDEPICTURE viene convertito in un oggetto forma. È possibile sovrascrivere questo comportamento se è necessario preservare il campo, ad esempio, se si desidera aggiornarlo programmaticamente. Tuttavia, si noti che questo approccio non è comune per Aspose.Words. Usalo a tuo rischio.

Uno dei possibili casi d'uso può essere l'utilizzo di un MERGEFIELD come campo figlio per modificare dinamicamente il percorso di origine dell'immagine. In questo caso è necessario che il campo INCLUDEPICTURE sia preservato nel modello.

 **Examples:** 

Mostra come preservare o scartare i campi INCLUDEPICTURE durante il caricamento di un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Indica se conservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. |

### setProgressCallback(IDocumentLoadingCallback value) {#setProgressCallback-com.aspose.words.IDocumentLoadingCallback}
```
public void setProgressCallback(IDocumentLoadingCallback value)
```


Chiamato durante il caricamento di un documento e accetta dati sul progresso del caricamento.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

Mostra come notificare l'utente se il caricamento del documento ha superato il tempo di caricamento previsto.

```

 public void progressCallback() throws Exception
 {
     LoadingProgressCallback progressCallback = new LoadingProgressCallback();

     LoadOptions loadOptions = new LoadOptions(); { loadOptions.setProgressCallback(progressCallback); }

     try
     {
         new Document(getMyDir() + "Big document.docx", loadOptions);
     }
     catch (IllegalStateException exception)
     {
         System.out.println(exception.getMessage());
         // Handle loading duration issue.
     }
 }

 /// 
 /// Cancel a document loading after the "MaxDuration" seconds.
 /// 
 public static class LoadingProgressCallback implements IDocumentLoadingCallback
 {
     /// 
     /// Ctr.
     /// 
     public LoadingProgressCallback()
     {
         mLoadingStartedAt = new Date();
     }

     /// 
     /// Callback method which called during document loading.
     /// 
     /// Loading arguments.
     public void notify(DocumentLoadingArgs args)
     {
         Date canceledAt = new Date();
         long diff = canceledAt.getTime() - mLoadingStartedAt.getTime();
         long ellapsedSeconds = TimeUnit.MILLISECONDS.toSeconds(diff);

         if (ellapsedSeconds > MAX_DURATION)
             throw new IllegalStateException(MessageFormat.format("EstimatedProgress = {0}; CanceledAt = {1}", args.getEstimatedProgress(), canceledAt));
     }

     /// 
     /// Date and time when document loading is started.
     /// 
     private Date mLoadingStartedAt;

     /// 
     /// Maximum allowed duration in sec.
     /// 
     private static final double MAX_DURATION = 0.5;
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) | Il valore corrispondente di [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/). |

### setRecoveryMode(int value) {#setRecoveryMode-int}
```
public void setRecoveryMode(int value)
```


Definisce come il documento deve essere gestito se si verificano errori durante il caricamento. Utilizza questa proprietà per specificare se il sistema deve tentare di recuperare il documento o seguire un altro comportamento definito. Il valore predefinito è [DocumentRecoveryMode.TRY\_RECOVER](../../com.aspose.words/documentrecoverymode/\#TRY-RECOVER).

 **Examples:** 

Mostra come provare a recuperare un documento se si sono verificati errori durante il caricamento.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore int corrispondente. Il valore deve essere una delle costanti di [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/). |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Consente di controllare come le risorse esterne (immagini, fogli di stile) vengono caricate quando un documento è importato da HTML, MHTML.

 **Examples:** 

Mostra come gestire le risorse esterne durante il caricamento dei documenti Html.

```

 public void loadOptionsCallback() throws Exception {
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setResourceLoadingCallback(new HtmlLinkedResourceLoadingCallback());

     // When we load the document, our callback will handle linked resources such as CSS stylesheets and images.
     Document doc = new Document(getMyDir() + "Images.html", loadOptions);
     doc.save(getArtifactsDir() + "LoadOptions.LoadOptionsCallback.pdf");
 }

 /// 
 /// Prints the filenames of all external stylesheets and substitutes all images of a loaded html document.
 /// 
 private static class HtmlLinkedResourceLoadingCallback implements IResourceLoadingCallback {
     public int resourceLoading(ResourceLoadingArgs args) throws IOException {
         switch (args.getResourceType()) {
             case ResourceType.CSS_STYLE_SHEET:
                 System.out.println(MessageFormat.format("External CSS Stylesheet found upon loading: {0}", args.getOriginalUri()));
                 return ResourceLoadingAction.DEFAULT;
             case ResourceType.IMAGE:
                 System.out.println(MessageFormat.format("External Image found upon loading: {0}", args.getOriginalUri()));

                 final String newImageFilename = "Logo.jpg";
                 System.out.println(MessageFormat.format("\tImage will be substituted with: {0}", newImageFilename));

                 byte[] imageBytes = FileUtils.readFileToByteArray(new File(getImageDir() + newImageFilename));
                 args.setData(imageBytes);

                 return ResourceLoadingAction.USER_PROVIDED;
         }

         return ResourceLoadingAction.DEFAULT;
     }
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) | Il valore corrispondente di [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/). |

### setTempFolder(String value) {#setTempFolder-java.lang.String}
```
public void setTempFolder(String value)
```


Consente di utilizzare file temporanei durante la lettura del documento. Per impostazione predefinita questa proprietà è null e non vengono utilizzati file temporanei.

 **Remarks:** 

La cartella deve esistere ed essere scrivibile, altrimenti verrà generata un'eccezione.

Aspose.Words elimina automaticamente tutti i file temporanei al termine della lettura.

 **Examples:** 

Mostra come caricare un documento utilizzando file temporanei.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

Mostra come utilizzare il disco rigido invece della memoria durante il caricamento di un documento.

```

 // When we load a document, various elements are temporarily stored in memory as the save operation occurs.
 // We can use this option to use a temporary folder in the local file system instead,
 // which will reduce our application's memory overhead.
 LoadOptions options = new LoadOptions();
 options.setTempFolder(getArtifactsDir() + "TempFiles");

 // The specified temporary folder must exist in the local file system before the load operation.
 Files.createDirectory(Paths.get(options.getTempFolder()));

 Document doc = new Document(getMyDir() + "Document.docx", options);

 // The folder will persist with no residual contents from the load operation.
 Assert.assertTrue(DocumentHelper.directoryGetFiles(options.getTempFolder(), "*.*").size() == 0);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

### setTrailingSpacesOptions(int value) {#setTrailingSpacesOptions-int}
```
public void setTrailingSpacesOptions(int value)
```


Imposta l'opzione preferita per la gestione degli spazi finali. Il valore predefinito è [TxtTrailingSpacesOptions.TRIM](../../com.aspose.words/txttrailingspacesoptions/\#TRIM).

 **Examples:** 

Mostra come eliminare gli spazi bianchi durante il caricamento di documenti di testo semplice.

```

 String textDoc = "      Line 1 \n" +
         "    Line 2   \n" +
         " Line 3       ";

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the start of every line.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.ConvertToIndent"
 // to remove all whitespace characters from the start of every line,
 // and then apply a left first line indent to the paragraph to simulate the effect of the whitespaces.
 // Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Trim"
 // to remove all whitespace characters from every line's start.
 loadOptions.setLeadingSpacesOptions(txtLeadingSpacesOptions);

 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Preserve"
 // to preserve all whitespace characters at the end of every line.
 // Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Trim" to
 // remove all whitespace characters from the end of every line.
 loadOptions.setTrailingSpacesOptions(txtTrailingSpacesOptions);

 Document doc = new Document(new ByteArrayInputStream(textDoc.getBytes()), loadOptions);
 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 switch (txtLeadingSpacesOptions) {
     case TxtLeadingSpacesOptions.CONVERT_TO_INDENT:
         Assert.assertEquals(37.8d, paragraphs.get(0).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(25.2d, paragraphs.get(1).getParagraphFormat().getFirstLineIndent());
         Assert.assertEquals(6.3d, paragraphs.get(2).getParagraphFormat().getFirstLineIndent());

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
     case TxtLeadingSpacesOptions.PRESERVE:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("      Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("    Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith(" Line 3"));
         break;
     case TxtLeadingSpacesOptions.TRIM:
         Assert.assertTrue(IterableUtils.matchesAll(paragraphs, s -> s.getParagraphFormat().getFirstLineIndent() == 0.0d));

         Assert.assertTrue(paragraphs.get(0).getText().startsWith("Line 1"));
         Assert.assertTrue(paragraphs.get(1).getText().startsWith("Line 2"));
         Assert.assertTrue(paragraphs.get(2).getText().startsWith("Line 3"));
         break;
 }

 switch (txtTrailingSpacesOptions) {
     case TxtTrailingSpacesOptions.PRESERVE:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1 \r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2   \r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3       \f"));
         break;
     case TxtTrailingSpacesOptions.TRIM:
         Assert.assertTrue(paragraphs.get(0).getText().endsWith("Line 1\r"));
         Assert.assertTrue(paragraphs.get(1).getText().endsWith("Line 2\r"));
         Assert.assertTrue(paragraphs.get(2).getText().endsWith("Line 3\f"));
         break;
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Opzione preferita per la gestione degli spazi finali. Il valore deve essere una delle costanti di [TxtTrailingSpacesOptions](../../com.aspose.words/txttrailingspacesoptions/). |

### setUpdateDirtyFields(boolean value) {#setUpdateDirtyFields-boolean}
```
public void setUpdateDirtyFields(boolean value)
```


Specifica se aggiornare i campi con l'attributo  dirty  .

 **Examples:** 

Mostra come utilizzare la proprietà speciale per aggiornare il risultato del campo.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setUseSystemLcid(boolean value) {#setUseSystemLcid-boolean}
```
public void setUseSystemLcid(boolean value)
```


Imposta se utilizzare il valore LCID ottenuto dal registro di Windows per determinare i margini predefiniti dell'impostazione pagina.

 **Remarks:** 

Se impostato su true, viene emulato il comportamento di MS Word che prende il valore LCID dal registro di Windows.

Il valore predefinito è  false .

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Indica se utilizzare il valore LCID ottenuto dal registro di Windows per determinare i margini predefiniti della configurazione della pagina. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe comportare una perdita di fedeltà dei dati o della formattazione.

 **Examples:** 

Mostra come stampare e memorizzare gli avvisi che si verificano durante il caricamento del documento.

```

 public void loadOptionsWarningCallback() throws Exception {
     // Create a new LoadOptions object and set its WarningCallback attribute
     // as an instance of our IWarningCallback implementation.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setWarningCallback(new DocumentLoadingWarningCallback());

     // Our callback will print all warnings that come up during the load operation.
     Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

     ArrayList warnings = ((DocumentLoadingWarningCallback)loadOptions.getWarningCallback()).getWarnings();
     Assert.assertEquals(2, warnings.size());
 }

 /// 
 /// IWarningCallback that prints warnings and their details as they arise during document loading.
 /// 
 private static class DocumentLoadingWarningCallback implements IWarningCallback {
     public void warning(WarningInfo info) {
         System.out.println(MessageFormat.format("Warning: {0}", info.getWarningType()));
         System.out.println(MessageFormat.format("\tSource: {0}", info.getSource()));
         System.out.println(MessageFormat.format("\tDescription: {0}", info.getDescription()));
         mWarnings.add(info);
     }

     public ArrayList getWarnings() {
         return mWarnings;
     }

     private final  ArrayList mWarnings = new ArrayList();
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Il valore corrispondente di [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

