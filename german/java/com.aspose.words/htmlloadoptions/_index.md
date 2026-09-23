---
title: "HtmlLoadOptions"
linktitle: "HtmlLoadOptions"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Angeben zusätzlicher Optionen beim Laden eines HTML-Dokuments in ein Document-Objekt in Java."
type: docs
weight: 382
url: /de/java/com.aspose.words/htmlloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions/)
```
public class HtmlLoadOptions extends LoadOptions
```

Ermöglicht das Angeben zusätzlicher Optionen beim Laden eines HTML-Dokuments in ein [Document](../../com.aspose.words/document/) Objekt.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Specify Load Options ][Specify Load Options].

 **Examples:** 

Zeigt, wie bedingte Kommentare beim Laden eines HTML-Dokuments unterstützt werden können.

```

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();

 // If the value is true, then we take VML code into account while parsing the loaded document.
 loadOptions.setSupportVml(supportVml);

 // This document contains a JPEG image within "
```


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [HtmlLoadOptions()](#HtmlLoadOptions) | Initialisiert eine neue Instanz dieser Klasse mit Standardwerten. |
| [HtmlLoadOptions(String password)](#HtmlLoadOptions-java.lang.String) | Eine Abkürzung, um eine neue Instanz dieser Klasse mit dem angegebenen Passwort zum Laden eines verschlüsselten Dokuments zu initialisieren. |
| [HtmlLoadOptions(int loadFormat, String password, String baseUri)](#HtmlLoadOptions-int-java.lang.String-java.lang.String) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| [getBaseUri()](#getBaseUri) | Gibt die Zeichenkette zurück, die verwendet wird, um relative URIs im Dokument bei Bedarf in absolute URIs aufzulösen. |
| [getBlockImportMode()](#getBlockImportMode) | Gibt einen Wert zurück, der festlegt, wie Eigenschaften von Block‑Elementen importiert werden. |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng) | Gibt an, ob Metadateien (**F:Aspose.FileFormat.Wmf** oder **F:Aspose.FileFormat.Emf**) in das Bildformat **F:Aspose.FileFormat.Png** konvertiert werden sollen. |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath) | Gibt an, ob Formen mit EquationXML in Office‑Math‑Objekte konvertiert werden sollen. |
| [getConvertSvgToEmf()](#getConvertSvgToEmf) | Gibt einen Wert zurück, der angibt, ob geladene SVG‑Bilder in das EMF‑Format konvertiert werden sollen. |
| [getEncoding()](#getEncoding) | Gibt die Kodierung zurück, die zum Laden eines HTML-, TXT‑ oder CHM‑Dokuments verwendet wird, wenn die Kodierung im Dokument nicht angegeben ist. |
| [getFontSettings()](#getFontSettings) | Ermöglicht das Festlegen von Dokument‑Schrifteinstellungen. |
| [getIgnoreNoscriptElements()](#getIgnoreNoscriptElements) | Gibt einen Wert zurück, der angibt, ob HTML‑Elemente ignoriert werden sollen. |
| [getIgnoreOleData()](#getIgnoreOleData) | Gibt an, ob OLE‑Daten ignoriert werden sollen. |
| [getLanguagePreferences()](#getLanguagePreferences) | Gibt die Spracheinstellungen zurück, die beim Laden des Dokuments verwendet werden. |
| [getLoadFormat()](#getLoadFormat) | Gibt das Format des zu ladenden Dokuments an. |
| [getMswVersion()](#getMswVersion) | Ermöglicht die Angabe, dass der Dokument‑Ladevorgang einer bestimmten MS‑Word‑Version entsprechen soll. |
| [getPassword()](#getPassword) | Gibt das Passwort zum Öffnen eines verschlüsselten Dokuments zurück. |
| [getPreferredControlType()](#getPreferredControlType) | Gibt den bevorzugten Typ von Dokumentknoten zurück, die importierte  und  Elemente darstellen. |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField) | Gibt an, ob das INCLUDEPICTURE‑Feld beim Lesen von Microsoft‑Word‑Formaten beibehalten werden soll. |
| [getProgressCallback()](#getProgressCallback) | Wird beim Laden eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt. |
| [getRecoveryMode()](#getRecoveryMode) | Definiert, wie das Dokument behandelt werden soll, wenn beim Laden Fehler auftreten. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback) | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML oder MHTML importiert wird. |
| [getSupportFontFaceRules()](#getSupportFontFaceRules) | Gibt einen Wert zurück, der angibt, ob @font-face‑Regeln unterstützt und deklarierte Schriften geladen werden sollen. |
| [getSupportVml()](#getSupportVml) | Gibt einen Wert zurück, der angibt, ob VML-Bilder unterstützt werden. |
| [getTempFolder()](#getTempFolder) | Ermöglicht die Verwendung temporärer Dateien beim Lesen des Dokuments. |
| [getUpdateDirtyFields()](#getUpdateDirtyFields) | Gibt an, ob die Felder mit dem  dirty  Attribut aktualisiert werden sollen. |
| [getUseSystemLcid()](#getUseSystemLcid) | Gibt an, ob der aus der Windows-Registrierung erhaltene LCID-Wert verwendet wird, um die Standardränder der Seiteneinrichtung zu bestimmen. |
| [getWarningCallback()](#getWarningCallback) | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu Daten- oder Formatierungsverlust führen könnte. |
| [getWebRequestTimeout()](#getWebRequestTimeout) | Die Anzahl der Millisekunden, die gewartet werden soll, bevor die Webanfrage abläuft. |
| [setBaseUri(String value)](#setBaseUri-java.lang.String) | Legt die Zeichenkette fest, die verwendet wird, um relative URIs im Dokument bei Bedarf in absolute URIs aufzulösen. |
| [setBlockImportMode(int value)](#setBlockImportMode-int) | Legt einen Wert fest, der angibt, wie Eigenschaften von Block-Elementen importiert werden. |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean) | Legt fest, ob Metadateien ( **F:Aspose.FileFormat.Wmf** oder **F:Aspose.FileFormat.Emf**) in das Bildformat **F:Aspose.FileFormat.Png** konvertiert werden. |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean) | Legt fest, ob Formen mit EquationXML in Office Math-Objekte konvertiert werden. |
| [setConvertSvgToEmf(boolean value)](#setConvertSvgToEmf-boolean) | Legt einen Wert fest, der angibt, ob geladene SVG-Bilder in das EMF-Format konvertiert werden. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) | Legt die Kodierung fest, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, wenn die Kodierung im Dokument nicht angegeben ist. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Ermöglicht das Festlegen von Dokument‑Schrifteinstellungen. |
| [setIgnoreNoscriptElements(boolean value)](#setIgnoreNoscriptElements-boolean) | Legt einen Wert fest, der angibt, ob  HTML-Elemente ignoriert werden sollen. |
| [setIgnoreOleData(boolean value)](#setIgnoreOleData-boolean) | Gibt an, ob OLE‑Daten ignoriert werden sollen. |
| [setLoadFormat(int value)](#setLoadFormat-int) | Gibt das Format des zu ladenden Dokuments an. |
| [setMswVersion(int value)](#setMswVersion-int) | Ermöglicht die Angabe, dass der Dokument‑Ladevorgang einer bestimmten MS‑Word‑Version entsprechen soll. |
| [setPassword(String value)](#setPassword-java.lang.String) | Legt das Passwort zum Öffnen eines verschlüsselten Dokuments fest. |
| [setPreferredControlType(int value)](#setPreferredControlType-int) | Legt den bevorzugten Typ von Dokumentknoten fest, die importierte  und  Elemente darstellen. |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean) | Legt fest, ob das INCLUDEPICTURE-Feld beim Lesen von Microsoft-Word-Formaten erhalten bleibt. |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback) | Wird beim Laden eines Dokuments aufgerufen und akzeptiert Daten zum Ladefortschritt. |
| [setRecoveryMode(int value)](#setRecoveryMode-int) | Definiert, wie das Dokument behandelt werden soll, wenn beim Laden Fehler auftreten. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback) | Ermöglicht die Steuerung, wie externe Ressourcen (Bilder, Stylesheets) geladen werden, wenn ein Dokument aus HTML oder MHTML importiert wird. |
| [setSupportFontFaceRules(boolean value)](#setSupportFontFaceRules-boolean) | Legt einen Wert fest, der angibt, ob @font-face-Regeln unterstützt und deklarierte Schriftarten geladen werden. |
| [setSupportVml(boolean value)](#setSupportVml-boolean) | Legt einen Wert fest, der angibt, ob VML-Bilder unterstützt werden. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Ermöglicht die Verwendung temporärer Dateien beim Lesen des Dokuments. |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean) | Gibt an, ob die Felder mit dem  dirty  Attribut aktualisiert werden sollen. |
| [setUseSystemLcid(boolean value)](#setUseSystemLcid-boolean) | Legt fest, ob der aus der Windows-Registrierung erhaltene LCID-Wert verwendet wird, um die Standardränder der Seiteneinrichtung zu bestimmen. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu Daten- oder Formatierungsverlust führen könnte. |
| [setWebRequestTimeout(int value)](#setWebRequestTimeout-int) | Die Anzahl der Millisekunden, die gewartet werden soll, bevor die Webanfrage abläuft. |
### HtmlLoadOptions() {#HtmlLoadOptions}
```
public HtmlLoadOptions()
```


Initialisiert eine neue Instanz dieser Klasse mit Standardwerten.

 **Examples:** 

Zeigt, wie bedingte Kommentare beim Laden eines HTML-Dokuments unterstützt werden können.

```

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();

 // If the value is true, then we take VML code into account while parsing the loaded document.
 loadOptions.setSupportVml(supportVml);

 // This document contains a JPEG image within "
```

### HtmlLoadOptions(String password) {#HtmlLoadOptions-java.lang.String}
```
public HtmlLoadOptions(String password)
```


Eine Abkürzung, um eine neue Instanz dieser Klasse mit dem angegebenen Passwort zum Laden eines verschlüsselten Dokuments zu initialisieren.

 **Examples:** 

Zeigt, wie ein HTML-Dokument verschlüsselt und anschließend mit einem Passwort geöffnet wird.

```

 // Create and sign an encrypted HTML document from an encrypted .docx.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw");

 SignOptions signOptions = new SignOptions();
 {
     signOptions.setComments("Comment");
     signOptions.setSignTime(new Date());
     signOptions.setDecryptionPassword("docPassword");
 }

 String inputFileName = getMyDir() + "Encrypted.docx";
 String outputFileName = getArtifactsDir() + "HtmlLoadOptions.EncryptedHtml.html";
 DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);

 // To load and read this document, we will need to pass its decryption
 // password using a HtmlLoadOptions object.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions("docPassword");
 Assert.assertEquals(loadOptions.getPassword(), signOptions.getDecryptionPassword());

 Document doc = new Document(outputFileName, loadOptions);
 Assert.assertEquals(doc.getText().trim(), "Test encrypted document.");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Passwort | java.lang.String | Das Passwort zum Öffnen eines verschlüsselten Dokuments. Kann  null  oder ein leerer String sein. |

### HtmlLoadOptions(int loadFormat, String password, String baseUri) {#HtmlLoadOptions-int-java.lang.String-java.lang.String}
```
public HtmlLoadOptions(int loadFormat, String password, String baseUri)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| loadFormat | int |  |
| Passwort | java.lang.String |  |
| baseUri | java.lang.String |  |

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
### getBlockImportMode() {#getBlockImportMode}
```
public int getBlockImportMode()
```


Gibt einen Wert zurück, der angibt, wie Eigenschaften von Block-Elementen importiert werden. Standardwert ist [BlockImportMode.MERGE](../../com.aspose.words/blockimportmode/\#MERGE).

 **Examples:** 

Zeigt, wie Eigenschaften von Block‑Elementen aus HTML‑basierten Dokumenten importiert werden.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```

**Returns:**
int - Ein Wert, der angibt, wie Eigenschaften von Block-Elementen importiert werden. Der zurückgegebene Wert ist einer der Konstanten von [BlockImportMode](../../com.aspose.words/blockimportmode/).
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
### getConvertSvgToEmf() {#getConvertSvgToEmf}
```
public boolean getConvertSvgToEmf()
```


Gibt einen Wert zurück, der angibt, ob geladene SVG‑Bilder in das EMF‑Format konvertiert werden sollen. Standardwert ist  false  und, wenn möglich, werden geladene SVG‑Bilder unverändert ohne Konvertierung gespeichert.

 **Remarks:** 

Neuere Versionen von MS Word unterstützen SVG‑Bilder nativ. Wenn die in den Ladeoptionen angegebene MS‑Word‑Version SVG unterstützt, speichert Aspose.Words SVG‑Bilder unverändert ohne Konvertierung. Wenn SVG nicht unterstützt wird, werden geladene SVG‑Bilder in das EMF‑Format konvertiert.

Wenn diese Option jedoch auf  true  gesetzt ist, konvertiert Aspose.Words geladene SVG‑Bilder in EMF, selbst wenn SVG‑Bilder von der angegebenen MS‑Word‑Version unterstützt werden.

 **Examples:** 

Zeigt, wie SVG-Objekte beim Speichern von HTML-Dokumenten in ein anderes Format konvertiert werden.

```

 String html =
     "\n                    \n                        Hello world!\n                    \n                ";

 // Use 'ConvertSvgToEmf' to turn back the legacy behavior
 // where all SVG images loaded from an HTML document were converted to EMF.
 // Now SVG images are loaded without conversion
 // if the MS Word version specified in load options supports SVG images natively.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions(); { loadOptions.setConvertSvgToEmf(true); }

 Document doc = new Document(new ByteArrayInputStream(html.getBytes()));

 // This document contains a  element in the form of text.
 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine how the saving operation handles this object.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.Png" to convert it to a PNG image.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.Svg" preserve it as a SVG object.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.EmfOrWmf" to convert it to a metafile.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setMetafileFormat(htmlMetafileFormat);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.MetafileFormat.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.MetafileFormat.html"), StandardCharsets.UTF_8);

 switch (htmlMetafileFormat) {
     case HtmlMetafileFormat.PNG:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         ""));
         break;
     case HtmlMetafileFormat.SVG:
         Assert.assertTrue(outDocContents.contains(
                 "" +
                         ""));
         break;
     case HtmlMetafileFormat.EMF_OR_WMF:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         ""));
         break;
 }
 
```

**Returns:**
boolean - Ein Wert, der angibt, ob geladene SVG‑Bilder in das EMF‑Format konvertiert werden sollen.
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
### getIgnoreNoscriptElements() {#getIgnoreNoscriptElements}
```
public boolean getIgnoreNoscriptElements()
```


Gibt einen Wert zurück, der angibt, ob  HTML‑Elemente ignoriert werden sollen. Standardwert ist  false .

 **Remarks:** 

Wie MS Word unterstützt Aspose.Words keine Skripte und lädt standardmäßig den Inhalt von  Elementen in das resultierende Dokument. In den meisten Browsern werden Skripte jedoch unterstützt und der Inhalt von  ist nicht sichtbar. Wird diese Eigenschaft auf  true  gesetzt, zwingt das Aspose.Words, alle  Elemente zu ignorieren und hilft, Dokumente zu erzeugen, die dem in Browsern gesehenen Ergebnis näher kommen.

 **Examples:** 

Zeigt, wie man  HTML‑Elemente ignoriert.

```

 final String html = "\r\n\r\n\r\nNOSCRIPT\r\n\r\n\r\n\r\n\r\n Your browser does not support JavaScript!\r\n\r\n";

 HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
 htmlLoadOptions.setIgnoreNoscriptElements(ignoreNoscriptElements);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), htmlLoadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.IgnoreNoscriptElements.pdf");
 
```

**Returns:**
boolean - Ein Wert, der angibt, ob  HTML‑Elemente ignoriert werden sollen.
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
### getPreferredControlType() {#getPreferredControlType}
```
public int getPreferredControlType()
```


Ermittelt den bevorzugten Typ von Dokumentknoten, die importierte  und  Elemente darstellen. Standardwert ist [HtmlControlType.FORM\_FIELD](../../com.aspose.words/htmlcontroltype/\#FORM-FIELD). Hinweis: Bitte beachten Sie, dass das Festlegen dieser Eigenschaft nicht garantiert, dass alle importierten Steuerelemente vom angegebenen Typ sind. Wenn ein HTML‑Steuerelement nicht mit Dokumentknoten des bevorzugten Typs darstellbar ist, verwendet Aspose.Words einen kompatiblen [HtmlControlType](../../com.aspose.words/htmlcontroltype/) für dieses Steuerelement. Beispiele: Zeigt, wie der bevorzugte Typ von Dokumentknoten festgelegt wird, die importierte  und  Elemente darstellen.   final String html = "\\r\\n\\r\\n\\r\\n" + "item1\\r\\n\\r\\n\\r\\n\\r\\n"; HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions(); htmlLoadOptions.setPreferredControlType(HtmlControlType.STRUCTURED\_DOCUMENT\_TAG); Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF\_8)), htmlLoadOptions); NodeCollection nodes = doc.getChildNodes(NodeType.STRUCTURED\_DOCUMENT\_TAG, true); StructuredDocumentTag tag = (StructuredDocumentTag) nodes.get(0);

**Returns:**
int - Bevorzugter Typ von Dokumentknoten, die importierte  und  Elemente darstellen. Der zurückgegebene Wert ist einer der Konstanten von [HtmlControlType](../../com.aspose.words/htmlcontroltype/).
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
### getSupportFontFaceRules() {#getSupportFontFaceRules}
```
public boolean getSupportFontFaceRules()
```


Ermittelt einen Wert, der angibt, ob @font-face-Regeln unterstützt werden und ob deklarierte Schriftarten geladen werden sollen. Der Standardwert ist  false .

 **Remarks:** 

Wenn diese Option aktiviert ist, werden in @font-face‑Regeln deklarierte Schriftarten geladen und in die Schriftartdefinitionen des resultierenden Dokuments eingebettet (siehe [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos)). Dadurch stehen die geladenen Schriftarten für das Rendern zur Verfügung, jedoch wird das Einbetten der Schriftarten beim Speichern nicht automatisch aktiviert. Um das Dokument mit geladenen Schriftarten zu speichern, muss die Eigenschaft [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) der [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos)-Sammlung auf true gesetzt.

Unterstützte Schriftformate sind TTF, EOT und WOFF.

**Returns:**
boolean – Ein Wert, der angibt, ob @font-face‑Regeln unterstützt werden und ob deklarierte Schriftarten geladen werden.
### getSupportVml() {#getSupportVml}
```
public boolean getSupportVml()
```


Gibt einen Wert zurück, der angibt, ob VML-Bilder unterstützt werden.

 **Examples:** 

Zeigt, wie bedingte Kommentare beim Laden eines HTML-Dokuments unterstützt werden können.

```

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();

 // If the value is true, then we take VML code into account while parsing the loaded document.
 loadOptions.setSupportVml(supportVml);

 // This document contains a JPEG image within "
```

**Returns:**
boolean – Ein Wert, der angibt, ob VML‑Bilder unterstützt werden.
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
### getWebRequestTimeout() {#getWebRequestTimeout}
```
public int getWebRequestTimeout()
```


Die Anzahl der Millisekunden, die gewartet wird, bevor die Web‑Anfrage abläuft. Der Standardwert beträgt 100 000 Millisekunden (100 Sekunden).

 **Remarks:** 

Die Anzahl der Millisekunden, die Aspose.Words auf eine Antwort wartet, wenn externe Ressourcen (Bilder, Stylesheets) in HTML‑ und MHTML‑Dokumenten geladen werden.

**Returns:**
int - Der entsprechende int-Wert.
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

### setBlockImportMode(int value) {#setBlockImportMode-int}
```
public void setBlockImportMode(int value)
```


Legt einen Wert fest, der angibt, wie Eigenschaften von Block‑Elementen importiert werden. Der Standardwert ist [BlockImportMode.MERGE](../../com.aspose.words/blockimportmode/\#MERGE).

 **Examples:** 

Zeigt, wie Eigenschaften von Block‑Elementen aus HTML‑basierten Dokumenten importiert werden.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Ein Wert, der angibt, wie Eigenschaften von Block‑Elementen importiert werden. Der Wert muss einer der Konstanten von [BlockImportMode](../../com.aspose.words/blockimportmode/) sein. |

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

### setConvertSvgToEmf(boolean value) {#setConvertSvgToEmf-boolean}
```
public void setConvertSvgToEmf(boolean value)
```


Legt einen Wert fest, der angibt, ob geladene SVG‑Bilder in das EMF‑Format konvertiert werden. Der Standardwert ist false und, wenn möglich, werden geladene SVG‑Bilder unverändert ohne Konvertierung gespeichert.

 **Remarks:** 

Neuere Versionen von MS Word unterstützen SVG‑Bilder nativ. Wenn die in den Ladeoptionen angegebene MS‑Word‑Version SVG unterstützt, speichert Aspose.Words SVG‑Bilder unverändert ohne Konvertierung. Wenn SVG nicht unterstützt wird, werden geladene SVG‑Bilder in das EMF‑Format konvertiert.

Wenn diese Option jedoch auf  true  gesetzt ist, konvertiert Aspose.Words geladene SVG‑Bilder in EMF, selbst wenn SVG‑Bilder von der angegebenen MS‑Word‑Version unterstützt werden.

 **Examples:** 

Zeigt, wie SVG-Objekte beim Speichern von HTML-Dokumenten in ein anderes Format konvertiert werden.

```

 String html =
     "\n                    \n                        Hello world!\n                    \n                ";

 // Use 'ConvertSvgToEmf' to turn back the legacy behavior
 // where all SVG images loaded from an HTML document were converted to EMF.
 // Now SVG images are loaded without conversion
 // if the MS Word version specified in load options supports SVG images natively.
 HtmlLoadOptions loadOptions = new HtmlLoadOptions(); { loadOptions.setConvertSvgToEmf(true); }

 Document doc = new Document(new ByteArrayInputStream(html.getBytes()));

 // This document contains a  element in the form of text.
 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine how the saving operation handles this object.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.Png" to convert it to a PNG image.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.Svg" preserve it as a SVG object.
 // Setting the "MetafileFormat" property to "HtmlMetafileFormat.EmfOrWmf" to convert it to a metafile.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setMetafileFormat(htmlMetafileFormat);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.MetafileFormat.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.MetafileFormat.html"), StandardCharsets.UTF_8);

 switch (htmlMetafileFormat) {
     case HtmlMetafileFormat.PNG:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         ""));
         break;
     case HtmlMetafileFormat.SVG:
         Assert.assertTrue(outDocContents.contains(
                 "" +
                         ""));
         break;
     case HtmlMetafileFormat.EMF_OR_WMF:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         ""));
         break;
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der angibt, ob geladene SVG‑Bilder in das EMF‑Format konvertiert werden sollen. |

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

### setIgnoreNoscriptElements(boolean value) {#setIgnoreNoscriptElements-boolean}
```
public void setIgnoreNoscriptElements(boolean value)
```


Legt einen Wert fest, der angibt, ob HTML‑Elemente ignoriert werden sollen. Standardwert ist false.

 **Remarks:** 

Wie MS Word unterstützt Aspose.Words keine Skripte und lädt standardmäßig den Inhalt von  Elementen in das resultierende Dokument. In den meisten Browsern werden Skripte jedoch unterstützt und der Inhalt von  ist nicht sichtbar. Wird diese Eigenschaft auf  true  gesetzt, zwingt das Aspose.Words, alle  Elemente zu ignorieren und hilft, Dokumente zu erzeugen, die dem in Browsern gesehenen Ergebnis näher kommen.

 **Examples:** 

Zeigt, wie man  HTML‑Elemente ignoriert.

```

 final String html = "\r\n\r\n\r\nNOSCRIPT\r\n\r\n\r\n\r\n\r\n Your browser does not support JavaScript!\r\n\r\n";

 HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
 htmlLoadOptions.setIgnoreNoscriptElements(ignoreNoscriptElements);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), htmlLoadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.IgnoreNoscriptElements.pdf");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der angibt, ob HTML‑Elemente ignoriert werden sollen. |

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

### setPreferredControlType(int value) {#setPreferredControlType-int}
```
public void setPreferredControlType(int value)
```


Legt den bevorzugten Typ von Dokumentknoten fest, die importierte  und  Elemente darstellen. Standardwert ist [HtmlControlType.FORM\_FIELD](../../com.aspose.words/htmlcontroltype/\#FORM-FIELD). Hinweise: Bitte beachten Sie, dass das Festlegen dieser Eigenschaft nicht garantiert, dass alle importierten Steuerelemente vom angegebenen Typ sind. Wenn ein HTML‑Steuerelement nicht mit Dokumentknoten des bevorzugten Typs darstellbar ist, verwendet Aspose.Words einen kompatiblen [HtmlControlType](../../com.aspose.words/htmlcontroltype/) für dieses Steuerelement. Beispiele: Zeigt, wie der bevorzugte Typ von Dokumentknoten festgelegt wird, die importierte  und  Elemente darstellen.   final String html = "\\r\\n\\r\\n\\r\\n" + "item1\\r\\n\\r\\n\\r\\n\\r\\n"; HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions(); htmlLoadOptions.setPreferredControlType(HtmlControlType.STRUCTURED\_DOCUMENT\_TAG); Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF\_8)), htmlLoadOptions); NodeCollection nodes = doc.getChildNodes(NodeType.STRUCTURED\_DOCUMENT\_TAG, true); StructuredDocumentTag tag = (StructuredDocumentTag) nodes.get(0);

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Bevorzugter Typ von Dokumentknoten, die importierte  und  Elemente darstellen. Der Wert muss einer der [HtmlControlType](../../com.aspose.words/htmlcontroltype/)‑Konstanten sein. |

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

### setSupportFontFaceRules(boolean value) {#setSupportFontFaceRules-boolean}
```
public void setSupportFontFaceRules(boolean value)
```


Legt einen Wert fest, der angibt, ob @font-face‑Regeln unterstützt und deklarierte Schriften geladen werden sollen. Standardwert ist false.

 **Remarks:** 

Wenn diese Option aktiviert ist, werden in @font-face‑Regeln deklarierte Schriftarten geladen und in die Schriftartdefinitionen des resultierenden Dokuments eingebettet (siehe [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos)). Dadurch stehen die geladenen Schriftarten für das Rendern zur Verfügung, jedoch wird das Einbetten der Schriftarten beim Speichern nicht automatisch aktiviert. Um das Dokument mit geladenen Schriftarten zu speichern, muss die Eigenschaft [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) der [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos)-Sammlung auf true gesetzt.

Unterstützte Schriftformate sind TTF, EOT und WOFF.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der angibt, ob @font-face‑Regeln unterstützt und deklarierte Schriften geladen werden sollen. |

### setSupportVml(boolean value) {#setSupportVml-boolean}
```
public void setSupportVml(boolean value)
```


Legt einen Wert fest, der angibt, ob VML-Bilder unterstützt werden.

 **Examples:** 

Zeigt, wie bedingte Kommentare beim Laden eines HTML-Dokuments unterstützt werden können.

```

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();

 // If the value is true, then we take VML code into account while parsing the loaded document.
 loadOptions.setSupportVml(supportVml);

 // This document contains a JPEG image within "
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Wert, der angibt, ob VML‑Bilder unterstützt werden. |

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

### setWebRequestTimeout(int value) {#setWebRequestTimeout-int}
```
public void setWebRequestTimeout(int value)
```


Die Anzahl der Millisekunden, die gewartet wird, bevor die Web‑Anfrage abläuft. Der Standardwert beträgt 100 000 Millisekunden (100 Sekunden).

 **Remarks:** 

Die Anzahl der Millisekunden, die Aspose.Words auf eine Antwort wartet, wenn externe Ressourcen (Bilder, Stylesheets) in HTML‑ und MHTML‑Dokumenten geladen werden.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

