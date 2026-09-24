---
title: "MarkdownLoadOptions"
linktitle: "MarkdownLoadOptions"
second_title: "Aspose.Words para Java"
description: "Permite especificar opciones adicionales al cargar un documento LoadFormat.MARKDOWN en un objeto Document en Java."
type: docs
weight: 454
url: /es/java/com.aspose.words/markdownloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions/)
```
public class MarkdownLoadOptions extends LoadOptions
```

Permite especificar opciones adicionales al cargar un documento [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN) en un objeto [Document](../../com.aspose.words/document/).

 **Examples:** 

Muestra cómo conservar una línea vacía al cargar un documento.

```

 String mdText = MessageFormat.format("{0}Line1{0}{0}Line2{0}{0}", System.lineSeparator());

 MarkdownLoadOptions loadOptions = new MarkdownLoadOptions();
 loadOptions.setPreserveEmptyLines(true);
 Document doc = new Document(new ByteArrayInputStream(mdText.getBytes()), loadOptions);

 Assert.assertEquals("\rLine1\r\rLine2\r\f", doc.getText());
 
```
## Constructores

| Constructor | Descripción |
| --- | --- |
| [MarkdownLoadOptions()](#MarkdownLoadOptions) | Inicializa una nueva instancia de la clase [MarkdownLoadOptions](../../com.aspose.words/markdownloadoptions/). |
## Métodos

| Método | Descripción |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Determina si el objeto especificado es igual en valor al objeto actual. |
| [getBaseUri()](#getBaseUri) | Obtiene la cadena que se usará para resolver URIs relativos encontrados en el documento en URIs absolutos cuando sea necesario. |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng) | Obtiene si convertir imágenes de metarchivo ( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) al formato de imagen **F:Aspose.FileFormat.Png**. |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath) | Obtiene si convertir formas con EquationXML a objetos Office Math. |
| [getEncoding()](#getEncoding) | Obtiene la codificación que se usará para cargar un documento HTML, TXT o CHM si la codificación no está especificada dentro del documento. |
| [getFontSettings()](#getFontSettings) | Permite especificar la configuración de fuentes del documento. |
| [getIgnoreOleData()](#getIgnoreOleData) | Especifica si ignorar los datos OLE. |
| [getImportUnderlineFormatting()](#getImportUnderlineFormatting) | Obtiene un valor booleano que indica si reconocer una secuencia de dos caracteres más "++" como formato de subrayado de texto. |
| [getLanguagePreferences()](#getLanguagePreferences) | Obtiene las preferencias de idioma que se usarán cuando se cargue el documento. |
| [getLoadFormat()](#getLoadFormat) | Especifica el formato del documento que se cargará. |
| [getMswVersion()](#getMswVersion) | Permite especificar que el proceso de carga del documento coincida con una versión específica de MS Word. |
| [getPassword()](#getPassword) | Obtiene la contraseña para abrir un documento cifrado. |
| [getPreserveEmptyLines()](#getPreserveEmptyLines) | Obtiene un valor booleano que indica si conservar líneas vacías al cargar un documento [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN). |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField) | Obtiene si preservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. |
| [getProgressCallback()](#getProgressCallback) | Se llama durante la carga de un documento y acepta datos sobre el progreso de la carga. |
| [getRecoveryMode()](#getRecoveryMode) | Define cómo debe manejarse el documento si se producen errores durante la carga. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback) | Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando un documento se importa desde HTML, MHTML. |
| [getSoftLineBreakCharacter()](#getSoftLineBreakCharacter) | Obtiene un valor de carácter que representa un salto de línea suave. |
| [getTempFolder()](#getTempFolder) | Permite usar archivos temporales al leer el documento. |
| [getUpdateDirtyFields()](#getUpdateDirtyFields) | Especifica si se deben actualizar los campos con el  dirty  atributo. |
| [getUseSystemLcid()](#getUseSystemLcid) | Obtiene si se debe usar el valor LCID obtenido del registro de Windows para determinar los márgenes predeterminados de la configuración de página. |
| [getWarningCallback()](#getWarningCallback) | Se llama durante una operación de carga, cuando se detecta un problema que podría resultar en pérdida de datos o de fidelidad de formato. |
| [setBaseUri(String value)](#setBaseUri-java.lang.String) | Establece la cadena que se usará para resolver URIs relativos encontrados en el documento en URIs absolutos cuando sea necesario. |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean) | Establece si se convierten imágenes metafile( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) al formato de imagen **F:Aspose.FileFormat.Png**. |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean) | Establece si se convierten formas con EquationXML a objetos de Office Math. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) | Establece la codificación que se usará para cargar un documento HTML, TXT o CHM si la codificación no está especificada dentro del documento. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Permite especificar la configuración de fuentes del documento. |
| [setIgnoreOleData(boolean value)](#setIgnoreOleData-boolean) | Especifica si ignorar los datos OLE. |
| [setImportUnderlineFormatting(boolean value)](#setImportUnderlineFormatting-boolean) | Establece un valor booleano que indica si reconocer una secuencia de dos caracteres más "++" como formato de subrayado de texto. |
| [setLoadFormat(int value)](#setLoadFormat-int) | Especifica el formato del documento que se cargará. |
| [setMswVersion(int value)](#setMswVersion-int) | Permite especificar que el proceso de carga del documento coincida con una versión específica de MS Word. |
| [setPassword(String value)](#setPassword-java.lang.String) | Establece la contraseña para abrir un documento cifrado. |
| [setPreserveEmptyLines(boolean value)](#setPreserveEmptyLines-boolean) | Establece un valor booleano que indica si conservar líneas vacías al cargar un documento [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN). |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean) | Establece si se debe preservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback) | Se llama durante la carga de un documento y acepta datos sobre el progreso de la carga. |
| [setRecoveryMode(int value)](#setRecoveryMode-int) | Define cómo debe manejarse el documento si se producen errores durante la carga. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback) | Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando un documento se importa desde HTML, MHTML. |
| [setSoftLineBreakCharacter(char value)](#setSoftLineBreakCharacter-char) | Establece un valor de carácter que representa un salto de línea suave. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Permite usar archivos temporales al leer el documento. |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean) | Especifica si se deben actualizar los campos con el  dirty  atributo. |
| [setUseSystemLcid(boolean value)](#setUseSystemLcid-boolean) | Establece si se debe usar el valor LCID obtenido del registro de Windows para determinar los márgenes predeterminados de la configuración de página. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Se llama durante una operación de carga, cuando se detecta un problema que podría resultar en pérdida de datos o de fidelidad de formato. |
### MarkdownLoadOptions() {#MarkdownLoadOptions}
```
public MarkdownLoadOptions()
```


Inicializa una nueva instancia de la clase [MarkdownLoadOptions](../../com.aspose.words/markdownloadoptions/).

 **Remarks:** 

Establece automáticamente [LoadFormat](../../com.aspose.words/loadformat/) a [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN).

 **Examples:** 

Muestra cómo conservar una línea vacía al cargar un documento.

```

 String mdText = MessageFormat.format("{0}Line1{0}{0}Line2{0}{0}", System.lineSeparator());

 MarkdownLoadOptions loadOptions = new MarkdownLoadOptions();
 loadOptions.setPreserveEmptyLines(true);
 Document doc = new Document(new ByteArrayInputStream(mdText.getBytes()), loadOptions);

 Assert.assertEquals("\rLine1\r\rLine2\r\f", doc.getText());
 
```

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determina si el objeto especificado es igual en valor al objeto actual.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getBaseUri() {#getBaseUri}
```
public String getBaseUri()
```


Obtiene la cadena que se utilizará para resolver URIs relativos encontrados en el documento en URIs absolutos cuando sea necesario. Puede ser  null  o una cadena vacía. El valor predeterminado es  null .

 **Remarks:** 

Esta propiedad se utiliza para resolver URIs relativos en absolutos en los siguientes casos:

1.  Al cargar un documento HTML desde un flujo y el documento contiene imágenes con URIs relativos y no tiene un URI base especificado en el elemento BASE del HTML.
2.  Al guardar un documento en PDF y otros formatos, para recuperar imágenes vinculadas mediante URIs relativos de modo que las imágenes puedan guardarse en el documento de salida.

 **Examples:** 

Muestra cómo abrir un documento HTML con imágenes desde un flujo utilizando un URI base.

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
java.lang.String - La cadena que se utilizará para resolver URIs relativos encontrados en el documento en URIs absolutos cuando sea necesario.
### getConvertMetafilesToPng() {#getConvertMetafilesToPng}
```
public boolean getConvertMetafilesToPng()
```


Obtiene si convertir imágenes de metarchivo ( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) al formato de imagen **F:Aspose.FileFormat.Png**.

 **Remarks:** 

Los Metafiles ( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) son un formato de imagen sin compresión y a veces requieren demasiada RAM para mantener y procesar el documento. Esta opción permite convertir todas las imágenes de metafile a **F:Aspose.FileFormat.Png** al cargar el documento. Tenga en cuenta: la conversión de gráficos vectoriales a raster disminuye la calidad de las imágenes.

 **Examples:** 

Muestra cómo convertir WMF/EMF a PNG durante la carga del documento.

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
boolean - Indica si se convierten las imágenes de metafile ( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) al formato de imagen **F:Aspose.FileFormat.Png**.
### getConvertShapeToOfficeMath() {#getConvertShapeToOfficeMath}
```
public boolean getConvertShapeToOfficeMath()
```


Obtiene si convertir formas con EquationXML a objetos Office Math.

 **Examples:** 

Muestra cómo convertir formas EquationXML a objetos Office Math.

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
boolean - Indica si se convierten las formas con EquationXML a objetos Office Math.
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


Obtiene la codificación que se utilizará para cargar un documento HTML, TXT o CHM si la codificación no está especificada dentro del documento. Puede ser  null . El valor predeterminado es  null .

 **Remarks:** 

Esta propiedad se usa solo al cargar documentos HTML, TXT o CHM.

Si la codificación no está especificada dentro del documento y esta propiedad es  null , el sistema intentará detectar automáticamente la codificación.

 **Examples:** 

Muestra cómo establecer la codificación con la que abrir un documento.

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
java.nio.charset.Charset - La codificación que se utilizará para cargar un documento HTML, TXT o CHM si la codificación no está especificada dentro del documento.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Permite especificar la configuración de fuentes del documento.

 **Remarks:** 

Al cargar algunos formatos, Aspose.Words puede necesitar resolver las fuentes. Por ejemplo, al cargar documentos HTML Aspose.Words puede resolver las fuentes para realizar la sustitución de fuentes.

Si se establece en  null , se usarán los ajustes de fuente estáticos predeterminados [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance).

El valor predeterminado es  null .

 **Examples:** 

Muestra cómo designar sustitutos de fuentes durante la carga.

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

Muestra cómo aplicar la configuración de sustitución de fuentes al cargar un documento.

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


Especifica si ignorar los datos OLE.

 **Remarks:** 

Ignorar datos OLE puede reducir el consumo de memoria y aumentar el rendimiento sin pérdida de datos en caso de que el formato de destino no admita objetos OLE.

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo ignorar datos OLE al cargar.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Returns:**
boolean - El valor  boolean  correspondiente.
### getImportUnderlineFormatting() {#getImportUnderlineFormatting}
```
public boolean getImportUnderlineFormatting()
```


Obtiene un valor booleano que indica si reconocer una secuencia de dos caracteres más "++" como formato de subrayado de texto. El valor predeterminado es false.

 **Examples:** 

Muestra cómo reconocer los caracteres más "++" como formato de subrayado de texto.

```

 try (ByteArrayInputStream stream = new ByteArrayInputStream("++12 and B++".getBytes(StandardCharsets.US_ASCII)))
 {
     MarkdownLoadOptions loadOptions = new MarkdownLoadOptions(); { loadOptions.setImportUnderlineFormatting(true); }
     Document doc = new Document(stream, loadOptions);

     Paragraph para = (Paragraph)doc.getChild(NodeType.PARAGRAPH, 0, true);
     Assert.assertEquals(Underline.SINGLE, para.getRuns().get(0).getFont().getUnderline());

     loadOptions = new MarkdownLoadOptions(); { loadOptions.setImportUnderlineFormatting(false); }
     doc = new Document(stream, loadOptions);

     para = (Paragraph)doc.getChild(NodeType.PARAGRAPH, 0, true);
     Assert.assertEquals(Underline.NONE, para.getRuns().get(0).getFont().getUnderline());
 }
 
```

**Returns:**
boolean - Un valor booleano que indica si reconocer una secuencia de dos caracteres más "++" como formato de subrayado de texto.
### getLanguagePreferences() {#getLanguagePreferences}
```
public LanguagePreferences getLanguagePreferences()
```


Obtiene las preferencias de idioma que se usarán cuando se cargue el documento.

 **Examples:** 

Muestra cómo aplicar preferencias de idioma al cargar un documento.

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


Especifica el formato del documento que se cargará. El valor predeterminado es [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO).

 **Remarks:** 

Se recomienda que especifique el valor [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) y permita que Aspose.Words detecte el formato del archivo automáticamente. Si conoce el formato del documento que está a punto de cargar, puede especificarlo explícitamente y esto reducirá ligeramente el tiempo de carga al eliminar la sobrecarga asociada con la detección automática del formato. Si especifica un formato de carga explícito y resulta ser incorrecto, se invocará la detección automática y se realizará un segundo intento de cargar el archivo.

 **Examples:** 

Muestra cómo especificar una URI base al abrir un documento html.

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
int - El valor  int  correspondiente. El valor devuelto es una de las constantes de [LoadFormat](../../com.aspose.words/loadformat/).
### getMswVersion() {#getMswVersion}
```
public int getMswVersion()
```


Permite especificar que el proceso de carga del documento coincida con una versión específica de MS Word. El valor predeterminado es [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019)

 **Remarks:** 

Diferentes versiones de Word pueden manejar ciertos aspectos del contenido y formato del documento de manera ligeramente distinta durante el proceso de carga, lo que puede resultar en pequeñas diferencias en el Modelo de Objetos del Documento.

 **Examples:** 

Muestra cómo emular el procedimiento de carga de una versión específica de Microsoft Word durante la carga del documento.

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
int - El valor  int  correspondiente. El valor devuelto es una de las constantes de [MsWordVersion](../../com.aspose.words/mswordversion/).
### getPassword() {#getPassword}
```
public String getPassword()
```


Obtiene la contraseña para abrir un documento cifrado. Puede ser  null  o una cadena vacía. El valor predeterminado es  null .

 **Remarks:** 

Necesita conocer la contraseña para abrir un documento cifrado. Si el documento no está cifrado, establezca esto en  null  o una cadena vacía.

 **Examples:** 

Muestra cómo firmar un archivo de documento cifrado.

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
java.lang.String - La contraseña para abrir un documento cifrado.
### getPreserveEmptyLines() {#getPreserveEmptyLines}
```
public boolean getPreserveEmptyLines()
```


Obtiene un valor booleano que indica si conservar líneas vacías al cargar un documento [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN). El valor predeterminado es false.

Normalmente, las líneas vacías entre elementos de nivel de bloque en Markdown se ignoran. Las líneas vacías al principio y al final del documento también se ignoran. Esta opción permite importar esas líneas vacías.

 **Examples:** 

Muestra cómo conservar una línea vacía al cargar un documento.

```

 String mdText = MessageFormat.format("{0}Line1{0}{0}Line2{0}{0}", System.lineSeparator());

 MarkdownLoadOptions loadOptions = new MarkdownLoadOptions();
 loadOptions.setPreserveEmptyLines(true);
 Document doc = new Document(new ByteArrayInputStream(mdText.getBytes()), loadOptions);

 Assert.assertEquals("\rLine1\r\rLine2\r\f", doc.getText());
 
```

**Returns:**
boolean - Un valor booleano que indica si conservar líneas vacías al cargar un documento [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN).
### getPreserveIncludePictureField() {#getPreserveIncludePictureField}
```
public boolean getPreserveIncludePictureField()
```


Obtiene si se debe preservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. El valor predeterminado es false.

 **Remarks:** 

Por defecto, el campo INCLUDEPICTURE se convierte en un objeto de forma. Puedes sobrescribirlo si necesitas que el campo se preserve, por ejemplo, si deseas actualizarlo programáticamente. Ten en cuenta, sin embargo, que este enfoque no es común para Aspose.Words. Úsalo bajo tu propio riesgo.

Uno de los posibles casos de uso puede ser utilizar un MERGEFIELD como campo hijo para cambiar dinámicamente la ruta de origen de la imagen. En este caso necesitas que el INCLUDEPICTURE se preserve en el modelo.

 **Examples:** 

Muestra cómo conservar o descartar los campos INCLUDEPICTURE al cargar un documento.

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
boolean - Indica si se debe preservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word.
### getProgressCallback() {#getProgressCallback}
```
public IDocumentLoadingCallback getProgressCallback()
```


Se llama durante la carga de un documento y acepta datos sobre el progreso de la carga.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

Muestra cómo notificar al usuario si la carga del documento supera el tiempo de carga esperado.

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


Define cómo debe manejarse el documento si se producen errores durante la carga. Usa esta propiedad para especificar si el sistema debe intentar recuperar el documento o seguir otro comportamiento definido. El valor predeterminado es [DocumentRecoveryMode.TRY\_RECOVER](../../com.aspose.words/documentrecoverymode/\#TRY-RECOVER).

 **Examples:** 

Muestra cómo intentar recuperar un documento si se produjeron errores durante la carga.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Returns:**
int - El valor int correspondiente. El valor devuelto es una de las constantes de [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/).
### getResourceLoadingCallback() {#getResourceLoadingCallback}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando un documento se importa desde HTML, MHTML.

 **Examples:** 

Muestra cómo manejar recursos externos al cargar documentos Html.

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
### getSoftLineBreakCharacter() {#getSoftLineBreakCharacter}
```
public char getSoftLineBreakCharacter()
```


Obtiene un valor de carácter que representa un salto de línea suave. El valor predeterminado es SPACE (U+0020).

 **Remarks:** 

Nota, establecer esta opción a [ControlChar.LINE\_BREAK\_CHAR](../../com.aspose.words/controlchar/\#LINE-BREAK-CHAR) permite cargar saltos de línea suaves como saltos de línea duros.

 **Examples:** 

Muestra cómo establecer el carácter de salto de línea suave.

```

 try (ByteArrayInputStream stream = new ByteArrayInputStream("line1\nline2".getBytes(StandardCharsets.UTF_8)))
 {
     MarkdownLoadOptions loadOptions = new MarkdownLoadOptions();
     loadOptions.setSoftLineBreakCharacter(ControlChar.LINE_BREAK_CHAR);
     Document doc = new Document(stream, loadOptions);

     Assert.assertEquals("line1line2", doc.getText().trim());
 }
 
```

**Returns:**
char - Un valor de carácter que representa un salto de línea suave.
### getTempFolder() {#getTempFolder}
```
public String getTempFolder()
```


Permite usar archivos temporales al leer el documento. Por defecto, esta propiedad es null y no se utilizan archivos temporales.

 **Remarks:** 

La carpeta debe existir y ser escribible, de lo contrario se lanzará una excepción.

Aspose.Words elimina automáticamente todos los archivos temporales cuando la lectura se completa.

 **Examples:** 

Muestra cómo cargar un documento usando archivos temporales.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

Muestra cómo usar el disco duro en lugar de la memoria al cargar un documento.

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
java.lang.String - El valor java.lang.String correspondiente.
### getUpdateDirtyFields() {#getUpdateDirtyFields}
```
public boolean getUpdateDirtyFields()
```


Especifica si se deben actualizar los campos con el  dirty  atributo.

 **Examples:** 

Muestra cómo usar la propiedad especial para actualizar el resultado del campo.

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
boolean - El valor  boolean  correspondiente.
### getUseSystemLcid() {#getUseSystemLcid}
```
public boolean getUseSystemLcid()
```


Obtiene si se debe usar el valor LCID obtenido del registro de Windows para determinar los márgenes predeterminados de la configuración de página.

 **Remarks:** 

Si se establece en true, se emula el comportamiento de MS Word que toma el valor LCID del registro de Windows.

El valor predeterminado es  false .

**Returns:**
boolean - Indica si se debe usar el valor LCID obtenido del registro de Windows para determinar los márgenes predeterminados de la configuración de página.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Se llama durante una operación de carga, cuando se detecta un problema que podría resultar en pérdida de datos o de fidelidad de formato.

 **Examples:** 

Muestra cómo imprimir y almacenar advertencias que ocurren durante la carga del documento.

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
### setBaseUri(String value) {#setBaseUri-java.lang.String}
```
public void setBaseUri(String value)
```


Establece la cadena que se usará para resolver URIs relativos encontrados en el documento a URIs absolutos cuando sea necesario. Puede ser null o una cadena vacía. El valor predeterminado es null.

 **Remarks:** 

Esta propiedad se utiliza para resolver URIs relativos en absolutos en los siguientes casos:

1.  Al cargar un documento HTML desde un flujo y el documento contiene imágenes con URIs relativos y no tiene un URI base especificado en el elemento BASE del HTML.
2.  Al guardar un documento en PDF y otros formatos, para recuperar imágenes vinculadas mediante URIs relativos de modo que las imágenes puedan guardarse en el documento de salida.

 **Examples:** 

Muestra cómo abrir un documento HTML con imágenes desde un flujo utilizando un URI base.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | La cadena que se utilizará para resolver URIs relativos encontrados en el documento en URIs absolutos cuando sea necesario. |

### setConvertMetafilesToPng(boolean value) {#setConvertMetafilesToPng-boolean}
```
public void setConvertMetafilesToPng(boolean value)
```


Establece si se convierten imágenes metafile( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) al formato de imagen **F:Aspose.FileFormat.Png**.

 **Remarks:** 

Los Metafiles ( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) son un formato de imagen sin compresión y a veces requieren demasiada RAM para mantener y procesar el documento. Esta opción permite convertir todas las imágenes de metafile a **F:Aspose.FileFormat.Png** al cargar el documento. Tenga en cuenta: la conversión de gráficos vectoriales a raster disminuye la calidad de las imágenes.

 **Examples:** 

Muestra cómo convertir WMF/EMF a PNG durante la carga del documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Indica si se convierten imágenes de metafile ( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) al formato de imagen **F:Aspose.FileFormat.Png**. |

### setConvertShapeToOfficeMath(boolean value) {#setConvertShapeToOfficeMath-boolean}
```
public void setConvertShapeToOfficeMath(boolean value)
```


Establece si se convierten formas con EquationXML a objetos de Office Math.

 **Examples:** 

Muestra cómo convertir formas EquationXML a objetos Office Math.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Indica si se convierten las formas con EquationXML en objetos Office Math. |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset}
```
public void setEncoding(Charset value)
```


Establece la codificación que se utilizará para cargar un documento HTML, TXT o CHM si la codificación no está especificada dentro del documento. Puede ser  null . El valor predeterminado es  null .

 **Remarks:** 

Esta propiedad se usa solo al cargar documentos HTML, TXT o CHM.

Si la codificación no está especificada dentro del documento y esta propiedad es  null , el sistema intentará detectar automáticamente la codificación.

 **Examples:** 

Muestra cómo establecer la codificación con la que abrir un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.nio.charset.Charset | La codificación que se utilizará para cargar un documento HTML, TXT o CHM si la codificación no está especificada dentro del documento. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Permite especificar la configuración de fuentes del documento.

 **Remarks:** 

Al cargar algunos formatos, Aspose.Words puede necesitar resolver las fuentes. Por ejemplo, al cargar documentos HTML Aspose.Words puede resolver las fuentes para realizar la sustitución de fuentes.

Si se establece en  null , se usarán los ajustes de fuente estáticos predeterminados [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance).

El valor predeterminado es  null .

 **Examples:** 

Muestra cómo designar sustitutos de fuentes durante la carga.

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

Muestra cómo aplicar la configuración de sustitución de fuentes al cargar un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | El valor correspondiente de [FontSettings](../../com.aspose.words/fontsettings/). |

### setIgnoreOleData(boolean value) {#setIgnoreOleData-boolean}
```
public void setIgnoreOleData(boolean value)
```


Especifica si ignorar los datos OLE.

 **Remarks:** 

Ignorar datos OLE puede reducir el consumo de memoria y aumentar el rendimiento sin pérdida de datos en caso de que el formato de destino no admita objetos OLE.

El valor predeterminado es  false .

 **Examples:** 

Muestra cómo ignorar datos OLE al cargar.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setImportUnderlineFormatting(boolean value) {#setImportUnderlineFormatting-boolean}
```
public void setImportUnderlineFormatting(boolean value)
```


Establece un valor booleano que indica si reconocer una secuencia de dos caracteres más "++" como formato de subrayado de texto. El valor predeterminado es false.

 **Examples:** 

Muestra cómo reconocer los caracteres más "++" como formato de subrayado de texto.

```

 try (ByteArrayInputStream stream = new ByteArrayInputStream("++12 and B++".getBytes(StandardCharsets.US_ASCII)))
 {
     MarkdownLoadOptions loadOptions = new MarkdownLoadOptions(); { loadOptions.setImportUnderlineFormatting(true); }
     Document doc = new Document(stream, loadOptions);

     Paragraph para = (Paragraph)doc.getChild(NodeType.PARAGRAPH, 0, true);
     Assert.assertEquals(Underline.SINGLE, para.getRuns().get(0).getFont().getUnderline());

     loadOptions = new MarkdownLoadOptions(); { loadOptions.setImportUnderlineFormatting(false); }
     doc = new Document(stream, loadOptions);

     para = (Paragraph)doc.getChild(NodeType.PARAGRAPH, 0, true);
     Assert.assertEquals(Underline.NONE, para.getRuns().get(0).getFont().getUnderline());
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor booleano que indica si reconocer una secuencia de dos caracteres más "++" como formato de subrayado de texto. |

### setLoadFormat(int value) {#setLoadFormat-int}
```
public void setLoadFormat(int value)
```


Especifica el formato del documento que se cargará. El valor predeterminado es [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO).

 **Remarks:** 

Se recomienda que especifique el valor [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) y permita que Aspose.Words detecte el formato del archivo automáticamente. Si conoce el formato del documento que está a punto de cargar, puede especificarlo explícitamente y esto reducirá ligeramente el tiempo de carga al eliminar la sobrecarga asociada con la detección automática del formato. Si especifica un formato de carga explícito y resulta ser incorrecto, se invocará la detección automática y se realizará un segundo intento de cargar el archivo.

 **Examples:** 

Muestra cómo especificar una URI base al abrir un documento html.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [LoadFormat](../../com.aspose.words/loadformat/). |

### setMswVersion(int value) {#setMswVersion-int}
```
public void setMswVersion(int value)
```


Permite especificar que el proceso de carga del documento coincida con una versión específica de MS Word. El valor predeterminado es [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019)

 **Remarks:** 

Diferentes versiones de Word pueden manejar ciertos aspectos del contenido y formato del documento de manera ligeramente distinta durante el proceso de carga, lo que puede resultar en pequeñas diferencias en el Modelo de Objetos del Documento.

 **Examples:** 

Muestra cómo emular el procedimiento de carga de una versión específica de Microsoft Word durante la carga del documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [MsWordVersion](../../com.aspose.words/mswordversion/). |

### setPassword(String value) {#setPassword-java.lang.String}
```
public void setPassword(String value)
```


Establece la contraseña para abrir un documento cifrado. Puede ser  null  o una cadena vacía. El valor predeterminado es  null .

 **Remarks:** 

Necesita conocer la contraseña para abrir un documento cifrado. Si el documento no está cifrado, establezca esto en  null  o una cadena vacía.

 **Examples:** 

Muestra cómo firmar un archivo de documento cifrado.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | La contraseña para abrir un documento cifrado. |

### setPreserveEmptyLines(boolean value) {#setPreserveEmptyLines-boolean}
```
public void setPreserveEmptyLines(boolean value)
```


Establece un valor booleano que indica si conservar líneas vacías al cargar un documento [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN). El valor predeterminado es false.

Normalmente, las líneas vacías entre elementos de nivel de bloque en Markdown se ignoran. Las líneas vacías al principio y al final del documento también se ignoran. Esta opción permite importar esas líneas vacías.

 **Examples:** 

Muestra cómo conservar una línea vacía al cargar un documento.

```

 String mdText = MessageFormat.format("{0}Line1{0}{0}Line2{0}{0}", System.lineSeparator());

 MarkdownLoadOptions loadOptions = new MarkdownLoadOptions();
 loadOptions.setPreserveEmptyLines(true);
 Document doc = new Document(new ByteArrayInputStream(mdText.getBytes()), loadOptions);

 Assert.assertEquals("\rLine1\r\rLine2\r\f", doc.getText());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | boolean | Un valor booleano que indica si conservar líneas vacías al cargar un documento [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN). |

### setPreserveIncludePictureField(boolean value) {#setPreserveIncludePictureField-boolean}
```
public void setPreserveIncludePictureField(boolean value)
```


Establece si se debe preservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. El valor predeterminado es  false .

 **Remarks:** 

Por defecto, el campo INCLUDEPICTURE se convierte en un objeto de forma. Puedes sobrescribirlo si necesitas que el campo se preserve, por ejemplo, si deseas actualizarlo programáticamente. Ten en cuenta, sin embargo, que este enfoque no es común para Aspose.Words. Úsalo bajo tu propio riesgo.

Uno de los posibles casos de uso puede ser utilizar un MERGEFIELD como campo hijo para cambiar dinámicamente la ruta de origen de la imagen. En este caso necesitas que el INCLUDEPICTURE se preserve en el modelo.

 **Examples:** 

Muestra cómo conservar o descartar los campos INCLUDEPICTURE al cargar un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Indica si se debe preservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. |

### setProgressCallback(IDocumentLoadingCallback value) {#setProgressCallback-com.aspose.words.IDocumentLoadingCallback}
```
public void setProgressCallback(IDocumentLoadingCallback value)
```


Se llama durante la carga de un documento y acepta datos sobre el progreso de la carga.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

Muestra cómo notificar al usuario si la carga del documento supera el tiempo de carga esperado.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) | El valor correspondiente de [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/). |

### setRecoveryMode(int value) {#setRecoveryMode-int}
```
public void setRecoveryMode(int value)
```


Define cómo debe manejarse el documento si se producen errores durante la carga. Usa esta propiedad para especificar si el sistema debe intentar recuperar el documento o seguir otro comportamiento definido. El valor predeterminado es [DocumentRecoveryMode.TRY\_RECOVER](../../com.aspose.words/documentrecoverymode/\#TRY-RECOVER).

 **Examples:** 

Muestra cómo intentar recuperar un documento si se produjeron errores durante la carga.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/). |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando un documento se importa desde HTML, MHTML.

 **Examples:** 

Muestra cómo manejar recursos externos al cargar documentos Html.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) | El valor correspondiente de [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/). |

### setSoftLineBreakCharacter(char value) {#setSoftLineBreakCharacter-char}
```
public void setSoftLineBreakCharacter(char value)
```


Establece un valor de carácter que representa un salto de línea suave. El valor predeterminado es  SPACE (U+0020) .

 **Remarks:** 

Nota, establecer esta opción a [ControlChar.LINE\_BREAK\_CHAR](../../com.aspose.words/controlchar/\#LINE-BREAK-CHAR) permite cargar saltos de línea suaves como saltos de línea duros.

 **Examples:** 

Muestra cómo establecer el carácter de salto de línea suave.

```

 try (ByteArrayInputStream stream = new ByteArrayInputStream("line1\nline2".getBytes(StandardCharsets.UTF_8)))
 {
     MarkdownLoadOptions loadOptions = new MarkdownLoadOptions();
     loadOptions.setSoftLineBreakCharacter(ControlChar.LINE_BREAK_CHAR);
     Document doc = new Document(stream, loadOptions);

     Assert.assertEquals("line1line2", doc.getText().trim());
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | char | Un valor de carácter que representa un salto de línea suave. |

### setTempFolder(String value) {#setTempFolder-java.lang.String}
```
public void setTempFolder(String value)
```


Permite usar archivos temporales al leer el documento. Por defecto, esta propiedad es null y no se utilizan archivos temporales.

 **Remarks:** 

La carpeta debe existir y ser escribible, de lo contrario se lanzará una excepción.

Aspose.Words elimina automáticamente todos los archivos temporales cuando la lectura se completa.

 **Examples:** 

Muestra cómo cargar un documento usando archivos temporales.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

Muestra cómo usar el disco duro en lugar de la memoria al cargar un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

### setUpdateDirtyFields(boolean value) {#setUpdateDirtyFields-boolean}
```
public void setUpdateDirtyFields(boolean value)
```


Especifica si se deben actualizar los campos con el  dirty  atributo.

 **Examples:** 

Muestra cómo usar la propiedad especial para actualizar el resultado del campo.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setUseSystemLcid(boolean value) {#setUseSystemLcid-boolean}
```
public void setUseSystemLcid(boolean value)
```


Establece si se debe usar el valor LCID obtenido del registro de Windows para determinar los márgenes predeterminados de la configuración de página.

 **Remarks:** 

Si se establece en true, se emula el comportamiento de MS Word que toma el valor LCID del registro de Windows.

El valor predeterminado es  false .

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Indica si se debe usar el valor LCID obtenido del registro de Windows para determinar los márgenes predeterminados de la configuración de página. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Se llama durante una operación de carga, cuando se detecta un problema que podría resultar en pérdida de datos o de fidelidad de formato.

 **Examples:** 

Muestra cómo imprimir y almacenar advertencias que ocurren durante la carga del documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | El valor correspondiente de [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

