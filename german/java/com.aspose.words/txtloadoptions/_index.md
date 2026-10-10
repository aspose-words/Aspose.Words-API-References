---
title: "TxtLoadOptions"
linktitle: "TxtLoadOptions"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Angeben zusätzlicher Optionen beim Laden eines LoadFormat.TEXT-Dokuments in ein Document-Objekt in Java."
type: docs
weight: 693
url: /de/java/com.aspose.words/txtloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions/)
```
public class TxtLoadOptions extends LoadOptions
```

Ermöglicht das Angeben zusätzlicher Optionen beim Laden eines [LoadFormat.TEXT](../../com.aspose.words/loadformat/\#TEXT)-Dokuments in ein [Document](../../com.aspose.words/document/)-Objekt.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Specify Load Options ][Specify Load Options].

 **Examples:** 

Zeigt, wie Hyperlinks gelesen und angezeigt werden.

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
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [TxtLoadOptions()](#TxtLoadOptions) | Initialisiert eine neue Instanz dieser Klasse mit Standardwerten. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| [getAutoNumberingDetection()](#getAutoNumberingDetection) | Gibt einen booleschen Wert zurück, der angibt, ob bei dem Laden eines Dokuments eine automatische Nummerierungserkennung durchgeführt wird. |
| [getBaseUri()](#getBaseUri) | Gibt die Zeichenkette zurück, die verwendet wird, um relative URIs im Dokument bei Bedarf in absolute URIs aufzulösen. |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng) | Gibt an, ob Metadateien (**F:Aspose.FileFormat.Wmf** oder **F:Aspose.FileFormat.Emf**) in das Bildformat **F:Aspose.FileFormat.Png** konvertiert werden sollen. |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath) | Gibt an, ob Formen mit EquationXML in Office‑Math‑Objekte konvertiert werden sollen. |
| [getDetectHyperlinks()](#getDetectHyperlinks) | Gibt an, ob Hyperlinks im Text erkannt werden sollen. |
| [getDetectNumberingWithWhitespaces()](#getDetectNumberingWithWhitespaces) | Ermöglicht die Angabe, wie nummerierte Listenelemente erkannt werden, wenn ein Dokument aus dem Nur-Text-Format importiert wird. |
| [getDocumentDirection()](#getDocumentDirection) | Gibt die Dokumentausrichtung zurück. |
| [getEncoding()](#getEncoding) | Gibt die Kodierung zurück, die zum Laden eines HTML-, TXT‑ oder CHM‑Dokuments verwendet wird, wenn die Kodierung im Dokument nicht angegeben ist. |
| [getFontSettings()](#getFontSettings) | Ermöglicht das Festlegen von Dokument‑Schrifteinstellungen. |
| [getIgnoreOleData()](#getIgnoreOleData) | Gibt an, ob OLE‑Daten ignoriert werden sollen. |
| [getLanguagePreferences()](#getLanguagePreferences) | Gibt die Spracheinstellungen zurück, die beim Laden des Dokuments verwendet werden. |
| [getLeadingSpacesOptions()](#getLeadingSpacesOptions) | Gibt die bevorzugte Option für die Behandlung von führenden Leerzeichen zurück. |
| [getLoadFormat()](#getLoadFormat) | Gibt das Format des zu ladenden Dokuments an. |
| [getMswVersion()](#getMswVersion) | Ermöglicht die Angabe, dass der Dokument‑Ladevorgang einer bestimmten MS‑Word‑Version entsprechen soll. |
| [getPassword()](#getPassword) | Gibt das Passwort zum Öffnen eines verschlüsselten Dokuments zurück. |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField) | Gibt an, ob das INCLUDEPICTURE‑Feld beim Lesen von Microsoft‑Word‑Formaten beibehalten werden soll. |
| [getProgressCallback()](#getProgressCallback) | Wird beim Laden eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt. |
| [getRecoveryMode()](#getRecoveryMode) | Definiert, wie das Dokument behandelt werden soll, wenn beim Laden Fehler auftreten. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback) | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML oder MHTML importiert wird. |
| [getTempFolder()](#getTempFolder) | Ermöglicht die Verwendung temporärer Dateien beim Lesen des Dokuments. |
| [getTrailingSpacesOptions()](#getTrailingSpacesOptions) | Liest die bevorzugte Option für die Behandlung von nachfolgenden Leerzeichen. |
| [getUpdateDirtyFields()](#getUpdateDirtyFields) | Gibt an, ob die Felder mit dem  dirty  Attribut aktualisiert werden sollen. |
| [getUseSystemLcid()](#getUseSystemLcid) | Gibt an, ob der aus der Windows-Registrierung erhaltene LCID-Wert verwendet wird, um die Standardränder der Seiteneinrichtung zu bestimmen. |
| [getWarningCallback()](#getWarningCallback) | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu Daten- oder Formatierungsverlust führen könnte. |
| [setAutoNumberingDetection(boolean value)](#setAutoNumberingDetection-boolean) | Legt einen booleschen Wert fest, der angibt, ob bei der Dokumentenladung die automatische Nummerierungserkennung durchgeführt wird. |
| [setBaseUri(String value)](#setBaseUri-java.lang.String) | Legt die Zeichenkette fest, die verwendet wird, um relative URIs im Dokument bei Bedarf in absolute URIs aufzulösen. |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean) | Legt fest, ob Metadateien ( **F:Aspose.FileFormat.Wmf** oder **F:Aspose.FileFormat.Emf**) in das Bildformat **F:Aspose.FileFormat.Png** konvertiert werden. |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean) | Legt fest, ob Formen mit EquationXML in Office Math-Objekte konvertiert werden. |
| [setDetectHyperlinks(boolean value)](#setDetectHyperlinks-boolean) | Gibt an, ob Hyperlinks im Text erkannt werden sollen. |
| [setDetectNumberingWithWhitespaces(boolean value)](#setDetectNumberingWithWhitespaces-boolean) | Ermöglicht die Angabe, wie nummerierte Listenelemente erkannt werden, wenn ein Dokument aus dem Nur-Text-Format importiert wird. |
| [setDocumentDirection(int value)](#setDocumentDirection-int) | Legt die Dokumentenrichtung fest. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) | Legt die Kodierung fest, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, wenn die Kodierung im Dokument nicht angegeben ist. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Ermöglicht das Festlegen von Dokument‑Schrifteinstellungen. |
| [setIgnoreOleData(boolean value)](#setIgnoreOleData-boolean) | Gibt an, ob OLE‑Daten ignoriert werden sollen. |
| [setLeadingSpacesOptions(int value)](#setLeadingSpacesOptions-int) | Legt die bevorzugte Option für die Behandlung von führenden Leerzeichen fest. |
| [setLoadFormat(int value)](#setLoadFormat-int) | Gibt das Format des zu ladenden Dokuments an. |
| [setMswVersion(int value)](#setMswVersion-int) | Ermöglicht die Angabe, dass der Dokument‑Ladevorgang einer bestimmten MS‑Word‑Version entsprechen soll. |
| [setPassword(String value)](#setPassword-java.lang.String) | Legt das Passwort zum Öffnen eines verschlüsselten Dokuments fest. |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean) | Legt fest, ob das INCLUDEPICTURE-Feld beim Lesen von Microsoft-Word-Formaten erhalten bleibt. |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback) | Wird beim Laden eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt. |
| [setRecoveryMode(int value)](#setRecoveryMode-int) | Definiert, wie das Dokument behandelt werden soll, wenn beim Laden Fehler auftreten. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback) | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML oder MHTML importiert wird. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Ermöglicht die Verwendung temporärer Dateien beim Lesen des Dokuments. |
| [setTrailingSpacesOptions(int value)](#setTrailingSpacesOptions-int) | Legt die bevorzugte Option für die Behandlung von nachfolgenden Leerzeichen fest. |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean) | Gibt an, ob die Felder mit dem  dirty  Attribut aktualisiert werden sollen. |
| [setUseSystemLcid(boolean value)](#setUseSystemLcid-boolean) | Legt fest, ob der aus der Windows-Registrierung erhaltene LCID-Wert verwendet wird, um die Standardränder der Seiteneinrichtung zu bestimmen. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu Daten- oder Formatierungsverlust führen könnte. |
### TxtLoadOptions() {#TxtLoadOptions}
```
public TxtLoadOptions()
```


Initialisiert eine neue Instanz dieser Klasse mit Standardwerten.

 **Examples:** 

Zeigt, wie Hyperlinks gelesen und angezeigt werden.

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


Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getAutoNumberingDetection() {#getAutoNumberingDetection}
```
public boolean getAutoNumberingDetection()
```


Liest einen booleschen Wert, der angibt, ob bei der Dokumentenladung die automatische Nummerierungserkennung durchgeführt wird. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie die automatische Nummerierungserkennung deaktiviert wird.

```

 TxtLoadOptions options = new TxtLoadOptions(); { options.setAutoNumberingDetection(false); }
 Document doc = new Document(getMyDir() + "Number detection.txt", options);
 
```

**Returns:**
boolean - Ein boolescher Wert, der angibt, ob bei der Dokumentenladung die automatische Nummerierungserkennung durchgeführt wird.
### getBaseUri() {#getBaseUri}
```
public String getBaseUri()
```


Gibt die Zeichenkette zurück, die verwendet wird, um relative URIs im Dokument bei Bedarf in absolute URIs aufzulösen. Kann  null  oder ein leerer String sein. Standard ist  null .

 **Remarks:** 

Diese Eigenschaft wird verwendet, um relative URIs in den folgenden Fällen in absolute umzuwandeln:

1.  Beim Laden eines HTML-Dokuments aus einem Stream, wenn das Dokument Bilder mit relativen URIs enthält und keine Basis-URI im BASE-HTML-Element angegeben ist.
2.  Beim Speichern eines Dokuments als PDF und in anderen Formaten, um Bilder, die über relative URIs verlinkt sind, abzurufen, damit die Bilder im Ausgabedokument gespeichert werden können.

 **Examples:** 

Zeigt, wie man ein HTML-Dokument mit Bildern aus einem Stream unter Verwendung einer Basis-URI öffnet.

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
java.lang.String - Die Zeichenkette, die verwendet wird, um gefundene relative URIs im Dokument bei Bedarf in absolute URIs aufzulösen.
### getConvertMetafilesToPng() {#getConvertMetafilesToPng}
```
public boolean getConvertMetafilesToPng()
```


Gibt an, ob Metadateien (**F:Aspose.FileFormat.Wmf** oder **F:Aspose.FileFormat.Emf**) in das Bildformat **F:Aspose.FileFormat.Png** konvertiert werden sollen.

 **Remarks:** 

Metadateien ( **F:Aspose.FileFormat.Wmf** oder **F:Aspose.FileFormat.Emf**) sind ein unkomprimiertes Bildformat und benötigen manchmal zu viel RAM, um das Dokument zu halten und zu verarbeiten. Diese Option ermöglicht es, alle Metadatei-Bilder beim Laden des Dokuments in **F:Aspose.FileFormat.Png** zu konvertieren. Bitte beachten Sie – die Konvertierung von Vektorgrafiken zu Raster verringert die Bildqualität.

 **Examples:** 

Zeigt, wie man WMF/EMF beim Laden eines Dokuments in PNG konvertiert.

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
boolean - Gibt an, ob Metadatei-Bilder ( **F:Aspose.FileFormat.Wmf** oder **F:Aspose.FileFormat.Emf**) in das Bildformat **F:Aspose.FileFormat.Png** konvertiert werden sollen.
### getConvertShapeToOfficeMath() {#getConvertShapeToOfficeMath}
```
public boolean getConvertShapeToOfficeMath()
```


Gibt an, ob Formen mit EquationXML in Office‑Math‑Objekte konvertiert werden sollen.

 **Examples:** 

Zeigt, wie man EquationXML‑Formen in Office‑Math‑Objekte konvertiert.

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
boolean - Gibt an, ob Formen mit EquationXML in Office‑Math‑Objekte konvertiert werden sollen.
### getDetectHyperlinks() {#getDetectHyperlinks}
```
public boolean getDetectHyperlinks()
```


Gibt an, ob Hyperlinks im Text erkannt werden sollen. Der Standardwert ist false.

 **Examples:** 

Zeigt, wie Hyperlinks gelesen und angezeigt werden.

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
boolean - Der entsprechende  boolean  Wert.
### getDetectNumberingWithWhitespaces() {#getDetectNumberingWithWhitespaces}
```
public boolean getDetectNumberingWithWhitespaces()
```


Ermöglicht die Angabe, wie nummerierte Listenelemente erkannt werden, wenn das Dokument aus einem Nur-Text-Format importiert wird. Der Standardwert ist true.

 **Remarks:** 

Wenn diese Option auf false gesetzt ist, erkennt der Listenerkennungsalgorithmus Listenkapitel, wenn Listennummern entweder mit einem Punkt, einer rechten Klammer oder Aufzählungszeichen (wie "\\u2022", "\*", "-" oder "o") enden.

Wenn diese Option auf true gesetzt ist, werden Leerzeichen ebenfalls als Trennzeichen für Listennummern verwendet: Der Listenerkennungsalgorithmus für arabische Nummerierung (1., 1.1.2.) nutzt sowohl Leerzeichen als auch Punkt (".")-Symbole.

 **Examples:** 

Zeigt, wie Listen beim Laden von Nur-Text-Dokumenten erkannt werden.

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
boolean - Der entsprechende  boolean  Wert.
### getDocumentDirection() {#getDocumentDirection}
```
public int getDocumentDirection()
```


Liest die Dokumentenrichtung. Der Standardwert ist [DocumentDirection.LEFT\_TO\_RIGHT](../../com.aspose.words/documentdirection/\#LEFT-TO-RIGHT).

 **Examples:** 

Zeigt, wie die Textflussrichtung eines Klartextdokuments erkannt wird.

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
int - Eine Dokumentenrichtung. Der zurückgegebene Wert ist einer der Konstanten von [DocumentDirection](../../com.aspose.words/documentdirection/).
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


Gibt die Kodierung zurück, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, wenn die Kodierung im Dokument nicht angegeben ist. Kann  null  sein. Standard ist  null .

 **Remarks:** 

Diese Eigenschaft wird nur beim Laden von HTML-, TXT- oder CHM-Dokumenten verwendet.

Wenn im Dokument keine Kodierung angegeben ist und diese Eigenschaft  null  ist, versucht das System, die Kodierung automatisch zu erkennen.

 **Examples:** 

Zeigt, wie man die Kodierung festlegt, mit der ein Dokument geöffnet wird.

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
java.nio.charset.Charset - Die Kodierung, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, wenn die Kodierung im Dokument nicht angegeben ist.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Ermöglicht das Festlegen von Dokument‑Schrifteinstellungen.

 **Remarks:** 

Beim Laden einiger Formate kann Aspose.Words das Auflösen der Schriftarten erfordern. Zum Beispiel kann Aspose.Words beim Laden von HTML-Dokumenten die Schriftarten auflösen, um einen Schriftarten‑Fallback durchzuführen.

Wenn auf  null  gesetzt, werden die standardmäßigen statischen Schriftarteinstellungen [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance) verwendet.

Der Standardwert ist  null .

 **Examples:** 

Zeigt, wie man Schriftart‑Ersatz während des Ladens festlegt.

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

Zeigt, wie man Einstellungen für den Schriftart‑Ersatz beim Laden eines Dokuments anwendet.

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


Gibt an, ob OLE‑Daten ignoriert werden sollen.

 **Remarks:** 

Das Ignorieren von OLE‑Daten kann den Speicherverbrauch reduzieren und die Leistung steigern, ohne dass Daten verloren gehen, wenn das Zielformat OLE‑Objekte nicht unterstützt.

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man OLE‑Daten beim Laden ignoriert.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getLanguagePreferences() {#getLanguagePreferences}
```
public LanguagePreferences getLanguagePreferences()
```


Gibt die Spracheinstellungen zurück, die beim Laden des Dokuments verwendet werden.

 **Examples:** 

Zeigt, wie man Sprachpräferenzen beim Laden eines Dokuments anwendet.

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


Liest die bevorzugte Option für die Behandlung von führenden Leerzeichen. Der Standardwert ist [TxtLeadingSpacesOptions.CONVERT\_TO\_INDENT](../../com.aspose.words/txtleadingspacesoptions/\#CONVERT-TO-INDENT).

 **Examples:** 

Zeigt, wie Leerzeichen beim Laden von Nur-Text-Dokumenten getrimmt werden.

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
int - Bevorzugte Option für die Behandlung von führenden Leerzeichen. Der zurückgegebene Wert ist einer der Konstanten von [TxtLeadingSpacesOptions](../../com.aspose.words/txtleadingspacesoptions/).
### getLoadFormat() {#getLoadFormat}
```
public int getLoadFormat()
```


Gibt das Format des zu ladenden Dokuments an. Standard ist [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO).

 **Remarks:** 

Es wird empfohlen, den Wert [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) anzugeben und Aspose.Words das Dateiformat automatisch erkennen zu lassen. Wenn Sie das Format des zu ladenden Dokuments kennen, können Sie das Format explizit angeben, wodurch die Ladezeit durch den Aufwand für die automatische Erkennung leicht reduziert wird. Geben Sie ein explizites Ladeformat an und stellt sich heraus, dass es falsch ist, wird die automatische Erkennung aufgerufen und ein zweiter Versuch, die Datei zu laden, unternommen.

 **Examples:** 

Zeigt, wie man eine Basis‑URI beim Öffnen eines HTML‑Dokuments angibt.

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
int - Der entsprechende  int  Wert. Der zurückgegebene Wert ist einer der Konstanten von [LoadFormat](../../com.aspose.words/loadformat/).
### getMswVersion() {#getMswVersion}
```
public int getMswVersion()
```


Ermöglicht die Angabe, dass der Dokument‑Ladevorgang einer bestimmten MS‑Word‑Version entsprechen soll. Standardwert ist [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019)

 **Remarks:** 

Verschiedene Word‑Versionen können bestimmte Aspekte des Dokumentinhalts und der Formatierung während des Ladevorgangs leicht unterschiedlich handhaben, was zu geringfügigen Unterschieden im Document Object Model führen kann.

 **Examples:** 

Zeigt, wie man den Ladevorgang einer bestimmten Microsoft‑Word‑Version beim Dokumentenladen emuliert.

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
int - Der entsprechende  int  Wert. Der zurückgegebene Wert ist einer der Konstanten von [MsWordVersion](../../com.aspose.words/mswordversion/).
### getPassword() {#getPassword}
```
public String getPassword()
```


Gibt das Passwort zum Öffnen eines verschlüsselten Dokuments zurück. Kann  null  oder ein leerer String sein. Standard ist  null .

 **Remarks:** 

Sie müssen das Passwort kennen, um ein verschlüsseltes Dokument zu öffnen. Ist das Dokument nicht verschlüsselt, setzen Sie dies auf  null  oder einen leeren String.

 **Examples:** 

Zeigt, wie man eine verschlüsselte Dokumentdatei signiert.

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
java.lang.String - Das Passwort zum Öffnen eines verschlüsselten Dokuments.
### getPreserveIncludePictureField() {#getPreserveIncludePictureField}
```
public boolean getPreserveIncludePictureField()
```


Ermittelt, ob das INCLUDEPICTURE-Feld beim Lesen von Microsoft-Word-Formaten beibehalten werden soll. Der Standardwert ist  false .

 **Remarks:** 

Standardmäßig wird das INCLUDEPICTURE-Feld in ein Formobjekt konvertiert. Sie können dies überschreiben, wenn Sie das Feld beibehalten müssen, zum Beispiel, wenn Sie es programmgesteuert aktualisieren möchten. Beachten Sie jedoch, dass dieser Ansatz bei Aspose.Words nicht üblich ist. Verwenden Sie ihn auf eigenes Risiko.

Ein möglicher Anwendungsfall könnte die Verwendung eines MERGEFIELD als untergeordnetes Feld sein, um den Quellpfad des Bildes dynamisch zu ändern. In diesem Fall muss das INCLUDEPICTURE im Modell beibehalten werden.

 **Examples:** 

Zeigt, wie man INCLUDEPICTURE‑Felder beim Laden eines Dokuments beibehält oder verwirft.

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
boolean - Gibt an, ob das INCLUDEPICTURE-Feld beim Lesen von Microsoft-Word-Formaten beibehalten werden soll.
### getProgressCallback() {#getProgressCallback}
```
public IDocumentLoadingCallback getProgressCallback()
```


Wird beim Laden eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

Zeigt, wie der Benutzer benachrichtigt wird, wenn das Laden des Dokuments die erwartete Ladezeit überschreitet.

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


Definiert, wie das Dokument behandelt werden soll, wenn beim Laden Fehler auftreten. Verwenden Sie diese Eigenschaft, um anzugeben, ob das System versuchen soll, das Dokument wiederherzustellen oder ein anderes definiertes Verhalten zu folgen. Der Standardwert ist [DocumentRecoveryMode.TRY\_RECOVER](../../com.aspose.words/documentrecoverymode/\#TRY-RECOVER).

 **Examples:** 

Zeigt, wie versucht wird, ein Dokument wiederherzustellen, wenn beim Laden Fehler aufgetreten sind.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Returns:**
int - Der entsprechende  int  Wert. Der zurückgegebene Wert ist einer der Konstanten von [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/).
### getResourceLoadingCallback() {#getResourceLoadingCallback}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML oder MHTML importiert wird.

 **Examples:** 

Zeigt, wie externe Ressourcen beim Laden von HTML-Dokumenten behandelt werden.

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


Ermöglicht die Verwendung temporärer Dateien beim Lesen des Dokuments. Standardmäßig ist diese Eigenschaft null und es werden keine temporären Dateien verwendet.

 **Remarks:** 

Der Ordner muss existieren und beschreibbar sein, andernfalls wird eine Ausnahme ausgelöst.

Aspose.Words löscht automatisch alle temporären Dateien, wenn das Lesen abgeschlossen ist.

 **Examples:** 

Zeigt, wie ein Dokument mit temporären Dateien geladen wird.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

Zeigt, wie beim Laden eines Dokuments die Festplatte anstelle des Speichers verwendet wird.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getTrailingSpacesOptions() {#getTrailingSpacesOptions}
```
public int getTrailingSpacesOptions()
```


Liest die bevorzugte Option für die Behandlung von nachfolgenden Leerzeichen. Der Standardwert ist [TxtTrailingSpacesOptions.TRIM](../../com.aspose.words/txttrailingspacesoptions/\#TRIM).

 **Examples:** 

Zeigt, wie Leerzeichen beim Laden von Nur-Text-Dokumenten getrimmt werden.

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
int - Bevorzugte Option für die Behandlung von nachfolgenden Leerzeichen. Der zurückgegebene Wert ist einer der Konstanten von [TxtTrailingSpacesOptions](../../com.aspose.words/txttrailingspacesoptions/).
### getUpdateDirtyFields() {#getUpdateDirtyFields}
```
public boolean getUpdateDirtyFields()
```


Gibt an, ob die Felder mit dem  dirty  Attribut aktualisiert werden sollen.

 **Examples:** 

Zeigt, wie man die spezielle Eigenschaft zum Aktualisieren des Feldergebnisses verwendet.

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
boolean - Der entsprechende  boolean  Wert.
### getUseSystemLcid() {#getUseSystemLcid}
```
public boolean getUseSystemLcid()
```


Gibt an, ob der aus der Windows-Registrierung erhaltene LCID-Wert verwendet wird, um die Standardränder der Seiteneinrichtung zu bestimmen.

 **Remarks:** 

Wenn auf true gesetzt, wird das Verhalten von MS Word emuliert, das den LCID‑Wert aus der Windows‑Registrierung übernimmt.

Der Standardwert ist  false .

**Returns:**
boolean – Gibt an, ob der aus der Windows‑Registrierung erhaltene LCID‑Wert verwendet wird, um die Standardränder der Seiteneinrichtung zu bestimmen.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu Daten- oder Formatierungsverlust führen könnte.

 **Examples:** 

Zeigt, wie Warnungen, die beim Laden eines Dokuments auftreten, ausgegeben und gespeichert werden.

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


Legt einen booleschen Wert fest, der angibt, ob bei der Dokumentenladung die automatische Nummerierungserkennung durchgeführt wird. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie die automatische Nummerierungserkennung deaktiviert wird.

```

 TxtLoadOptions options = new TxtLoadOptions(); { options.setAutoNumberingDetection(false); }
 Document doc = new Document(getMyDir() + "Number detection.txt", options);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein boolescher Wert, der angibt, ob bei der Dokumentenladung die automatische Nummerierungserkennung durchgeführt wird. |

### setBaseUri(String value) {#setBaseUri-java.lang.String}
```
public void setBaseUri(String value)
```


Legt die Zeichenkette fest, die zum Auflösen relativer URIs im Dokument in absolute URIs verwendet wird, falls erforderlich. Kann null oder eine leere Zeichenkette sein. Standard ist null.

 **Remarks:** 

Diese Eigenschaft wird verwendet, um relative URIs in den folgenden Fällen in absolute umzuwandeln:

1.  Beim Laden eines HTML-Dokuments aus einem Stream, wenn das Dokument Bilder mit relativen URIs enthält und keine Basis-URI im BASE-HTML-Element angegeben ist.
2.  Beim Speichern eines Dokuments als PDF und in anderen Formaten, um Bilder, die über relative URIs verlinkt sind, abzurufen, damit die Bilder im Ausgabedokument gespeichert werden können.

 **Examples:** 

Zeigt, wie man ein HTML-Dokument mit Bildern aus einem Stream unter Verwendung einer Basis-URI öffnet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Die Zeichenkette, die zum Auflösen relativer URIs im Dokument in absolute URIs verwendet wird, falls erforderlich. |

### setConvertMetafilesToPng(boolean value) {#setConvertMetafilesToPng-boolean}
```
public void setConvertMetafilesToPng(boolean value)
```


Legt fest, ob Metadateien ( **F:Aspose.FileFormat.Wmf** oder **F:Aspose.FileFormat.Emf**) in das Bildformat **F:Aspose.FileFormat.Png** konvertiert werden.

 **Remarks:** 

Metadateien ( **F:Aspose.FileFormat.Wmf** oder **F:Aspose.FileFormat.Emf**) sind ein unkomprimiertes Bildformat und benötigen manchmal zu viel RAM, um das Dokument zu halten und zu verarbeiten. Diese Option ermöglicht es, alle Metadatei-Bilder beim Laden des Dokuments in **F:Aspose.FileFormat.Png** zu konvertieren. Bitte beachten Sie – die Konvertierung von Vektorgrafiken zu Raster verringert die Bildqualität.

 **Examples:** 

Zeigt, wie man WMF/EMF beim Laden eines Dokuments in PNG konvertiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Gibt an, ob Metadatei‑( **F:Aspose.FileFormat.Wmf** oder **F:Aspose.FileFormat.Emf**) Bilder in das Bildformat **F:Aspose.FileFormat.Png** konvertiert werden sollen. |

### setConvertShapeToOfficeMath(boolean value) {#setConvertShapeToOfficeMath-boolean}
```
public void setConvertShapeToOfficeMath(boolean value)
```


Legt fest, ob Formen mit EquationXML in Office Math-Objekte konvertiert werden.

 **Examples:** 

Zeigt, wie man EquationXML‑Formen in Office‑Math‑Objekte konvertiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Gibt an, ob Formen mit EquationXML in Office‑Math‑Objekte konvertiert werden sollen. |

### setDetectHyperlinks(boolean value) {#setDetectHyperlinks-boolean}
```
public void setDetectHyperlinks(boolean value)
```


Gibt an, ob Hyperlinks im Text erkannt werden sollen. Der Standardwert ist false.

 **Examples:** 

Zeigt, wie Hyperlinks gelesen und angezeigt werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setDetectNumberingWithWhitespaces(boolean value) {#setDetectNumberingWithWhitespaces-boolean}
```
public void setDetectNumberingWithWhitespaces(boolean value)
```


Ermöglicht die Angabe, wie nummerierte Listenelemente erkannt werden, wenn das Dokument aus einem Nur-Text-Format importiert wird. Der Standardwert ist true.

 **Remarks:** 

Wenn diese Option auf false gesetzt ist, erkennt der Listenerkennungsalgorithmus Listenkapitel, wenn Listennummern entweder mit einem Punkt, einer rechten Klammer oder Aufzählungszeichen (wie "\\u2022", "\*", "-" oder "o") enden.

Wenn diese Option auf true gesetzt ist, werden Leerzeichen ebenfalls als Trennzeichen für Listennummern verwendet: Der Listenerkennungsalgorithmus für arabische Nummerierung (1., 1.1.2.) nutzt sowohl Leerzeichen als auch Punkt (".")-Symbole.

 **Examples:** 

Zeigt, wie Listen beim Laden von Nur-Text-Dokumenten erkannt werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setDocumentDirection(int value) {#setDocumentDirection-int}
```
public void setDocumentDirection(int value)
```


Legt die Dokumentenrichtung fest. Der Standardwert ist [DocumentDirection.LEFT\_TO\_RIGHT](../../com.aspose.words/documentdirection/\#LEFT-TO-RIGHT).

 **Examples:** 

Zeigt, wie die Textflussrichtung eines Klartextdokuments erkannt wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Eine Dokumentenrichtung. Der Wert muss einer der Konstanten von [DocumentDirection](../../com.aspose.words/documentdirection/) sein. |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset}
```
public void setEncoding(Charset value)
```


Legt die Codierung fest, die zum Laden eines HTML‑, TXT‑ oder CHM‑Dokuments verwendet wird, wenn die Codierung im Dokument nicht angegeben ist. Kann null sein. Standard ist null.

 **Remarks:** 

Diese Eigenschaft wird nur beim Laden von HTML-, TXT- oder CHM-Dokumenten verwendet.

Wenn im Dokument keine Kodierung angegeben ist und diese Eigenschaft  null  ist, versucht das System, die Kodierung automatisch zu erkennen.

 **Examples:** 

Zeigt, wie man die Kodierung festlegt, mit der ein Dokument geöffnet wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.nio.charset.Charset | Die Codierung, die zum Laden eines HTML‑, TXT‑ oder CHM‑Dokuments verwendet wird, wenn die Codierung im Dokument nicht angegeben ist. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Ermöglicht das Festlegen von Dokument‑Schrifteinstellungen.

 **Remarks:** 

Beim Laden einiger Formate kann Aspose.Words das Auflösen der Schriftarten erfordern. Zum Beispiel kann Aspose.Words beim Laden von HTML-Dokumenten die Schriftarten auflösen, um einen Schriftarten‑Fallback durchzuführen.

Wenn auf  null  gesetzt, werden die standardmäßigen statischen Schriftarteinstellungen [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance) verwendet.

Der Standardwert ist  null .

 **Examples:** 

Zeigt, wie man Schriftart‑Ersatz während des Ladens festlegt.

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

Zeigt, wie man Einstellungen für den Schriftart‑Ersatz beim Laden eines Dokuments anwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | Der entsprechende [FontSettings](../../com.aspose.words/fontsettings/) Wert. |

### setIgnoreOleData(boolean value) {#setIgnoreOleData-boolean}
```
public void setIgnoreOleData(boolean value)
```


Gibt an, ob OLE‑Daten ignoriert werden sollen.

 **Remarks:** 

Das Ignorieren von OLE‑Daten kann den Speicherverbrauch reduzieren und die Leistung steigern, ohne dass Daten verloren gehen, wenn das Zielformat OLE‑Objekte nicht unterstützt.

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man OLE‑Daten beim Laden ignoriert.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setLeadingSpacesOptions(int value) {#setLeadingSpacesOptions-int}
```
public void setLeadingSpacesOptions(int value)
```


Legt die bevorzugte Option für die Behandlung von führenden Leerzeichen fest. Der Standardwert ist [TxtLeadingSpacesOptions.CONVERT\_TO\_INDENT](../../com.aspose.words/txtleadingspacesoptions/\#CONVERT-TO-INDENT).

 **Examples:** 

Zeigt, wie Leerzeichen beim Laden von Nur-Text-Dokumenten getrimmt werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Bevorzugte Option für die Behandlung von führenden Leerzeichen. Der Wert muss einer der Konstanten von [TxtLeadingSpacesOptions](../../com.aspose.words/txtleadingspacesoptions/) sein. |

### setLoadFormat(int value) {#setLoadFormat-int}
```
public void setLoadFormat(int value)
```


Gibt das Format des zu ladenden Dokuments an. Standard ist [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO).

 **Remarks:** 

Es wird empfohlen, den Wert [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) anzugeben und Aspose.Words das Dateiformat automatisch erkennen zu lassen. Wenn Sie das Format des zu ladenden Dokuments kennen, können Sie das Format explizit angeben, wodurch die Ladezeit durch den Aufwand für die automatische Erkennung leicht reduziert wird. Geben Sie ein explizites Ladeformat an und stellt sich heraus, dass es falsch ist, wird die automatische Erkennung aufgerufen und ein zweiter Versuch, die Datei zu laden, unternommen.

 **Examples:** 

Zeigt, wie man eine Basis‑URI beim Öffnen eines HTML‑Dokuments angibt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der [LoadFormat](../../com.aspose.words/loadformat/)‑Konstanten sein. |

### setMswVersion(int value) {#setMswVersion-int}
```
public void setMswVersion(int value)
```


Ermöglicht die Angabe, dass der Dokument‑Ladevorgang einer bestimmten MS‑Word‑Version entsprechen soll. Standardwert ist [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019)

 **Remarks:** 

Verschiedene Word‑Versionen können bestimmte Aspekte des Dokumentinhalts und der Formatierung während des Ladevorgangs leicht unterschiedlich handhaben, was zu geringfügigen Unterschieden im Document Object Model führen kann.

 **Examples:** 

Zeigt, wie man den Ladevorgang einer bestimmten Microsoft‑Word‑Version beim Dokumentenladen emuliert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der [MsWordVersion](../../com.aspose.words/mswordversion/)‑Konstanten sein. |

### setPassword(String value) {#setPassword-java.lang.String}
```
public void setPassword(String value)
```


Legt das Passwort zum Öffnen eines verschlüsselten Dokuments fest. Kann null oder ein leerer String sein. Standard ist null.

 **Remarks:** 

Sie müssen das Passwort kennen, um ein verschlüsseltes Dokument zu öffnen. Ist das Dokument nicht verschlüsselt, setzen Sie dies auf  null  oder einen leeren String.

 **Examples:** 

Zeigt, wie man eine verschlüsselte Dokumentdatei signiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Das Passwort zum Öffnen eines verschlüsselten Dokuments. |

### setPreserveIncludePictureField(boolean value) {#setPreserveIncludePictureField-boolean}
```
public void setPreserveIncludePictureField(boolean value)
```


Legt fest, ob das INCLUDEPICTURE‑Feld beim Lesen von Microsoft‑Word‑Formaten erhalten bleiben soll. Der Standardwert ist false.

 **Remarks:** 

Standardmäßig wird das INCLUDEPICTURE-Feld in ein Formobjekt konvertiert. Sie können dies überschreiben, wenn Sie das Feld beibehalten müssen, zum Beispiel, wenn Sie es programmgesteuert aktualisieren möchten. Beachten Sie jedoch, dass dieser Ansatz bei Aspose.Words nicht üblich ist. Verwenden Sie ihn auf eigenes Risiko.

Ein möglicher Anwendungsfall könnte die Verwendung eines MERGEFIELD als untergeordnetes Feld sein, um den Quellpfad des Bildes dynamisch zu ändern. In diesem Fall muss das INCLUDEPICTURE im Modell beibehalten werden.

 **Examples:** 

Zeigt, wie man INCLUDEPICTURE‑Felder beim Laden eines Dokuments beibehält oder verwirft.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ob das INCLUDEPICTURE‑Feld beim Lesen von Microsoft‑Word‑Formaten erhalten bleiben soll. |

### setProgressCallback(IDocumentLoadingCallback value) {#setProgressCallback-com.aspose.words.IDocumentLoadingCallback}
```
public void setProgressCallback(IDocumentLoadingCallback value)
```


Wird beim Laden eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

Zeigt, wie der Benutzer benachrichtigt wird, wenn das Laden des Dokuments die erwartete Ladezeit überschreitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) | Der entsprechende [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/)-Wert. |

### setRecoveryMode(int value) {#setRecoveryMode-int}
```
public void setRecoveryMode(int value)
```


Definiert, wie das Dokument behandelt werden soll, wenn beim Laden Fehler auftreten. Verwenden Sie diese Eigenschaft, um anzugeben, ob das System versuchen soll, das Dokument wiederherzustellen oder ein anderes definiertes Verhalten zu folgen. Der Standardwert ist [DocumentRecoveryMode.TRY\_RECOVER](../../com.aspose.words/documentrecoverymode/\#TRY-RECOVER).

 **Examples:** 

Zeigt, wie versucht wird, ein Dokument wiederherzustellen, wenn beim Laden Fehler aufgetreten sind.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/)‑Konstanten sein. |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML oder MHTML importiert wird.

 **Examples:** 

Zeigt, wie externe Ressourcen beim Laden von HTML-Dokumenten behandelt werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) | Der entsprechende [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/)-Wert. |

### setTempFolder(String value) {#setTempFolder-java.lang.String}
```
public void setTempFolder(String value)
```


Ermöglicht die Verwendung temporärer Dateien beim Lesen des Dokuments. Standardmäßig ist diese Eigenschaft null und es werden keine temporären Dateien verwendet.

 **Remarks:** 

Der Ordner muss existieren und beschreibbar sein, andernfalls wird eine Ausnahme ausgelöst.

Aspose.Words löscht automatisch alle temporären Dateien, wenn das Lesen abgeschlossen ist.

 **Examples:** 

Zeigt, wie ein Dokument mit temporären Dateien geladen wird.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

Zeigt, wie beim Laden eines Dokuments die Festplatte anstelle des Speichers verwendet wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setTrailingSpacesOptions(int value) {#setTrailingSpacesOptions-int}
```
public void setTrailingSpacesOptions(int value)
```


Legt die bevorzugte Option für die Behandlung von nachgestellten Leerzeichen fest. Der Standardwert ist [TxtTrailingSpacesOptions.TRIM](../../com.aspose.words/txttrailingspacesoptions/\#TRIM).

 **Examples:** 

Zeigt, wie Leerzeichen beim Laden von Nur-Text-Dokumenten getrimmt werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Bevorzugte Option für die Behandlung von nachgestellten Leerzeichen. Der Wert muss einer der Konstanten von [TxtTrailingSpacesOptions](../../com.aspose.words/txttrailingspacesoptions/) sein. |

### setUpdateDirtyFields(boolean value) {#setUpdateDirtyFields-boolean}
```
public void setUpdateDirtyFields(boolean value)
```


Gibt an, ob die Felder mit dem  dirty  Attribut aktualisiert werden sollen.

 **Examples:** 

Zeigt, wie man die spezielle Eigenschaft zum Aktualisieren des Feldergebnisses verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setUseSystemLcid(boolean value) {#setUseSystemLcid-boolean}
```
public void setUseSystemLcid(boolean value)
```


Legt fest, ob der aus der Windows-Registrierung erhaltene LCID-Wert verwendet wird, um die Standardränder der Seiteneinrichtung zu bestimmen.

 **Remarks:** 

Wenn auf true gesetzt, wird das Verhalten von MS Word emuliert, das den LCID‑Wert aus der Windows‑Registrierung übernimmt.

Der Standardwert ist  false .

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ob der aus der Windows-Registrierung erhaltene LCID-Wert verwendet werden soll, um die Standardränder der Seiteneinrichtung zu bestimmen. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu Daten- oder Formatierungsverlust führen könnte.

 **Examples:** 

Zeigt, wie Warnungen, die beim Laden eines Dokuments auftreten, ausgegeben und gespeichert werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Der entsprechende [IWarningCallback](../../com.aspose.words/iwarningcallback/) Wert. |

