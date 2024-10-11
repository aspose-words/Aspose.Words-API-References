---
title: TxtLoadOptions
linktitle: TxtLoadOptions
second_title: Aspose.Words for Java
description: Allows to specify additional options when loading LoadFormat.TEXT document into a Document object in Java.
type: docs
weight: 646
url: /java/com.aspose.words/txtloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions/)
```
public class TxtLoadOptions extends LoadOptions
```

Allows to specify additional options when loading [LoadFormat.TEXT](../../com.aspose.words/loadformat/\#TEXT) document into a [Document](../../com.aspose.words/document/) object.

To learn more, visit the [ Specify Load Options ][Specify Load Options] documentation article.

 **Examples:** 

Shows how to read and display hyperlinks.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [TxtLoadOptions()](#TxtLoadOptions) | Initializes a new instance of this class with default values. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Determines whether the specified object is equal in value to the current object. |
| [getAutoNumberingDetection()](#getAutoNumberingDetection) | Gets a boolean value indicating either automatic numbering detection will be performed while loading a document. |
| [getBaseUri()](#getBaseUri) | Gets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng) | Gets whether to convert metafile( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) images to **F:Aspose.FileFormat.Png** image format. |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath) | Gets whether to convert shapes with EquationXML to Office Math objects. |
| [getDetectHyperlinks()](#getDetectHyperlinks) | Specifies either to detect hyperlinks in text. |
| [getDetectNumberingWithWhitespaces()](#getDetectNumberingWithWhitespaces) | Allows to specify how numbered list items are recognized when document is imported from plain text format. |
| [getDocumentDirection()](#getDocumentDirection) | Gets a document direction. |
| [getEncoding()](#getEncoding) | Gets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. |
| [getFontSettings()](#getFontSettings) | Allows to specify document font settings. |
| [getIgnoreOleData()](#getIgnoreOleData) | Specifies whether to ignore the OLE data. |
| [getLanguagePreferences()](#getLanguagePreferences) | Gets language preferences that will be used when document is loading. |
| [getLeadingSpacesOptions()](#getLeadingSpacesOptions) | Gets preferred option of a leading space handling. |
| [getLoadFormat()](#getLoadFormat) | Specifies the format of the document to be loaded. |
| [getMswVersion()](#getMswVersion) | Allows to specify that the document loading process should match a specific MS Word version. |
| [getPassword()](#getPassword) | Gets the password for opening an encrypted document. |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField) | Gets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. |
| [getProgressCallback()](#getProgressCallback) | Called during loading a document and accepts data about loading progress. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [getTempFolder()](#getTempFolder) | Allows to use temporary files when reading document. |
| [getTrailingSpacesOptions()](#getTrailingSpacesOptions) | Gets preferred option of a trailing space handling. |
| [getUpdateDirtyFields()](#getUpdateDirtyFields) | Specifies whether to update the fields with the  dirty  attribute. |
| [getUseSystemLcid()](#getUseSystemLcid) | Gets whether to use LCID value obtained from Windows registry to determine page setup default margins. |
| [getWarningCallback()](#getWarningCallback) | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |
| [setAutoNumberingDetection(boolean value)](#setAutoNumberingDetection-boolean) | Sets a boolean value indicating either automatic numbering detection will be performed while loading a document. |
| [setBaseUri(String value)](#setBaseUri-java.lang.String) | Sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean) | Sets whether to convert metafile( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) images to **F:Aspose.FileFormat.Png** image format. |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean) | Sets whether to convert shapes with EquationXML to Office Math objects. |
| [setDetectHyperlinks(boolean value)](#setDetectHyperlinks-boolean) | Specifies either to detect hyperlinks in text. |
| [setDetectNumberingWithWhitespaces(boolean value)](#setDetectNumberingWithWhitespaces-boolean) | Allows to specify how numbered list items are recognized when document is imported from plain text format. |
| [setDocumentDirection(int value)](#setDocumentDirection-int) | Sets a document direction. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) | Sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Allows to specify document font settings. |
| [setIgnoreOleData(boolean value)](#setIgnoreOleData-boolean) | Specifies whether to ignore the OLE data. |
| [setLeadingSpacesOptions(int value)](#setLeadingSpacesOptions-int) | Sets preferred option of a leading space handling. |
| [setLoadFormat(int value)](#setLoadFormat-int) | Specifies the format of the document to be loaded. |
| [setMswVersion(int value)](#setMswVersion-int) | Allows to specify that the document loading process should match a specific MS Word version. |
| [setPassword(String value)](#setPassword-java.lang.String) | Sets the password for opening an encrypted document. |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean) | Sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback) | Called during loading a document and accepts data about loading progress. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback) | Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Allows to use temporary files when reading document. |
| [setTrailingSpacesOptions(int value)](#setTrailingSpacesOptions-int) | Sets preferred option of a trailing space handling. |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean) | Specifies whether to update the fields with the  dirty  attribute. |
| [setUseSystemLcid(boolean value)](#setUseSystemLcid-boolean) | Sets whether to use LCID value obtained from Windows registry to determine page setup default margins. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss. |
### TxtLoadOptions() {#TxtLoadOptions}
```
public TxtLoadOptions()
```


Initializes a new instance of this class with default values.

 **Examples:** 

Shows how to read and display hyperlinks.

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


Determines whether the specified object is equal in value to the current object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getAutoNumberingDetection() {#getAutoNumberingDetection}
```
public boolean getAutoNumberingDetection()
```


Gets a boolean value indicating either automatic numbering detection will be performed while loading a document. The default value is  true .

 **Examples:** 

Shows how to disable automatic numbering detection.

```

 TxtLoadOptions options = new TxtLoadOptions(); { options.setAutoNumberingDetection(false); }
 Document doc = new Document(getMyDir() + "Number detection.txt", options);
 
```

**Returns:**
boolean - A boolean value indicating either automatic numbering detection will be performed while loading a document.
### getBaseUri() {#getBaseUri}
```
public String getBaseUri()
```


Gets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be  null  or empty string. Default is  null .

 **Remarks:** 

This property is used to resolve relative URIs into absolute in the following cases:

1.  When loading an HTML document from a stream and the document contains images with relative URIs and does not have a base URI specified in the BASE HTML element.
2.  When saving a document to PDF and other formats, to retrieve images linked using relative URIs so the images can be saved into the output document.

 **Examples:** 

Shows how to open an HTML document with images from a stream using a base URI.

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
java.lang.String - The string that will be used to resolve relative URIs found in the document into absolute URIs when required.
### getConvertMetafilesToPng() {#getConvertMetafilesToPng}
```
public boolean getConvertMetafilesToPng()
```


Gets whether to convert metafile( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) images to **F:Aspose.FileFormat.Png** image format.

 **Remarks:** 

Metafiles ( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) is an uncompressed image format and sometimes requires to much RAM to hold and process document. This option allows to convert all metafile images to **F:Aspose.FileFormat.Png** on document loading. Please note - conversion vector graphics to raster decreases quality of the images.

 **Examples:** 

Shows how to convert WMF/EMF to PNG during loading document.

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
boolean - Whether to convert metafile( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) images to **F:Aspose.FileFormat.Png** image format.
### getConvertShapeToOfficeMath() {#getConvertShapeToOfficeMath}
```
public boolean getConvertShapeToOfficeMath()
```


Gets whether to convert shapes with EquationXML to Office Math objects.

 **Examples:** 

Shows how to convert EquationXML shapes to Office Math objects.

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
boolean - Whether to convert shapes with EquationXML to Office Math objects.
### getDetectHyperlinks() {#getDetectHyperlinks}
```
public boolean getDetectHyperlinks()
```


Specifies either to detect hyperlinks in text. The default value is  false .

 **Examples:** 

Shows how to read and display hyperlinks.

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
boolean - The corresponding  boolean  value.
### getDetectNumberingWithWhitespaces() {#getDetectNumberingWithWhitespaces}
```
public boolean getDetectNumberingWithWhitespaces()
```


Allows to specify how numbered list items are recognized when document is imported from plain text format. The default value is  true .

 **Remarks:** 

If this option is set to  false , lists recognition algorithm detects list paragraphs, when list numbers ends with either dot, right bracket or bullet symbols (such as "\\u2022", "\*", "-" or "o").

If this option is set to  true , whitespaces are also used as list number delimiters: list recognition algorithm for Arabic style numbering (1., 1.1.2.) uses both whitespaces and dot (".") symbols.

 **Examples:** 

Shows how to detect lists when loading plaintext documents.

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
boolean - The corresponding  boolean  value.
### getDocumentDirection() {#getDocumentDirection}
```
public int getDocumentDirection()
```


Gets a document direction. The default value is [DocumentDirection.LEFT\_TO\_RIGHT](../../com.aspose.words/documentdirection/\#LEFT-TO-RIGHT).

 **Examples:** 

Shows how to detect plaintext document text direction.

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
int - A document direction. The returned value is one of [DocumentDirection](../../com.aspose.words/documentdirection/) constants.
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


Gets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be  null . Default is  null .

 **Remarks:** 

This property is used only when loading HTML, TXT, or CHM documents.

If encoding is not specified inside the document and this property is  null , then the system will try to automatically detect the encoding.

 **Examples:** 

Shows how to set the encoding with which to open a document.

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
java.nio.charset.Charset - The encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Allows to specify document font settings.

 **Remarks:** 

When loading some formats, Aspose.Words may require to resolve the fonts. For example, when loading HTML documents Aspose.Words may resolve the fonts to perform font fallback.

If set to  null , default static font settings [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance) will be used.

The default value is  null .

 **Examples:** 

Shows how to apply font substitution settings while loading a document.

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

Shows how to designate font substitutes during loading.

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

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value.
### getIgnoreOleData() {#getIgnoreOleData}
```
public boolean getIgnoreOleData()
```


Specifies whether to ignore the OLE data.

 **Remarks:** 

Ignoring OLE data may reduce memory consumption and increase performance without data lost in a case when destination format does not support OLE objects.

The default value is  false .

 **Examples:** 

Shows how to ingore OLE data while loading.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getLanguagePreferences() {#getLanguagePreferences}
```
public LanguagePreferences getLanguagePreferences()
```


Gets language preferences that will be used when document is loading.

 **Examples:** 

Shows how to apply language preferences when loading a document.

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


Gets preferred option of a leading space handling. Default value is [TxtLeadingSpacesOptions.CONVERT\_TO\_INDENT](../../com.aspose.words/txtleadingspacesoptions/\#CONVERT-TO-INDENT).

 **Examples:** 

Shows how to trim whitespace when loading plaintext documents.

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
int - Preferred option of a leading space handling. The returned value is one of [TxtLeadingSpacesOptions](../../com.aspose.words/txtleadingspacesoptions/) constants.
### getLoadFormat() {#getLoadFormat}
```
public int getLoadFormat()
```


Specifies the format of the document to be loaded. Default is [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO).

 **Remarks:** 

It is recommended that you specify the [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) value and let Aspose.Words detect the file format automatically. If you know the format of the document you are about to load, you can specify the format explicitly and this will slightly reduce the loading time by the overhead associated with auto detecting the format. If you specify an explicit load format and it will turn out to be wrong, the auto detection will be invoked and a second attempt to load the file will be made.

 **Examples:** 

Shows how to specify a base URI when opening an html document.

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
int - The corresponding  int  value. The returned value is one of [LoadFormat](../../com.aspose.words/loadformat/) constants.
### getMswVersion() {#getMswVersion}
```
public int getMswVersion()
```


Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019)

 **Remarks:** 

Different Word versions may handle certain aspects of document content and formatting slightly differently during the loading process, which may result in minor differences in Document Object Model.

 **Examples:** 

Shows how to emulate the loading procedure of a specific Microsoft Word version during document loading.

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
int - The corresponding  int  value. The returned value is one of [MsWordVersion](../../com.aspose.words/mswordversion/) constants.
### getPassword() {#getPassword}
```
public String getPassword()
```


Gets the password for opening an encrypted document. Can be  null  or empty string. Default is  null .

 **Remarks:** 

You need to know the password to open an encrypted document. If the document is not encrypted, set this to  null  or empty string.

 **Examples:** 

Shows how to sign encrypted document file.

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
java.lang.String - The password for opening an encrypted document.
### getPreserveIncludePictureField() {#getPreserveIncludePictureField}
```
public boolean getPreserveIncludePictureField()
```


Gets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is  false .

 **Remarks:** 

By default, the INCLUDEPICTURE field is converted into a shape object. You can override that if you need the field to be preserved, for example, if you wish to update it programmatically. Note however that this approach is not common for Aspose.Words. Use it on your own risk.

One of the possible use cases may be using a MERGEFIELD as a child field to dynamically change the source path of the picture. In this case you need the INCLUDEPICTURE to be preserved in the model.

 **Examples:** 

Shows how to preserve or discard INCLUDEPICTURE fields when loading a document.

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
boolean - Whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats.
### getProgressCallback() {#getProgressCallback}
```
public IDocumentLoadingCallback getProgressCallback()
```


Called during loading a document and accepts data about loading progress.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

Shows how to notify the user if document loading exceeded expected loading time.

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
### getResourceLoadingCallback() {#getResourceLoadingCallback}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.

 **Examples:** 

Shows how to handle external resources when loading Html documents.

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


Allows to use temporary files when reading document. By default this property is  null  and no temporary files are used.

 **Remarks:** 

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when reading is complete.

 **Examples:** 

Shows how to load a document using temporary files.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

Shows how to use the hard drive instead of memory when loading a document.

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
java.lang.String - The corresponding java.lang.String value.
### getTrailingSpacesOptions() {#getTrailingSpacesOptions}
```
public int getTrailingSpacesOptions()
```


Gets preferred option of a trailing space handling. Default value is [TxtTrailingSpacesOptions.TRIM](../../com.aspose.words/txttrailingspacesoptions/\#TRIM).

 **Examples:** 

Shows how to trim whitespace when loading plaintext documents.

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
int - Preferred option of a trailing space handling. The returned value is one of [TxtTrailingSpacesOptions](../../com.aspose.words/txttrailingspacesoptions/) constants.
### getUpdateDirtyFields() {#getUpdateDirtyFields}
```
public boolean getUpdateDirtyFields()
```


Specifies whether to update the fields with the  dirty  attribute.

 **Examples:** 

Shows how to use special property for updating field result.

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
boolean - The corresponding  boolean  value.
### getUseSystemLcid() {#getUseSystemLcid}
```
public boolean getUseSystemLcid()
```


Gets whether to use LCID value obtained from Windows registry to determine page setup default margins.

 **Remarks:** 

If set to  true , then MS Word behavior is emulated which takes LCID value from Windows registry.

The default value is  false .

**Returns:**
boolean - Whether to use LCID value obtained from Windows registry to determine page setup default margins.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss.

 **Examples:** 

Shows how to print and store warnings that occur during document loading.

```

 public void loadOptionsWarningCallback() throws Exception {
     // Create a new LoadOptions object and set its WarningCallback attribute
     // as an instance of our IWarningCallback implementation.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setWarningCallback(new DocumentLoadingWarningCallback());

     // Our callback will print all warnings that come up during the load operation.
     Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

     ArrayList warnings = ((DocumentLoadingWarningCallback) loadOptions.getWarningCallback()).getWarnings();
     Assert.assertEquals(3, warnings.size());
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


Sets a boolean value indicating either automatic numbering detection will be performed while loading a document. The default value is  true .

 **Examples:** 

Shows how to disable automatic numbering detection.

```

 TxtLoadOptions options = new TxtLoadOptions(); { options.setAutoNumberingDetection(false); }
 Document doc = new Document(getMyDir() + "Number detection.txt", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating either automatic numbering detection will be performed while loading a document. |

### setBaseUri(String value) {#setBaseUri-java.lang.String}
```
public void setBaseUri(String value)
```


Sets the string that will be used to resolve relative URIs found in the document into absolute URIs when required. Can be  null  or empty string. Default is  null .

 **Remarks:** 

This property is used to resolve relative URIs into absolute in the following cases:

1.  When loading an HTML document from a stream and the document contains images with relative URIs and does not have a base URI specified in the BASE HTML element.
2.  When saving a document to PDF and other formats, to retrieve images linked using relative URIs so the images can be saved into the output document.

 **Examples:** 

Shows how to open an HTML document with images from a stream using a base URI.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The string that will be used to resolve relative URIs found in the document into absolute URIs when required. |

### setConvertMetafilesToPng(boolean value) {#setConvertMetafilesToPng-boolean}
```
public void setConvertMetafilesToPng(boolean value)
```


Sets whether to convert metafile( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) images to **F:Aspose.FileFormat.Png** image format.

 **Remarks:** 

Metafiles ( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) is an uncompressed image format and sometimes requires to much RAM to hold and process document. This option allows to convert all metafile images to **F:Aspose.FileFormat.Png** on document loading. Please note - conversion vector graphics to raster decreases quality of the images.

 **Examples:** 

Shows how to convert WMF/EMF to PNG during loading document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to convert metafile( **F:Aspose.FileFormat.Wmf** or **F:Aspose.FileFormat.Emf**) images to **F:Aspose.FileFormat.Png** image format. |

### setConvertShapeToOfficeMath(boolean value) {#setConvertShapeToOfficeMath-boolean}
```
public void setConvertShapeToOfficeMath(boolean value)
```


Sets whether to convert shapes with EquationXML to Office Math objects.

 **Examples:** 

Shows how to convert EquationXML shapes to Office Math objects.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to convert shapes with EquationXML to Office Math objects. |

### setDetectHyperlinks(boolean value) {#setDetectHyperlinks-boolean}
```
public void setDetectHyperlinks(boolean value)
```


Specifies either to detect hyperlinks in text. The default value is  false .

 **Examples:** 

Shows how to read and display hyperlinks.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setDetectNumberingWithWhitespaces(boolean value) {#setDetectNumberingWithWhitespaces-boolean}
```
public void setDetectNumberingWithWhitespaces(boolean value)
```


Allows to specify how numbered list items are recognized when document is imported from plain text format. The default value is  true .

 **Remarks:** 

If this option is set to  false , lists recognition algorithm detects list paragraphs, when list numbers ends with either dot, right bracket or bullet symbols (such as "\\u2022", "\*", "-" or "o").

If this option is set to  true , whitespaces are also used as list number delimiters: list recognition algorithm for Arabic style numbering (1., 1.1.2.) uses both whitespaces and dot (".") symbols.

 **Examples:** 

Shows how to detect lists when loading plaintext documents.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setDocumentDirection(int value) {#setDocumentDirection-int}
```
public void setDocumentDirection(int value)
```


Sets a document direction. The default value is [DocumentDirection.LEFT\_TO\_RIGHT](../../com.aspose.words/documentdirection/\#LEFT-TO-RIGHT).

 **Examples:** 

Shows how to detect plaintext document text direction.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A document direction. The value must be one of [DocumentDirection](../../com.aspose.words/documentdirection/) constants. |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset}
```
public void setEncoding(Charset value)
```


Sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. Can be  null . Default is  null .

 **Remarks:** 

This property is used only when loading HTML, TXT, or CHM documents.

If encoding is not specified inside the document and this property is  null , then the system will try to automatically detect the encoding.

 **Examples:** 

Shows how to set the encoding with which to open a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.nio.charset.Charset | The encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Allows to specify document font settings.

 **Remarks:** 

When loading some formats, Aspose.Words may require to resolve the fonts. For example, when loading HTML documents Aspose.Words may resolve the fonts to perform font fallback.

If set to  null , default static font settings [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance) will be used.

The default value is  null .

 **Examples:** 

Shows how to apply font substitution settings while loading a document.

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

Shows how to designate font substitutes during loading.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | The corresponding [FontSettings](../../com.aspose.words/fontsettings/) value. |

### setIgnoreOleData(boolean value) {#setIgnoreOleData-boolean}
```
public void setIgnoreOleData(boolean value)
```


Specifies whether to ignore the OLE data.

 **Remarks:** 

Ignoring OLE data may reduce memory consumption and increase performance without data lost in a case when destination format does not support OLE objects.

The default value is  false .

 **Examples:** 

Shows how to ingore OLE data while loading.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setLeadingSpacesOptions(int value) {#setLeadingSpacesOptions-int}
```
public void setLeadingSpacesOptions(int value)
```


Sets preferred option of a leading space handling. Default value is [TxtLeadingSpacesOptions.CONVERT\_TO\_INDENT](../../com.aspose.words/txtleadingspacesoptions/\#CONVERT-TO-INDENT).

 **Examples:** 

Shows how to trim whitespace when loading plaintext documents.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Preferred option of a leading space handling. The value must be one of [TxtLeadingSpacesOptions](../../com.aspose.words/txtleadingspacesoptions/) constants. |

### setLoadFormat(int value) {#setLoadFormat-int}
```
public void setLoadFormat(int value)
```


Specifies the format of the document to be loaded. Default is [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO).

 **Remarks:** 

It is recommended that you specify the [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) value and let Aspose.Words detect the file format automatically. If you know the format of the document you are about to load, you can specify the format explicitly and this will slightly reduce the loading time by the overhead associated with auto detecting the format. If you specify an explicit load format and it will turn out to be wrong, the auto detection will be invoked and a second attempt to load the file will be made.

 **Examples:** 

Shows how to specify a base URI when opening an html document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [LoadFormat](../../com.aspose.words/loadformat/) constants. |

### setMswVersion(int value) {#setMswVersion-int}
```
public void setMswVersion(int value)
```


Allows to specify that the document loading process should match a specific MS Word version. Default value is [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019)

 **Remarks:** 

Different Word versions may handle certain aspects of document content and formatting slightly differently during the loading process, which may result in minor differences in Document Object Model.

 **Examples:** 

Shows how to emulate the loading procedure of a specific Microsoft Word version during document loading.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [MsWordVersion](../../com.aspose.words/mswordversion/) constants. |

### setPassword(String value) {#setPassword-java.lang.String}
```
public void setPassword(String value)
```


Sets the password for opening an encrypted document. Can be  null  or empty string. Default is  null .

 **Remarks:** 

You need to know the password to open an encrypted document. If the document is not encrypted, set this to  null  or empty string.

 **Examples:** 

Shows how to sign encrypted document file.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The password for opening an encrypted document. |

### setPreserveIncludePictureField(boolean value) {#setPreserveIncludePictureField-boolean}
```
public void setPreserveIncludePictureField(boolean value)
```


Sets whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. The default value is  false .

 **Remarks:** 

By default, the INCLUDEPICTURE field is converted into a shape object. You can override that if you need the field to be preserved, for example, if you wish to update it programmatically. Note however that this approach is not common for Aspose.Words. Use it on your own risk.

One of the possible use cases may be using a MERGEFIELD as a child field to dynamically change the source path of the picture. In this case you need the INCLUDEPICTURE to be preserved in the model.

 **Examples:** 

Shows how to preserve or discard INCLUDEPICTURE fields when loading a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to preserve the INCLUDEPICTURE field when reading Microsoft Word formats. |

### setProgressCallback(IDocumentLoadingCallback value) {#setProgressCallback-com.aspose.words.IDocumentLoadingCallback}
```
public void setProgressCallback(IDocumentLoadingCallback value)
```


Called during loading a document and accepts data about loading progress.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

Shows how to notify the user if document loading exceeded expected loading time.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) | The corresponding [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) value. |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.

 **Examples:** 

Shows how to handle external resources when loading Html documents.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) | The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) value. |

### setTempFolder(String value) {#setTempFolder-java.lang.String}
```
public void setTempFolder(String value)
```


Allows to use temporary files when reading document. By default this property is  null  and no temporary files are used.

 **Remarks:** 

The folder must exist and be writable, otherwise an exception will be thrown.

Aspose.Words automatically deletes all temporary files when reading is complete.

 **Examples:** 

Shows how to load a document using temporary files.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

Shows how to use the hard drive instead of memory when loading a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setTrailingSpacesOptions(int value) {#setTrailingSpacesOptions-int}
```
public void setTrailingSpacesOptions(int value)
```


Sets preferred option of a trailing space handling. Default value is [TxtTrailingSpacesOptions.TRIM](../../com.aspose.words/txttrailingspacesoptions/\#TRIM).

 **Examples:** 

Shows how to trim whitespace when loading plaintext documents.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Preferred option of a trailing space handling. The value must be one of [TxtTrailingSpacesOptions](../../com.aspose.words/txttrailingspacesoptions/) constants. |

### setUpdateDirtyFields(boolean value) {#setUpdateDirtyFields-boolean}
```
public void setUpdateDirtyFields(boolean value)
```


Specifies whether to update the fields with the  dirty  attribute.

 **Examples:** 

Shows how to use special property for updating field result.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setUseSystemLcid(boolean value) {#setUseSystemLcid-boolean}
```
public void setUseSystemLcid(boolean value)
```


Sets whether to use LCID value obtained from Windows registry to determine page setup default margins.

 **Remarks:** 

If set to  true , then MS Word behavior is emulated which takes LCID value from Windows registry.

The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Whether to use LCID value obtained from Windows registry to determine page setup default margins. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss.

 **Examples:** 

Shows how to print and store warnings that occur during document loading.

```

 public void loadOptionsWarningCallback() throws Exception {
     // Create a new LoadOptions object and set its WarningCallback attribute
     // as an instance of our IWarningCallback implementation.
     LoadOptions loadOptions = new LoadOptions();
     loadOptions.setWarningCallback(new DocumentLoadingWarningCallback());

     // Our callback will print all warnings that come up during the load operation.
     Document doc = new Document(getMyDir() + "Document.docx", loadOptions);

     ArrayList warnings = ((DocumentLoadingWarningCallback) loadOptions.getWarningCallback()).getWarnings();
     Assert.assertEquals(3, warnings.size());
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
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value. |

