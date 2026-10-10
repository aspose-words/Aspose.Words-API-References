---
title: "HtmlLoadOptions"
linktitle: "HtmlLoadOptions"
second_title: "Aspose.Words para Java"
description: "Permite especificar opciones adicionales al cargar un documento HTML en un objeto Document en Java."
type: docs
weight: 382
url: /es/java/com.aspose.words/htmlloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions/)
```
public class HtmlLoadOptions extends LoadOptions
```

Permite especificar opciones adicionales al cargar un documento HTML en un objeto [Document](../../com.aspose.words/document/).

Para obtener más información, visite el artículo de documentación [ Specify Load Options ][Specify Load Options].

 **Examples:** 

Muestra cómo admitir comentarios condicionales al cargar un documento HTML.

```

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();

 // If the value is true, then we take VML code into account while parsing the loaded document.
 loadOptions.setSupportVml(supportVml);

 // This document contains a JPEG image within "
```


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## Constructores

| Constructor | Descripción |
| --- | --- |
| [HtmlLoadOptions()](#HtmlLoadOptions) | Inicializa una nueva instancia de esta clase con valores predeterminados. |
| [HtmlLoadOptions(String password)](#HtmlLoadOptions-java.lang.String) | Un atajo para inicializar una nueva instancia de esta clase con la contraseña especificada para cargar un documento cifrado. |
| [HtmlLoadOptions(int loadFormat, String password, String baseUri)](#HtmlLoadOptions-int-java.lang.String-java.lang.String) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Determina si el objeto especificado es igual en valor al objeto actual. |
| [getBaseUri()](#getBaseUri) | Obtiene la cadena que se usará para resolver URIs relativos encontrados en el documento en URIs absolutos cuando sea necesario. |
| [getBlockImportMode()](#getBlockImportMode) | Obtiene un valor que especifica cómo se importan las propiedades de los elementos de nivel de bloque. |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng) | Obtiene si convertir imágenes de metarchivo ( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) al formato de imagen **F:Aspose.FileFormat.Png**. |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath) | Obtiene si convertir formas con EquationXML a objetos Office Math. |
| [getConvertSvgToEmf()](#getConvertSvgToEmf) | Obtiene un valor que indica si convertir imágenes SVG cargadas al formato EMF. |
| [getEncoding()](#getEncoding) | Obtiene la codificación que se usará para cargar un documento HTML, TXT o CHM si la codificación no está especificada dentro del documento. |
| [getFontSettings()](#getFontSettings) | Permite especificar la configuración de fuentes del documento. |
| [getIgnoreNoscriptElements()](#getIgnoreNoscriptElements) | Obtiene un valor que indica si ignorar los elementos HTML. |
| [getIgnoreOleData()](#getIgnoreOleData) | Especifica si ignorar los datos OLE. |
| [getLanguagePreferences()](#getLanguagePreferences) | Obtiene las preferencias de idioma que se usarán cuando se cargue el documento. |
| [getLoadFormat()](#getLoadFormat) | Especifica el formato del documento que se cargará. |
| [getMswVersion()](#getMswVersion) | Permite especificar que el proceso de carga del documento coincida con una versión específica de MS Word. |
| [getPassword()](#getPassword) | Obtiene la contraseña para abrir un documento cifrado. |
| [getPreferredControlType()](#getPreferredControlType) | Obtiene el tipo preferido de nodos de documento que representarán los elementos importados  y . |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField) | Obtiene si preservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. |
| [getProgressCallback()](#getProgressCallback) | Se llama durante la carga de un documento y acepta datos sobre el progreso de la carga. |
| [getRecoveryMode()](#getRecoveryMode) | Define cómo debe manejarse el documento si se producen errores durante la carga. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback) | Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando un documento se importa desde HTML, MHTML. |
| [getSupportFontFaceRules()](#getSupportFontFaceRules) | Obtiene un valor que indica si se admiten reglas @font-face y si se cargan las fuentes declaradas. |
| [getSupportVml()](#getSupportVml) | Obtiene un valor que indica si se admiten imágenes VML. |
| [getTempFolder()](#getTempFolder) | Permite usar archivos temporales al leer el documento. |
| [getUpdateDirtyFields()](#getUpdateDirtyFields) | Especifica si se deben actualizar los campos con el  dirty  atributo. |
| [getUseSystemLcid()](#getUseSystemLcid) | Obtiene si se debe usar el valor LCID obtenido del registro de Windows para determinar los márgenes predeterminados de la configuración de página. |
| [getWarningCallback()](#getWarningCallback) | Se llama durante una operación de carga, cuando se detecta un problema que podría resultar en pérdida de datos o de fidelidad de formato. |
| [getWebRequestTimeout()](#getWebRequestTimeout) | El número de milisegundos a esperar antes de que la solicitud web expire. |
| [setBaseUri(String value)](#setBaseUri-java.lang.String) | Establece la cadena que se usará para resolver URIs relativos encontrados en el documento en URIs absolutos cuando sea necesario. |
| [setBlockImportMode(int value)](#setBlockImportMode-int) | Establece un valor que especifica cómo se importan las propiedades de los elementos de nivel de bloque. |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean) | Establece si se convierten imágenes metafile( **F:Aspose.FileFormat.Wmf** o **F:Aspose.FileFormat.Emf**) al formato de imagen **F:Aspose.FileFormat.Png**. |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean) | Establece si se convierten formas con EquationXML a objetos de Office Math. |
| [setConvertSvgToEmf(boolean value)](#setConvertSvgToEmf-boolean) | Establece un valor que indica si se convierten imágenes SVG cargadas al formato EMF. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) | Establece la codificación que se usará para cargar un documento HTML, TXT o CHM si la codificación no está especificada dentro del documento. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Permite especificar la configuración de fuentes del documento. |
| [setIgnoreNoscriptElements(boolean value)](#setIgnoreNoscriptElements-boolean) | Establece un valor que indica si se deben ignorar  los elementos HTML. |
| [setIgnoreOleData(boolean value)](#setIgnoreOleData-boolean) | Especifica si ignorar los datos OLE. |
| [setLoadFormat(int value)](#setLoadFormat-int) | Especifica el formato del documento que se cargará. |
| [setMswVersion(int value)](#setMswVersion-int) | Permite especificar que el proceso de carga del documento coincida con una versión específica de MS Word. |
| [setPassword(String value)](#setPassword-java.lang.String) | Establece la contraseña para abrir un documento cifrado. |
| [setPreferredControlType(int value)](#setPreferredControlType-int) | Establece el tipo preferido de nodos de documento que representarán los elementos importados  y  elementos. |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean) | Establece si se debe preservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback) | Se llama durante la carga de un documento y acepta datos sobre el progreso de la carga. |
| [setRecoveryMode(int value)](#setRecoveryMode-int) | Define cómo debe manejarse el documento si se producen errores durante la carga. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback) | Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando un documento se importa desde HTML, MHTML. |
| [setSupportFontFaceRules(boolean value)](#setSupportFontFaceRules-boolean) | Establece un valor que indica si se admiten reglas @font-face y si se cargan las fuentes declaradas. |
| [setSupportVml(boolean value)](#setSupportVml-boolean) | Establece un valor que indica si se admiten imágenes VML. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Permite usar archivos temporales al leer el documento. |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean) | Especifica si se deben actualizar los campos con el  dirty  atributo. |
| [setUseSystemLcid(boolean value)](#setUseSystemLcid-boolean) | Establece si se debe usar el valor LCID obtenido del registro de Windows para determinar los márgenes predeterminados de la configuración de página. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Se llama durante una operación de carga, cuando se detecta un problema que podría resultar en pérdida de datos o de fidelidad de formato. |
| [setWebRequestTimeout(int value)](#setWebRequestTimeout-int) | El número de milisegundos a esperar antes de que la solicitud web expire. |
### HtmlLoadOptions() {#HtmlLoadOptions}
```
public HtmlLoadOptions()
```


Inicializa una nueva instancia de esta clase con valores predeterminados.

 **Examples:** 

Muestra cómo admitir comentarios condicionales al cargar un documento HTML.

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


Un atajo para inicializar una nueva instancia de esta clase con la contraseña especificada para cargar un documento cifrado.

 **Examples:** 

Muestra cómo cifrar un documento Html y luego abrirlo usando una contraseña.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| contraseña | java.lang.String | La contraseña para abrir un documento cifrado. Puede ser  null  o una cadena vacía. |

### HtmlLoadOptions(int loadFormat, String password, String baseUri) {#HtmlLoadOptions-int-java.lang.String-java.lang.String}
```
public HtmlLoadOptions(int loadFormat, String password, String baseUri)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| loadFormat | int |  |
| contraseña | java.lang.String |  |
| baseUri | java.lang.String |  |

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
### getBlockImportMode() {#getBlockImportMode}
```
public int getBlockImportMode()
```


Obtiene un valor que especifica cómo se importan las propiedades de los elementos de nivel de bloque. El valor predeterminado es [BlockImportMode.MERGE](../../com.aspose.words/blockimportmode/\#MERGE).

 **Examples:** 

Muestra cómo se importan las propiedades de los elementos de bloque desde documentos basados en HTML.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```

**Returns:**
int - Un valor que especifica cómo se importan las propiedades de los elementos de nivel de bloque. El valor devuelto es una de las constantes de [BlockImportMode](../../com.aspose.words/blockimportmode/).
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
### getConvertSvgToEmf() {#getConvertSvgToEmf}
```
public boolean getConvertSvgToEmf()
```


Obtiene un valor que indica si se convierten las imágenes SVG cargadas al formato EMF. El valor predeterminado es  false  y, si es posible, las imágenes SVG cargadas se almacenan tal cual sin conversión.

 **Remarks:** 

Las versiones más recientes de MS Word admiten imágenes SVG de forma nativa. Si la versión de MS Word especificada en las opciones de carga admite SVG, Aspose.Words almacenará las imágenes SVG tal cual sin conversión. Si SVG no es compatible, las imágenes SVG cargadas se convertirán al formato EMF.

Si, sin embargo, esta opción se establece en  true , Aspose.Words convertirá las imágenes SVG cargadas a EMF incluso si las imágenes SVG son compatibles con la versión especificada de MS Word.

 **Examples:** 

Muestra cómo convertir objetos SVG a un formato diferente al guardar documentos HTML.

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
boolean - Un valor que indica si se convierten las imágenes SVG cargadas al formato EMF.
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
### getIgnoreNoscriptElements() {#getIgnoreNoscriptElements}
```
public boolean getIgnoreNoscriptElements()
```


Obtiene un valor que indica si se deben ignorar los elementos  HTML. El valor predeterminado es  false .

 **Remarks:** 

Al igual que MS Word, Aspose.Words no admite scripts y, por defecto, carga el contenido de los elementos  en el documento resultante. Sin embargo, en la mayoría de los navegadores los scripts son compatibles y el contenido de  no es visible. Establecer esta propiedad en  true  obliga a Aspose.Words a ignorar todos los elementos  y ayuda a producir documentos que se asemejen más a lo que se ve en los navegadores.

 **Examples:** 

Muestra cómo ignorar los elementos  HTML.

```

 final String html = "\r\n\r\n\r\nNOSCRIPT\r\n\r\n\r\n\r\n\r\n Your browser does not support JavaScript!\r\n\r\n";

 HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
 htmlLoadOptions.setIgnoreNoscriptElements(ignoreNoscriptElements);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), htmlLoadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.IgnoreNoscriptElements.pdf");
 
```

**Returns:**
boolean - Un valor que indica si se deben ignorar los elementos  HTML.
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
### getPreferredControlType() {#getPreferredControlType}
```
public int getPreferredControlType()
```


Obtiene el tipo preferido de nodos de documento que representarán los elementos  y . Valor predeterminado es [HtmlControlType.FORM\_FIELD](../../com.aspose.words/htmlcontroltype/\#FORM-FIELD). Observaciones: Tenga en cuenta que establecer esta propiedad no garantiza que todos los controles importados sean del tipo especificado. Si un control HTML no es representable con nodos de documento del tipo preferido, Aspose.Words utilizará un [HtmlControlType](../../com.aspose.words/htmlcontroltype/) compatible para ese control. Ejemplos: Muestra cómo establecer el tipo preferido de nodos de documento que representarán los elementos  y .   final String html = "\\r\\n\\r\\n\\r\\n" + "item1\\r\\n\\r\\n\\r\\n\\r\\n"; HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions(); htmlLoadOptions.setPreferredControlType(HtmlControlType.STRUCTURED\_DOCUMENT\_TAG); Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF\_8)), htmlLoadOptions); NodeCollection nodes = doc.getChildNodes(NodeType.STRUCTURED\_DOCUMENT\_TAG, true); StructuredDocumentTag tag = (StructuredDocumentTag) nodes.get(0);

**Returns:**
int - Tipo preferido de nodos de documento que representarán los elementos  y . El valor devuelto es una de las constantes de [HtmlControlType](../../com.aspose.words/htmlcontroltype/).
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
### getSupportFontFaceRules() {#getSupportFontFaceRules}
```
public boolean getSupportFontFaceRules()
```


Obtiene un valor que indica si se deben admitir reglas @font-face y si se deben cargar las fuentes declaradas. El valor predeterminado es false.

 **Remarks:** 

Si esta opción está habilitada, las fuentes declaradas en reglas @font-face se cargan e incrustan en las definiciones de fuentes del documento resultante (ver [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos)). Esto hace que las fuentes cargadas estén disponibles para el renderizado, pero no habilita automáticamente la incrustación de las fuentes al guardar. Para guardar el documento con las fuentes cargadas, la propiedad [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) de la colección [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) debe establecerse en true.

Los formatos de fuente compatibles son TTF, EOT y WOFF.

**Returns:**
boolean - Un valor que indica si se deben admitir reglas @font-face y si se deben cargar las fuentes declaradas.
### getSupportVml() {#getSupportVml}
```
public boolean getSupportVml()
```


Obtiene un valor que indica si se admiten imágenes VML.

 **Examples:** 

Muestra cómo admitir comentarios condicionales al cargar un documento HTML.

```

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();

 // If the value is true, then we take VML code into account while parsing the loaded document.
 loadOptions.setSupportVml(supportVml);

 // This document contains a JPEG image within "
```

**Returns:**
boolean - Un valor que indica si se deben admitir imágenes VML.
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
### getWebRequestTimeout() {#getWebRequestTimeout}
```
public int getWebRequestTimeout()
```


El número de milisegundos a esperar antes de que la solicitud web expire. El valor predeterminado es 100000 milisegundos (100 segundos).

 **Remarks:** 

El número de milisegundos que Aspose.Words espera por una respuesta al cargar recursos externos (imágenes, hojas de estilo) vinculados en documentos HTML y MHTML.

**Returns:**
int - El valor  int  correspondiente.
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

### setBlockImportMode(int value) {#setBlockImportMode-int}
```
public void setBlockImportMode(int value)
```


Establece un valor que especifica cómo se importan las propiedades de los elementos de nivel de bloque. El valor predeterminado es [BlockImportMode.MERGE](../../com.aspose.words/blockimportmode/\#MERGE).

 **Examples:** 

Muestra cómo se importan las propiedades de los elementos de bloque desde documentos basados en HTML.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Un valor que especifica cómo se importan las propiedades de los elementos de nivel de bloque. El valor debe ser una de las constantes de [BlockImportMode](../../com.aspose.words/blockimportmode/). |

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

### setConvertSvgToEmf(boolean value) {#setConvertSvgToEmf-boolean}
```
public void setConvertSvgToEmf(boolean value)
```


Establece un valor que indica si se convierten las imágenes SVG cargadas al formato EMF. El valor predeterminado es  false  y, si es posible, las imágenes SVG cargadas se almacenan tal cual sin conversión.

 **Remarks:** 

Las versiones más recientes de MS Word admiten imágenes SVG de forma nativa. Si la versión de MS Word especificada en las opciones de carga admite SVG, Aspose.Words almacenará las imágenes SVG tal cual sin conversión. Si SVG no es compatible, las imágenes SVG cargadas se convertirán al formato EMF.

Si, sin embargo, esta opción se establece en  true , Aspose.Words convertirá las imágenes SVG cargadas a EMF incluso si las imágenes SVG son compatibles con la versión especificada de MS Word.

 **Examples:** 

Muestra cómo convertir objetos SVG a un formato diferente al guardar documentos HTML.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que indica si se convierten las imágenes SVG cargadas al formato EMF. |

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

### setIgnoreNoscriptElements(boolean value) {#setIgnoreNoscriptElements-boolean}
```
public void setIgnoreNoscriptElements(boolean value)
```


Establece un valor que indica si se deben ignorar los elementos HTML. El valor predeterminado es  false .

 **Remarks:** 

Al igual que MS Word, Aspose.Words no admite scripts y, por defecto, carga el contenido de los elementos  en el documento resultante. Sin embargo, en la mayoría de los navegadores los scripts son compatibles y el contenido de  no es visible. Establecer esta propiedad en  true  obliga a Aspose.Words a ignorar todos los elementos  y ayuda a producir documentos que se asemejen más a lo que se ve en los navegadores.

 **Examples:** 

Muestra cómo ignorar los elementos  HTML.

```

 final String html = "\r\n\r\n\r\nNOSCRIPT\r\n\r\n\r\n\r\n\r\n Your browser does not support JavaScript!\r\n\r\n";

 HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
 htmlLoadOptions.setIgnoreNoscriptElements(ignoreNoscriptElements);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), htmlLoadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.IgnoreNoscriptElements.pdf");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que indica si se deben ignorar los elementos HTML. |

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

### setPreferredControlType(int value) {#setPreferredControlType-int}
```
public void setPreferredControlType(int value)
```


Establece el tipo preferido de nodos de documento que representarán los elementos importados  y . El valor predeterminado es [HtmlControlType.FORM\_FIELD](../../com.aspose.words/htmlcontroltype/\#FORM-FIELD). Comentarios: Tenga en cuenta que establecer esta propiedad no garantiza que todos los controles importados sean del tipo especificado. Si un control HTML no es representable con nodos de documento del tipo preferido, Aspose.Words utilizará un [HtmlControlType](../../com.aspose.words/htmlcontroltype/) compatible para ese control. Ejemplos: Muestra cómo establecer el tipo preferido de nodos de documento que representarán los elementos importados  y .   final String html = "\\r\\n\\r\\n\\r\\n" + "item1\\r\\n\\r\\n\\r\\n\\r\\n"; HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions(); htmlLoadOptions.setPreferredControlType(HtmlControlType.STRUCTURED\_DOCUMENT\_TAG); Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF\_8)), htmlLoadOptions); NodeCollection nodes = doc.getChildNodes(NodeType.STRUCTURED\_DOCUMENT\_TAG, true); StructuredDocumentTag tag = (StructuredDocumentTag) nodes.get(0);

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Tipo preferido de nodos de documento que representarán los elementos importados  y . El valor debe ser una de las constantes de [HtmlControlType](../../com.aspose.words/htmlcontroltype/). |

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

### setSupportFontFaceRules(boolean value) {#setSupportFontFaceRules-boolean}
```
public void setSupportFontFaceRules(boolean value)
```


Establece un valor que indica si se deben admitir reglas @font-face y si se deben cargar fuentes declaradas. El valor predeterminado es  false .

 **Remarks:** 

Si esta opción está habilitada, las fuentes declaradas en reglas @font-face se cargan e incrustan en las definiciones de fuentes del documento resultante (ver [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos)). Esto hace que las fuentes cargadas estén disponibles para el renderizado, pero no habilita automáticamente la incrustación de las fuentes al guardar. Para guardar el documento con las fuentes cargadas, la propiedad [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) de la colección [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) debe establecerse en true.

Los formatos de fuente compatibles son TTF, EOT y WOFF.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que indica si se deben admitir reglas @font-face y si se deben cargar fuentes declaradas. |

### setSupportVml(boolean value) {#setSupportVml-boolean}
```
public void setSupportVml(boolean value)
```


Establece un valor que indica si se admiten imágenes VML.

 **Examples:** 

Muestra cómo admitir comentarios condicionales al cargar un documento HTML.

```

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();

 // If the value is true, then we take VML code into account while parsing the loaded document.
 loadOptions.setSupportVml(supportVml);

 // This document contains a JPEG image within "
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor que indica si se admiten imágenes VML. |

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

### setWebRequestTimeout(int value) {#setWebRequestTimeout-int}
```
public void setWebRequestTimeout(int value)
```


El número de milisegundos a esperar antes de que la solicitud web expire. El valor predeterminado es 100000 milisegundos (100 segundos).

 **Remarks:** 

El número de milisegundos que Aspose.Words espera por una respuesta al cargar recursos externos (imágenes, hojas de estilo) vinculados en documentos HTML y MHTML.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

