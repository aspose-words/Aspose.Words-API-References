---
title: "HtmlLoadOptions"
linktitle: "HtmlLoadOptions"
second_title: "Aspose.Words для Java"
description: "Позволяет указывать дополнительные параметры при загрузке HTML‑документа в объект Document в Java."
type: docs
weight: 382
url: /ru/java/com.aspose.words/htmlloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions/)
```
public class HtmlLoadOptions extends LoadOptions
```

Позволяет указывать дополнительные параметры при загрузке HTML‑документа в объект [Document](../../com.aspose.words/document/).

Чтобы узнать больше, посетите статью документации [ Specify Load Options ][Specify Load Options].

 **Examples:** 

Показывает, как поддерживать условные комментарии при загрузке HTML‑документа.

```

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();

 // If the value is true, then we take VML code into account while parsing the loaded document.
 loadOptions.setSupportVml(supportVml);

 // This document contains a JPEG image within "
```


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [HtmlLoadOptions()](#HtmlLoadOptions) | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |
| [HtmlLoadOptions(String password)](#HtmlLoadOptions-java.lang.String) | Сокращение для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа. |
| [HtmlLoadOptions(int loadFormat, String password, String baseUri)](#HtmlLoadOptions-int-java.lang.String-java.lang.String) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [getBaseUri()](#getBaseUri) | Получает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости. |
| [getBlockImportMode()](#getBlockImportMode) | Получает значение, указывающее, как импортируются свойства блочных элементов. |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng) | Получает, следует ли конвертировать метафайлы ( **F:Aspose.FileFormat.Wmf** или **F:Aspose.FileFormat.Emf**) в формат изображения **F:Aspose.FileFormat.Png**. |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath) | Получает, следует ли конвертировать фигуры с EquationXML в объекты Office Math. |
| [getConvertSvgToEmf()](#getConvertSvgToEmf) | Получает значение, указывающее, следует ли конвертировать загруженные SVG‑изображения в формат EMF. |
| [getEncoding()](#getEncoding) | Получает кодировку, которая будет использоваться для загрузки HTML, TXT или CHM‑документа, если кодировка не указана внутри документа. |
| [getFontSettings()](#getFontSettings) | Позволяет задавать параметры шрифтов документа. |
| [getIgnoreNoscriptElements()](#getIgnoreNoscriptElements) | Получает значение, указывающее, следует ли игнорировать элементы HTML. |
| [getIgnoreOleData()](#getIgnoreOleData) | Указывает, следует ли игнорировать данные OLE. |
| [getLanguagePreferences()](#getLanguagePreferences) | Получает предпочтения языка, которые будут использоваться при загрузке документа. |
| [getLoadFormat()](#getLoadFormat) | Указывает формат загружаемого документа. |
| [getMswVersion()](#getMswVersion) | Позволяет указать, что процесс загрузки документа должен соответствовать определённой версии MS Word. |
| [getPassword()](#getPassword) | Получает пароль для открытия зашифрованного документа. |
| [getPreferredControlType()](#getPreferredControlType) | Получает предпочтительный тип узлов документа, которые будут представлять импортированные  и  элементы. |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField) | Получает, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. |
| [getProgressCallback()](#getProgressCallback) | Вызывается во время загрузки документа и принимает данные о прогрессе загрузки. |
| [getRecoveryMode()](#getRecoveryMode) | Определяет, как документ должен обрабатываться, если при загрузке происходят ошибки. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback) | Позволяет контролировать, как внешние ресурсы (изображения, таблицы стилей) загружаются при импорте документа из HTML, MHTML. |
| [getSupportFontFaceRules()](#getSupportFontFaceRules) | Возвращает значение, указывающее, поддерживать ли правила @font-face и загружать ли объявленные шрифты. |
| [getSupportVml()](#getSupportVml) | Возвращает значение, указывающее, поддерживать ли VML‑изображения. |
| [getTempFolder()](#getTempFolder) | Позволяет использовать временные файлы при чтении документа. |
| [getUpdateDirtyFields()](#getUpdateDirtyFields) | Указывает, обновлять ли поля с атрибутом  dirty . |
| [getUseSystemLcid()](#getUseSystemLcid) | Возвращает, использовать ли значение LCID, полученное из реестра Windows, для определения полей по умолчанию в настройках страницы. |
| [getWarningCallback()](#getWarningCallback) | Вызывается во время операции загрузки, когда обнаруживается проблема, которая может привести к потере точности данных или форматирования. |
| [getWebRequestTimeout()](#getWebRequestTimeout) | Количество миллисекунд ожидания до истечения времени запроса. |
| [setBaseUri(String value)](#setBaseUri-java.lang.String) | Устанавливает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости. |
| [setBlockImportMode(int value)](#setBlockImportMode-int) | Устанавливает значение, определяющее, как импортируются свойства блочных элементов. |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean) | Устанавливает, преобразовывать ли метафайлы( **F:Aspose.FileFormat.Wmf** или **F:Aspose.FileFormat.Emf**) в формат изображения **F:Aspose.FileFormat.Png**. |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean) | Устанавливает, преобразовывать ли фигуры с EquationXML в объекты Office Math. |
| [setConvertSvgToEmf(boolean value)](#setConvertSvgToEmf-boolean) | Устанавливает значение, указывающее, преобразовывать ли загруженные SVG‑изображения в формат EMF. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) | Устанавливает кодировку, которая будет использоваться для загрузки HTML, TXT или CHM документа, если кодировка не указана в документе. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Позволяет задавать параметры шрифтов документа. |
| [setIgnoreNoscriptElements(boolean value)](#setIgnoreNoscriptElements-boolean) | Устанавливает значение, указывающее, игнорировать ли  HTML‑элементы. |
| [setIgnoreOleData(boolean value)](#setIgnoreOleData-boolean) | Указывает, следует ли игнорировать данные OLE. |
| [setLoadFormat(int value)](#setLoadFormat-int) | Указывает формат загружаемого документа. |
| [setMswVersion(int value)](#setMswVersion-int) | Позволяет указать, что процесс загрузки документа должен соответствовать определённой версии MS Word. |
| [setPassword(String value)](#setPassword-java.lang.String) | Устанавливает пароль для открытия зашифрованного документа. |
| [setPreferredControlType(int value)](#setPreferredControlType-int) | Устанавливает предпочтительный тип узлов документа, которые будут представлять импортированные  и  элементы. |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean) | Устанавливает, сохранять ли поле INCLUDEPICTURE при чтении форматов Microsoft Word. |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback) | Вызывается во время загрузки документа и принимает данные о прогрессе загрузки. |
| [setRecoveryMode(int value)](#setRecoveryMode-int) | Определяет, как документ должен обрабатываться, если при загрузке происходят ошибки. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback) | Позволяет контролировать, как внешние ресурсы (изображения, таблицы стилей) загружаются при импорте документа из HTML, MHTML. |
| [setSupportFontFaceRules(boolean value)](#setSupportFontFaceRules-boolean) | Устанавливает значение, указывающее, поддерживать ли правила @font-face и загружать объявленные шрифты. |
| [setSupportVml(boolean value)](#setSupportVml-boolean) | Устанавливает значение, указывающее, поддерживать ли VML‑изображения. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | Позволяет использовать временные файлы при чтении документа. |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean) | Указывает, обновлять ли поля с атрибутом  dirty . |
| [setUseSystemLcid(boolean value)](#setUseSystemLcid-boolean) | Устанавливает, использовать ли значение LCID, полученное из реестра Windows, для определения полей по умолчанию в настройках страницы. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Вызывается во время операции загрузки, когда обнаруживается проблема, которая может привести к потере точности данных или форматирования. |
| [setWebRequestTimeout(int value)](#setWebRequestTimeout-int) | Количество миллисекунд ожидания до истечения времени запроса. |
### HtmlLoadOptions() {#HtmlLoadOptions}
```
public HtmlLoadOptions()
```


Инициализирует новый экземпляр этого класса со значениями по умолчанию.

 **Examples:** 

Показывает, как поддерживать условные комментарии при загрузке HTML‑документа.

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


Сокращение для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа.

 **Examples:** 

Показывает, как зашифровать HTML‑документ, а затем открыть его с помощью пароля.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| пароль | java.lang.String | Пароль для открытия зашифрованного документа. Может быть  null  или пустой строкой. |

### HtmlLoadOptions(int loadFormat, String password, String baseUri) {#HtmlLoadOptions-int-java.lang.String-java.lang.String}
```
public HtmlLoadOptions(int loadFormat, String password, String baseUri)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| loadFormat | int |  |
| пароль | java.lang.String |  |
| baseUri | java.lang.String |  |

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Определяет, равен ли указанный объект по значению текущему объекту.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getBaseUri() {#getBaseUri}
```
public String getBaseUri()
```


Получает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости. Может быть  null  или пустой строкой. По умолчанию —  null .

 **Remarks:** 

Это свойство используется для преобразования относительных URI в абсолютные в следующих случаях:

1.  При загрузке HTML‑документа из потока, если документ содержит изображения с относительными URI и не имеет базового URI, указанного в элементе BASE HTML.
2.  При сохранении документа в PDF и другие форматы, чтобы получить изображения, связанные с помощью относительных URI, чтобы их можно было сохранить в выходном документе.

 **Examples:** 

Показывает, как открыть HTML‑документ с изображениями из потока, используя базовый URI.

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
java.lang.String - Строка, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости.
### getBlockImportMode() {#getBlockImportMode}
```
public int getBlockImportMode()
```


Получает значение, указывающее, как импортируются свойства блочных элементов. Значение по умолчанию — [BlockImportMode.MERGE](../../com.aspose.words/blockimportmode/\#MERGE).

 **Examples:** 

Показывает, как свойства блочных элементов импортируются из HTML‑документов.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```

**Returns:**
int - Значение, указывающее, как импортируются свойства блочных элементов. Возвращаемое значение является одной из констант [BlockImportMode](../../com.aspose.words/blockimportmode/).
### getConvertMetafilesToPng() {#getConvertMetafilesToPng}
```
public boolean getConvertMetafilesToPng()
```


Получает, следует ли конвертировать метафайлы ( **F:Aspose.FileFormat.Wmf** или **F:Aspose.FileFormat.Emf**) в формат изображения **F:Aspose.FileFormat.Png**.

 **Remarks:** 

Метaфайлы ( **F:Aspose.FileFormat.Wmf** или **F:Aspose.FileFormat.Emf**) — это несжатый формат изображений, который иногда требует слишком много ОЗУ для хранения и обработки документа. Эта опция позволяет при загрузке документа преобразовать все изображения метафайлов в **F:Aspose.FileFormat.Png**. Обратите внимание — преобразование векторной графики в растровую уменьшает качество изображений.

 **Examples:** 

Показывает, как преобразовать WMF/EMF в PNG при загрузке документа.

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
boolean - Нужно ли преобразовывать изображения метафайлов ( **F:Aspose.FileFormat.Wmf** или **F:Aspose.FileFormat.Emf**) в формат изображения **F:Aspose.FileFormat.Png**.
### getConvertShapeToOfficeMath() {#getConvertShapeToOfficeMath}
```
public boolean getConvertShapeToOfficeMath()
```


Получает, следует ли конвертировать фигуры с EquationXML в объекты Office Math.

 **Examples:** 

Показывает, как преобразовать фигуры EquationXML в объекты Office Math.

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
boolean - Нужно ли преобразовывать фигуры с EquationXML в объекты Office Math.
### getConvertSvgToEmf() {#getConvertSvgToEmf}
```
public boolean getConvertSvgToEmf()
```


Получает значение, указывающее, следует ли преобразовывать загруженные SVG‑изображения в формат EMF. Значение по умолчанию —  false , и, если возможно, загруженные SVG‑изображения сохраняются без преобразования.

 **Remarks:** 

Новые версии MS Word поддерживают SVG‑изображения напрямую. Если версия MS Word, указанная в параметрах загрузки, поддерживает SVG, Aspose.Words сохранит SVG‑изображения без преобразования. Если SVG не поддерживается, загруженные SVG‑изображения будут преобразованы в формат EMF.

Если же эта опция установлена в  true , Aspose.Words будет преобразовывать загруженные SVG‑изображения в EMF, даже если SVG‑изображения поддерживаются указанной версией MS Word.

 **Examples:** 

Показывает, как преобразовать объекты SVG в другой формат при сохранении HTML‑документов.

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
boolean - Значение, указывающее, следует ли преобразовывать загруженные SVG‑изображения в формат EMF.
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


Получает кодировку, которая будет использоваться для загрузки HTML, TXT или CHM‑документа, если кодировка не указана внутри документа. Может быть  null . По умолчанию —  null .

 **Remarks:** 

Это свойство используется только при загрузке HTML, TXT или CHM‑документов.

Если кодировка не указана внутри документа и это свойство равно  null , система попытается автоматически определить кодировку.

 **Examples:** 

Показывает, как задать кодировку для открытия документа.

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
java.nio.charset.Charset - Кодировка, которая будет использоваться для загрузки HTML, TXT или CHM‑документа, если кодировка не указана внутри документа.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Позволяет задавать параметры шрифтов документа.

 **Remarks:** 

При загрузке некоторых форматов Aspose.Words может потребоваться разрешить шрифты. Например, при загрузке HTML‑документов Aspose.Words может разрешать шрифты для выполнения резервирования шрифтов.

Если установлено в  null , будут использованы настройки статических шрифтов по умолчанию [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance).

Значение по умолчанию равно  null .

 **Examples:** 

Показывает, как назначать заменители шрифтов при загрузке.

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

Показывает, как применять настройки замены шрифтов при загрузке документа.

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


Возвращает значение, указывающее, следует ли игнорировать  HTML‑элементы. Значение по умолчанию —  false .

 **Remarks:** 

Как и MS Word, Aspose.Words не поддерживает скрипты и по умолчанию загружает содержимое  элементов в получаемый документ. Однако в большинстве браузеров скрипты поддерживаются, и содержимое  не отображается. Установка этого свойства в  true  заставляет Aspose.Words игнорировать все  элементы и помогает создавать документы, более похожие на то, что видят в браузерах.

 **Examples:** 

Показывает, как игнорировать  HTML‑элементы.

```

 final String html = "\r\n\r\n\r\nNOSCRIPT\r\n\r\n\r\n\r\n\r\n Your browser does not support JavaScript!\r\n\r\n";

 HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
 htmlLoadOptions.setIgnoreNoscriptElements(ignoreNoscriptElements);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), htmlLoadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.IgnoreNoscriptElements.pdf");
 
```

**Returns:**
boolean — значение, указывающее, следует ли игнорировать  HTML‑элементы.
### getIgnoreOleData() {#getIgnoreOleData}
```
public boolean getIgnoreOleData()
```


Указывает, следует ли игнорировать данные OLE.

 **Remarks:** 

Игнорирование данных OLE может снизить потребление памяти и повысить производительность без потери данных в случае, когда целевой формат не поддерживает объекты OLE.

Значение по умолчанию — false.

 **Examples:** 

Показывает, как игнорировать данные OLE при загрузке.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Returns:**
boolean - Соответствующее  boolean  значение.
### getLanguagePreferences() {#getLanguagePreferences}
```
public LanguagePreferences getLanguagePreferences()
```


Получает предпочтения языка, которые будут использоваться при загрузке документа.

 **Examples:** 

Показывает, как применить языковые предпочтения при загрузке документа.

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


Указывает формат загружаемого документа. По умолчанию — [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO).

 **Remarks:** 

Рекомендуется указывать значение [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) и позволять Aspose.Words автоматически определять формат файла. Если вы знаете формат документа, который собираетесь загрузить, вы можете задать его явно, что слегка сократит время загрузки за счёт уменьшения накладных расходов на автоматическое определение формата. Если указанный явно формат окажется неверным, будет выполнено автоматическое определение и будет предпринята вторая попытка загрузить файл.

 **Examples:** 

Показывает, как указать базовый URI при открытии HTML‑документа.

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
int — соответствующее  int  значение. Возвращаемое значение является одной из констант [LoadFormat](../../com.aspose.words/loadformat/).
### getMswVersion() {#getMswVersion}
```
public int getMswVersion()
```


Позволяет указать, что процесс загрузки документа должен соответствовать определённой версии MS Word. Значение по умолчанию — [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019).

 **Remarks:** 

Разные версии Word могут несколько по‑разному обрабатывать определённые аспекты содержимого и форматирования документа во время загрузки, что может привести к небольшим различиям в объектной модели документа (Document Object Model).

 **Examples:** 

Показывает, как эмулировать процесс загрузки документа, соответствующий конкретной версии Microsoft Word.

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
int — соответствующее  int  значение. Возвращаемое значение является одной из констант [MsWordVersion](../../com.aspose.words/mswordversion/).
### getPassword() {#getPassword}
```
public String getPassword()
```


Возвращает пароль для открытия зашифрованного документа. Может быть  null  или пустой строкой. По умолчанию —  null .

 **Remarks:** 

Для открытия зашифрованного документа необходимо знать пароль. Если документ не зашифрован, установите значение  null  или пустую строку.

 **Examples:** 

Показывает, как подписать зашифрованный файл документа.

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
java.lang.String — пароль для открытия зашифрованного документа.
### getPreferredControlType() {#getPreferredControlType}
```
public int getPreferredControlType()
```


Возвращает предпочтительный тип узлов документа, которые будут представлять импортированные  и  элементы. Значение по умолчанию — [HtmlControlType.FORM\_FIELD](../../com.aspose.words/htmlcontroltype/\#FORM-FIELD). Примечание: обратите внимание, что установка этого свойства не гарантирует, что все импортированные элементы управления будут иметь указанный тип. Если HTML‑элемент нельзя представить узлами документа предпочтительного типа, Aspose.Words использует совместимый [HtmlControlType](../../com.aspose.words/htmlcontroltype/) для этого элемента. Примеры: показывает, как задать предпочтительный тип узлов документа, представляющих импортированные  и  элементы.   final String html = "\\r\\n\\r\\n\\r\\n" + "item1\\r\\n\\r\\n\\r\\n\\r\\n"; HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions(); htmlLoadOptions.setPreferredControlType(HtmlControlType.STRUCTURED\_DOCUMENT\_TAG); Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF\_8)), htmlLoadOptions); NodeCollection nodes = doc.getChildNodes(NodeType.STRUCTURED\_DOCUMENT\_TAG, true); StructuredDocumentTag tag = (StructuredDocumentTag) nodes.get(0);

**Returns:**
int — предпочтительный тип узлов документа, которые будут представлять импортированные  и  элементы. Возвращаемое значение является одной из констант [HtmlControlType](../../com.aspose.words/htmlcontroltype/).
### getPreserveIncludePictureField() {#getPreserveIncludePictureField}
```
public boolean getPreserveIncludePictureField()
```


Получает, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию — false.

 **Remarks:** 

По умолчанию поле INCLUDEPICTURE преобразуется в объект фигуры. Вы можете переопределить это, если требуется сохранить поле, например, если хотите обновлять его программно. Однако обратите внимание, что такой подход не распространён в Aspose.Words. Используйте его на свой страх и риск.

Одним из возможных сценариев использования может быть применение MERGEFIELD в качестве дочернего поля для динамического изменения пути к изображению. В этом случае необходимо сохранить INCLUDEPICTURE в модели.

 **Examples:** 

Показывает, как сохранять или отбрасывать поля INCLUDEPICTURE при загрузке документа.

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
boolean — следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word.
### getProgressCallback() {#getProgressCallback}
```
public IDocumentLoadingCallback getProgressCallback()
```


Вызывается во время загрузки документа и принимает данные о прогрессе загрузки.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

Показывает, как уведомить пользователя, если загрузка документа превысила ожидаемое время.

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


Определяет, как документ должен обрабатываться при возникновении ошибок во время загрузки. Используйте это свойство, чтобы указать, должна ли система пытаться восстановить документ или следовать другому определённому поведению. Значение по умолчанию — [DocumentRecoveryMode.TRY\_RECOVER](../../com.aspose.words/documentrecoverymode/\#TRY-RECOVER).

 **Examples:** 

Показывает, как попытаться восстановить документ, если во время загрузки произошли ошибки.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Returns:**
int — соответствующее значение int. Возвращаемое значение является одной из констант [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/).
### getResourceLoadingCallback() {#getResourceLoadingCallback}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Позволяет контролировать, как внешние ресурсы (изображения, таблицы стилей) загружаются при импорте документа из HTML, MHTML.

 **Examples:** 

Показывает, как обрабатывать внешние ресурсы при загрузке HTML‑документов.

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


Получает значение, указывающее, поддерживать ли правила @font-face и загружать объявленные шрифты. Значение по умолчанию — false.

 **Remarks:** 

Если эта опция включена, шрифты, объявленные в правилах @font-face, загружаются и встраиваются в определения шрифтов получаемого документа (см. [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos)). Это делает загруженные шрифты доступными для рендеринга, но не включает автоматическое встраивание шрифтов при сохранении. Чтобы сохранить документ с загруженными шрифтами, свойство [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) коллекции [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) должно быть установлено в true.

Поддерживаемые форматы шрифтов: TTF, EOT и WOFF.

**Returns:**
boolean — значение, указывающее, поддерживать ли правила @font-face и загружать объявленные шрифты.
### getSupportVml() {#getSupportVml}
```
public boolean getSupportVml()
```


Возвращает значение, указывающее, поддерживать ли VML‑изображения.

 **Examples:** 

Показывает, как поддерживать условные комментарии при загрузке HTML‑документа.

```

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();

 // If the value is true, then we take VML code into account while parsing the loaded document.
 loadOptions.setSupportVml(supportVml);

 // This document contains a JPEG image within "
```

**Returns:**
boolean — значение, указывающее, поддерживать ли изображения VML.
### getTempFolder() {#getTempFolder}
```
public String getTempFolder()
```


Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство равно null, и временные файлы не используются.

 **Remarks:** 

Папка должна существовать и быть доступной для записи, иначе будет выброшено исключение.

Aspose.Words автоматически удаляет все временные файлы после завершения чтения.

 **Examples:** 

Показывает, как загрузить документ, используя временные файлы.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

Показывает, как использовать жёсткий диск вместо памяти при загрузке документа.

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
java.lang.String - Соответствующее значение java.lang.String.
### getUpdateDirtyFields() {#getUpdateDirtyFields}
```
public boolean getUpdateDirtyFields()
```


Указывает, обновлять ли поля с атрибутом  dirty .

 **Examples:** 

Показывает, как использовать специальное свойство для обновления результата поля.

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
boolean - Соответствующее  boolean  значение.
### getUseSystemLcid() {#getUseSystemLcid}
```
public boolean getUseSystemLcid()
```


Возвращает, использовать ли значение LCID, полученное из реестра Windows, для определения полей по умолчанию в настройках страницы.

 **Remarks:** 

Если установить в true, то эмулируется поведение MS Word, которое берёт значение LCID из реестра Windows.

Значение по умолчанию — false.

**Returns:**
boolean — следует ли использовать значение LCID, полученное из реестра Windows, для определения полей по умолчанию при настройке страницы.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Вызывается во время операции загрузки, когда обнаруживается проблема, которая может привести к потере точности данных или форматирования.

 **Examples:** 

Показывает, как выводить и сохранять предупреждения, возникающие при загрузке документа.

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


Количество миллисекунд ожидания до истечения времени веб‑запроса. Значение по умолчанию — 100000 миллисекунд (100 секунд).

 **Remarks:** 

Количество миллисекунд, которое Aspose.Words ждёт ответа при загрузке внешних ресурсов (изображений, таблиц стилей), связанных в HTML‑ и MHTML‑документах.

**Returns:**
int — соответствующее значение  int .
### setBaseUri(String value) {#setBaseUri-java.lang.String}
```
public void setBaseUri(String value)
```


Устанавливает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости. Может быть null или пустой строкой. Значение по умолчанию — null.

 **Remarks:** 

Это свойство используется для преобразования относительных URI в абсолютные в следующих случаях:

1.  При загрузке HTML‑документа из потока, если документ содержит изображения с относительными URI и не имеет базового URI, указанного в элементе BASE HTML.
2.  При сохранении документа в PDF и другие форматы, чтобы получить изображения, связанные с помощью относительных URI, чтобы их можно было сохранить в выходном документе.

 **Examples:** 

Показывает, как открыть HTML‑документ с изображениями из потока, используя базовый URI.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Строка, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости. |

### setBlockImportMode(int value) {#setBlockImportMode-int}
```
public void setBlockImportMode(int value)
```


Устанавливает значение, определяющее, как импортируются свойства блочных элементов. Значение по умолчанию — [BlockImportMode.MERGE](../../com.aspose.words/blockimportmode/\#MERGE).

 **Examples:** 

Показывает, как свойства блочных элементов импортируются из HTML‑документов.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Значение, определяющее, как импортируются свойства блочных элементов. Значение должно быть одной из констант [BlockImportMode](../../com.aspose.words/blockimportmode/). |

### setConvertMetafilesToPng(boolean value) {#setConvertMetafilesToPng-boolean}
```
public void setConvertMetafilesToPng(boolean value)
```


Устанавливает, преобразовывать ли метафайлы( **F:Aspose.FileFormat.Wmf** или **F:Aspose.FileFormat.Emf**) в формат изображения **F:Aspose.FileFormat.Png**.

 **Remarks:** 

Метaфайлы ( **F:Aspose.FileFormat.Wmf** или **F:Aspose.FileFormat.Emf**) — это несжатый формат изображений, который иногда требует слишком много ОЗУ для хранения и обработки документа. Эта опция позволяет при загрузке документа преобразовать все изображения метафайлов в **F:Aspose.FileFormat.Png**. Обратите внимание — преобразование векторной графики в растровую уменьшает качество изображений.

 **Examples:** 

Показывает, как преобразовать WMF/EMF в PNG при загрузке документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Определяет, следует ли конвертировать метафайлы ( **F:Aspose.FileFormat.Wmf** или **F:Aspose.FileFormat.Emf**) в формат изображения **F:Aspose.FileFormat.Png**. |

### setConvertShapeToOfficeMath(boolean value) {#setConvertShapeToOfficeMath-boolean}
```
public void setConvertShapeToOfficeMath(boolean value)
```


Устанавливает, преобразовывать ли фигуры с EquationXML в объекты Office Math.

 **Examples:** 

Показывает, как преобразовать фигуры EquationXML в объекты Office Math.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Определяет, следует ли конвертировать фигуры с EquationXML в объекты Office Math. |

### setConvertSvgToEmf(boolean value) {#setConvertSvgToEmf-boolean}
```
public void setConvertSvgToEmf(boolean value)
```


Устанавливает значение, указывающее, следует ли конвертировать загруженные SVG‑изображения в формат EMF. Значение по умолчанию —  false , и, если возможно, загруженные SVG‑изображения сохраняются без конвертации.

 **Remarks:** 

Новые версии MS Word поддерживают SVG‑изображения напрямую. Если версия MS Word, указанная в параметрах загрузки, поддерживает SVG, Aspose.Words сохранит SVG‑изображения без преобразования. Если SVG не поддерживается, загруженные SVG‑изображения будут преобразованы в формат EMF.

Если же эта опция установлена в  true , Aspose.Words будет преобразовывать загруженные SVG‑изображения в EMF, даже если SVG‑изображения поддерживаются указанной версией MS Word.

 **Examples:** 

Показывает, как преобразовать объекты SVG в другой формат при сохранении HTML‑документов.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, указывающее, следует ли конвертировать загруженные SVG‑изображения в формат EMF. |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset}
```
public void setEncoding(Charset value)
```


Устанавливает кодировку, которая будет использоваться для загрузки HTML, TXT или CHM‑документа, если кодировка не указана внутри документа. Может быть  null . По умолчанию —  null .

 **Remarks:** 

Это свойство используется только при загрузке HTML, TXT или CHM‑документов.

Если кодировка не указана внутри документа и это свойство равно  null , система попытается автоматически определить кодировку.

 **Examples:** 

Показывает, как задать кодировку для открытия документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.nio.charset.Charset | Кодировка, которая будет использоваться для загрузки HTML, TXT или CHM‑документа, если кодировка не указана внутри документа. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Позволяет задавать параметры шрифтов документа.

 **Remarks:** 

При загрузке некоторых форматов Aspose.Words может потребоваться разрешить шрифты. Например, при загрузке HTML‑документов Aspose.Words может разрешать шрифты для выполнения резервирования шрифтов.

Если установлено в  null , будут использованы настройки статических шрифтов по умолчанию [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance).

Значение по умолчанию равно  null .

 **Examples:** 

Показывает, как назначать заменители шрифтов при загрузке.

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

Показывает, как применять настройки замены шрифтов при загрузке документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | Соответствующее значение [FontSettings](../../com.aspose.words/fontsettings/). |

### setIgnoreNoscriptElements(boolean value) {#setIgnoreNoscriptElements-boolean}
```
public void setIgnoreNoscriptElements(boolean value)
```


Устанавливает значение, указывающее, следует ли игнорировать  HTML‑элементы. Значение по умолчанию —  false .

 **Remarks:** 

Как и MS Word, Aspose.Words не поддерживает скрипты и по умолчанию загружает содержимое  элементов в получаемый документ. Однако в большинстве браузеров скрипты поддерживаются, и содержимое  не отображается. Установка этого свойства в  true  заставляет Aspose.Words игнорировать все  элементы и помогает создавать документы, более похожие на то, что видят в браузерах.

 **Examples:** 

Показывает, как игнорировать  HTML‑элементы.

```

 final String html = "\r\n\r\n\r\nNOSCRIPT\r\n\r\n\r\n\r\n\r\n Your browser does not support JavaScript!\r\n\r\n";

 HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
 htmlLoadOptions.setIgnoreNoscriptElements(ignoreNoscriptElements);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), htmlLoadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.IgnoreNoscriptElements.pdf");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, указывающее, следует ли игнорировать  HTML‑элементы. |

### setIgnoreOleData(boolean value) {#setIgnoreOleData-boolean}
```
public void setIgnoreOleData(boolean value)
```


Указывает, следует ли игнорировать данные OLE.

 **Remarks:** 

Игнорирование данных OLE может снизить потребление памяти и повысить производительность без потери данных в случае, когда целевой формат не поддерживает объекты OLE.

Значение по умолчанию — false.

 **Examples:** 

Показывает, как игнорировать данные OLE при загрузке.

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setLoadFormat(int value) {#setLoadFormat-int}
```
public void setLoadFormat(int value)
```


Указывает формат загружаемого документа. По умолчанию — [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO).

 **Remarks:** 

Рекомендуется указывать значение [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) и позволять Aspose.Words автоматически определять формат файла. Если вы знаете формат документа, который собираетесь загрузить, вы можете задать его явно, что слегка сократит время загрузки за счёт уменьшения накладных расходов на автоматическое определение формата. Если указанный явно формат окажется неверным, будет выполнено автоматическое определение и будет предпринята вторая попытка загрузить файл.

 **Examples:** 

Показывает, как указать базовый URI при открытии HTML‑документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее  int  значение. Значение должно быть одной из констант [LoadFormat](../../com.aspose.words/loadformat/). |

### setMswVersion(int value) {#setMswVersion-int}
```
public void setMswVersion(int value)
```


Позволяет указать, что процесс загрузки документа должен соответствовать определённой версии MS Word. Значение по умолчанию — [MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion/\#WORD-2019).

 **Remarks:** 

Разные версии Word могут несколько по‑разному обрабатывать определённые аспекты содержимого и форматирования документа во время загрузки, что может привести к небольшим различиям в объектной модели документа (Document Object Model).

 **Examples:** 

Показывает, как эмулировать процесс загрузки документа, соответствующий конкретной версии Microsoft Word.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее  int  значение. Значение должно быть одной из констант [MsWordVersion](../../com.aspose.words/mswordversion/). |

### setPassword(String value) {#setPassword-java.lang.String}
```
public void setPassword(String value)
```


Устанавливает пароль для открытия зашифрованного документа. Может быть  null  или пустой строкой. По умолчанию —  null .

 **Remarks:** 

Для открытия зашифрованного документа необходимо знать пароль. Если документ не зашифрован, установите значение  null  или пустую строку.

 **Examples:** 

Показывает, как подписать зашифрованный файл документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Пароль для открытия зашифрованного документа. |

### setPreferredControlType(int value) {#setPreferredControlType-int}
```
public void setPreferredControlType(int value)
```


Устанавливает предпочтительный тип узлов документа, которые будут представлять импортированные  и  элементы. Значение по умолчанию — [HtmlControlType.FORM\_FIELD](../../com.aspose.words/htmlcontroltype/\#FORM-FIELD). Примечание: обратите внимание, что установка этого свойства не гарантирует, что все импортированные элементы управления будут указанного типа. Если HTML‑элемент не может быть представлен узлами документа предпочтительного типа, Aspose.Words использует совместимый [HtmlControlType](../../com.aspose.words/htmlcontroltype/) для этого элемента. Примеры: показывает, как установить предпочтительный тип узлов документа, которые будут представлять импортированные  и  элементы.   final String html = "\\r\\n\\r\\n\\r\\n" + "item1\\r\\n\\r\\n\\r\\n\\r\\n"; HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions(); htmlLoadOptions.setPreferredControlType(HtmlControlType.STRUCTURED\_DOCUMENT\_TAG); Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF\_8)), htmlLoadOptions); NodeCollection nodes = doc.getChildNodes(NodeType.STRUCTURED\_DOCUMENT\_TAG, true); StructuredDocumentTag tag = (StructuredDocumentTag) nodes.get(0);

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Предпочтительный тип узлов документа, которые будут представлять импортированные  и  элементы. Значение должно быть одной из констант [HtmlControlType](../../com.aspose.words/htmlcontroltype/). |

### setPreserveIncludePictureField(boolean value) {#setPreserveIncludePictureField-boolean}
```
public void setPreserveIncludePictureField(boolean value)
```


Устанавливает, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию —  false .

 **Remarks:** 

По умолчанию поле INCLUDEPICTURE преобразуется в объект фигуры. Вы можете переопределить это, если требуется сохранить поле, например, если хотите обновлять его программно. Однако обратите внимание, что такой подход не распространён в Aspose.Words. Используйте его на свой страх и риск.

Одним из возможных сценариев использования может быть применение MERGEFIELD в качестве дочернего поля для динамического изменения пути к изображению. В этом случае необходимо сохранить INCLUDEPICTURE в модели.

 **Examples:** 

Показывает, как сохранять или отбрасывать поля INCLUDEPICTURE при загрузке документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Определяет, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. |

### setProgressCallback(IDocumentLoadingCallback value) {#setProgressCallback-com.aspose.words.IDocumentLoadingCallback}
```
public void setProgressCallback(IDocumentLoadingCallback value)
```


Вызывается во время загрузки документа и принимает данные о прогрессе загрузки.

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

Показывает, как уведомить пользователя, если загрузка документа превысила ожидаемое время.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) | Соответствующее значение [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/). |

### setRecoveryMode(int value) {#setRecoveryMode-int}
```
public void setRecoveryMode(int value)
```


Определяет, как документ должен обрабатываться при возникновении ошибок во время загрузки. Используйте это свойство, чтобы указать, должна ли система пытаться восстановить документ или следовать другому определённому поведению. Значение по умолчанию — [DocumentRecoveryMode.TRY\_RECOVER](../../com.aspose.words/documentrecoverymode/\#TRY-RECOVER).

 **Examples:** 

Показывает, как попытаться восстановить документ, если во время загрузки произошли ошибки.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее  int  значение. Значение должно быть одной из констант [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/). |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Позволяет контролировать, как внешние ресурсы (изображения, таблицы стилей) загружаются при импорте документа из HTML, MHTML.

 **Examples:** 

Показывает, как обрабатывать внешние ресурсы при загрузке HTML‑документов.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) | Соответствующее значение [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/). |

### setSupportFontFaceRules(boolean value) {#setSupportFontFaceRules-boolean}
```
public void setSupportFontFaceRules(boolean value)
```


Устанавливает значение, указывающее, следует ли поддерживать правила @font-face и загружать объявленные шрифты. Значение по умолчанию —  false .

 **Remarks:** 

Если эта опция включена, шрифты, объявленные в правилах @font-face, загружаются и встраиваются в определения шрифтов получаемого документа (см. [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos)). Это делает загруженные шрифты доступными для рендеринга, но не включает автоматическое встраивание шрифтов при сохранении. Чтобы сохранить документ с загруженными шрифтами, свойство [FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection/\#getEmbedTrueTypeFonts) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection/\#setEmbedTrueTypeFonts-boolean) коллекции [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase/\#getFontInfos) должно быть установлено в true.

Поддерживаемые форматы шрифтов: TTF, EOT и WOFF.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, указывающее, следует ли поддерживать правила @font-face и загружать объявленные шрифты. |

### setSupportVml(boolean value) {#setSupportVml-boolean}
```
public void setSupportVml(boolean value)
```


Устанавливает значение, указывающее, поддерживать ли VML‑изображения.

 **Examples:** 

Показывает, как поддерживать условные комментарии при загрузке HTML‑документа.

```

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();

 // If the value is true, then we take VML code into account while parsing the loaded document.
 loadOptions.setSupportVml(supportVml);

 // This document contains a JPEG image within "
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Значение, указывающее, следует ли поддерживать изображения VML. |

### setTempFolder(String value) {#setTempFolder-java.lang.String}
```
public void setTempFolder(String value)
```


Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство равно null, и временные файлы не используются.

 **Remarks:** 

Папка должна существовать и быть доступной для записи, иначе будет выброшено исключение.

Aspose.Words автоматически удаляет все временные файлы после завершения чтения.

 **Examples:** 

Показывает, как загрузить документ, используя временные файлы.

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

Показывает, как использовать жёсткий диск вместо памяти при загрузке документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

### setUpdateDirtyFields(boolean value) {#setUpdateDirtyFields-boolean}
```
public void setUpdateDirtyFields(boolean value)
```


Указывает, обновлять ли поля с атрибутом  dirty .

 **Examples:** 

Показывает, как использовать специальное свойство для обновления результата поля.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Соответствующее  boolean  значение. |

### setUseSystemLcid(boolean value) {#setUseSystemLcid-boolean}
```
public void setUseSystemLcid(boolean value)
```


Устанавливает, использовать ли значение LCID, полученное из реестра Windows, для определения полей по умолчанию в настройках страницы.

 **Remarks:** 

Если установить в true, то эмулируется поведение MS Word, которое берёт значение LCID из реестра Windows.

Значение по умолчанию — false.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | boolean | Определяет, использовать ли значение LCID, полученное из реестра Windows, для определения полей по умолчанию при настройке страницы. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Вызывается во время операции загрузки, когда обнаруживается проблема, которая может привести к потере точности данных или форматирования.

 **Examples:** 

Показывает, как выводить и сохранять предупреждения, возникающие при загрузке документа.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | Соответствующее значение [IWarningCallback](../../com.aspose.words/iwarningcallback/). |

### setWebRequestTimeout(int value) {#setWebRequestTimeout-int}
```
public void setWebRequestTimeout(int value)
```


Количество миллисекунд ожидания до истечения времени веб‑запроса. Значение по умолчанию — 100000 миллисекунд (100 секунд).

 **Remarks:** 

Количество миллисекунд, которое Aspose.Words ждёт ответа при загрузке внешних ресурсов (изображений, таблиц стилей), связанных в HTML‑ и MHTML‑документах.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | int | Соответствующее  int  значение. |

