---
title: "MarkdownLoadOptions"
linktitle: "MarkdownLoadOptions"
second_title: "Aspose.Words for Java"
description: "允许在 Java 中将 LoadFormat.MARKDOWN 文档加载到 Document 对象时指定其他选项。"
type: docs
weight: 454
url: /zh/java/com.aspose.words/markdownloadoptions/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions/)
```
public class MarkdownLoadOptions extends LoadOptions
```

允许在加载 [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN) 文档到 [Document](../../com.aspose.words/document/) 对象时指定其他选项。

 **Examples:** 

展示如何在加载文档时保留空行。

```

 String mdText = MessageFormat.format("{0}Line1{0}{0}Line2{0}{0}", System.lineSeparator());

 MarkdownLoadOptions loadOptions = new MarkdownLoadOptions();
 loadOptions.setPreserveEmptyLines(true);
 Document doc = new Document(new ByteArrayInputStream(mdText.getBytes()), loadOptions);

 Assert.assertEquals("\rLine1\r\rLine2\r\f", doc.getText());
 
```
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [MarkdownLoadOptions()](#MarkdownLoadOptions) | 初始化 [MarkdownLoadOptions](../../com.aspose.words/markdownloadoptions/) 类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | 确定指定对象的值是否等于当前对象。 |
| [getBaseUri()](#getBaseUri) | 获取将在需要时用于将文档中找到的相对 URI 解析为绝对 URI 的字符串。 |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng) | 获取是否将元文件（**F:Aspose.FileFormat.Wmf** 或 **F:Aspose.FileFormat.Emf**）图像转换为 **F:Aspose.FileFormat.Png** 图像格式。 |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath) | 获取是否将带有 EquationXML 的形状转换为 Office Math 对象。 |
| [getEncoding()](#getEncoding) | 获取在文档内部未指定编码时，用于加载 HTML、TXT 或 CHM 文档的编码。 |
| [getFontSettings()](#getFontSettings) | 允许指定文档字体设置。 |
| [getIgnoreOleData()](#getIgnoreOleData) | 指定是否忽略 OLE 数据。 |
| [getImportUnderlineFormatting()](#getImportUnderlineFormatting) | 获取一个布尔值，指示是否将两个加号 "++" 的序列识别为下划线文本格式。 |
| [getLanguagePreferences()](#getLanguagePreferences) | 获取在加载文档时将使用的语言首选项。 |
| [getLoadFormat()](#getLoadFormat) | 指定要加载的文档的格式。 |
| [getMswVersion()](#getMswVersion) | 允许指定文档加载过程应匹配特定的 MS Word 版本。 |
| [getPassword()](#getPassword) | 获取打开加密文档的密码。 |
| [getPreserveEmptyLines()](#getPreserveEmptyLines) | 获取一个布尔值，指示在加载 [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN) 文档时是否保留空行。 |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField) | 获取在读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。 |
| [getProgressCallback()](#getProgressCallback) | 在加载文档期间调用，并接受有关加载进度的数据。 |
| [getRecoveryMode()](#getRecoveryMode) | 定义在加载期间出现错误时文档应如何处理。 |
| [getResourceLoadingCallback()](#getResourceLoadingCallback) | 允许控制在文档从 HTML、MHTML 导入时外部资源（图像、样式表）的加载方式。 |
| [getSoftLineBreakCharacter()](#getSoftLineBreakCharacter) | 获取表示软换行的字符值。 |
| [getTempFolder()](#getTempFolder) | 允许在读取文档时使用临时文件。 |
| [getUpdateDirtyFields()](#getUpdateDirtyFields) | 指定是否使用 dirty 属性更新字段。 |
| [getUseSystemLcid()](#getUseSystemLcid) | 获取是否使用从 Windows 注册表获取的 LCID 值来确定页面设置的默认边距。 |
| [getWarningCallback()](#getWarningCallback) | 在加载操作期间调用，当检测到可能导致数据或格式保真度丢失的问题时。 |
| [setBaseUri(String value)](#setBaseUri-java.lang.String) | 设置将在需要时用于将文档中发现的相对 URI 解析为绝对 URI 的字符串。 |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean) | 设置是否将元文件（**F:Aspose.FileFormat.Wmf** 或 **F:Aspose.FileFormat.Emf**）图像转换为 **F:Aspose.FileFormat.Png** 图像格式。 |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean) | 设置是否将带有 EquationXML 的形状转换为 Office Math 对象。 |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset) | 设置在文档内部未指定编码时，用于加载 HTML、TXT 或 CHM 文档的编码。 |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | 允许指定文档字体设置。 |
| [setIgnoreOleData(boolean value)](#setIgnoreOleData-boolean) | 指定是否忽略 OLE 数据。 |
| [setImportUnderlineFormatting(boolean value)](#setImportUnderlineFormatting-boolean) | 设置一个布尔值，指示是否将两个加号字符 "++" 的序列识别为下划线文本格式。 |
| [setLoadFormat(int value)](#setLoadFormat-int) | 指定要加载的文档的格式。 |
| [setMswVersion(int value)](#setMswVersion-int) | 允许指定文档加载过程应匹配特定的 MS Word 版本。 |
| [setPassword(String value)](#setPassword-java.lang.String) | 设置打开加密文档的密码。 |
| [setPreserveEmptyLines(boolean value)](#setPreserveEmptyLines-boolean) | 设置一个布尔值，指示在加载 [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN) 文档时是否保留空行。 |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean) | 设置在读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。 |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback) | 在加载文档期间调用，并接受有关加载进度的数据。 |
| [setRecoveryMode(int value)](#setRecoveryMode-int) | 定义在加载期间出现错误时文档应如何处理。 |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback) | 允许控制在文档从 HTML、MHTML 导入时外部资源（图像、样式表）的加载方式。 |
| [setSoftLineBreakCharacter(char value)](#setSoftLineBreakCharacter-char) | 设置表示软换行的字符值。 |
| [setTempFolder(String value)](#setTempFolder-java.lang.String) | 允许在读取文档时使用临时文件。 |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean) | 指定是否使用 dirty 属性更新字段。 |
| [setUseSystemLcid(boolean value)](#setUseSystemLcid-boolean) | 设置是否使用从 Windows 注册表获取的 LCID 值来确定页面设置的默认边距。 |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | 在加载操作期间调用，当检测到可能导致数据或格式保真度丢失的问题时。 |
### MarkdownLoadOptions() {#MarkdownLoadOptions}
```
public MarkdownLoadOptions()
```


初始化 [MarkdownLoadOptions](../../com.aspose.words/markdownloadoptions/) 类的新实例。

 **Remarks:** 

自动将 [LoadFormat](../../com.aspose.words/loadformat/) 设置为 [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN)。

 **Examples:** 

展示如何在加载文档时保留空行。

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


确定指定对象的值是否等于当前对象。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getBaseUri() {#getBaseUri}
```
public String getBaseUri()
```


获取将在需要时用于将文档中发现的相对 URI 解析为绝对 URI 的字符串。可以为  null  或空字符串。默认是  null 。

 **Remarks:** 

此属性用于在以下情况下将相对 URI 解析为绝对 URI：

1.  当从流加载 HTML 文档且文档包含具有相对 URI 的图像且在 BASE HTML 元素中未指定基准 URI 时。
2.  当将文档保存为 PDF 等格式时，检索使用相对 URI 链接的图像，以便将这些图像保存到输出文档中。

 **Examples:** 

展示如何使用基准 URI 从流中打开带有图像的 HTML 文档。

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
java.lang.String - 将用于在需要时将文档中找到的相对 URI 解析为绝对 URI 的字符串。
### getConvertMetafilesToPng() {#getConvertMetafilesToPng}
```
public boolean getConvertMetafilesToPng()
```


获取是否将元文件（**F:Aspose.FileFormat.Wmf** 或 **F:Aspose.FileFormat.Emf**）图像转换为 **F:Aspose.FileFormat.Png** 图像格式。

 **Remarks:** 

元文件（ **F:Aspose.FileFormat.Wmf** 或 **F:Aspose.FileFormat.Emf**）是一种未压缩的图像格式，有时需要大量 RAM 来保存和处理文档。此选项允许在文档加载时将所有元文件图像转换为 **F:Aspose.FileFormat.Png**。请注意——将矢量图形转换为光栅图会降低图像质量。

 **Examples:** 

展示如何在加载文档时将 WMF/EMF 转换为 PNG。

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
boolean - 是否将元文件（ **F:Aspose.FileFormat.Wmf** 或 **F:Aspose.FileFormat.Emf**）图像转换为 **F:Aspose.FileFormat.Png** 图像格式。
### getConvertShapeToOfficeMath() {#getConvertShapeToOfficeMath}
```
public boolean getConvertShapeToOfficeMath()
```


获取是否将带有 EquationXML 的形状转换为 Office Math 对象。

 **Examples:** 

展示如何将 EquationXML 形状转换为 Office Math 对象。

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
boolean - 是否将带有 EquationXML 的形状转换为 Office Math 对象。
### getEncoding() {#getEncoding}
```
public Charset getEncoding()
```


获取在文档内部未指定编码时用于加载 HTML、TXT 或 CHM 文档的编码。可以为 null。默认是 null。

 **Remarks:** 

此属性仅在加载 HTML、TXT 或 CHM 文档时使用。

如果文档内部未指定编码且此属性为 null，则系统将尝试自动检测编码。

 **Examples:** 

展示如何设置打开文档时使用的编码。

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
java.nio.charset.Charset - 在文档内部未指定编码时用于加载 HTML、TXT 或 CHM 文档的编码。
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


允许指定文档字体设置。

 **Remarks:** 

加载某些格式时，Aspose.Words 可能需要解析字体。例如，加载 HTML 文档时，Aspose.Words 可能解析字体以执行字体回退。

如果设置为 null，将使用默认的静态字体设置 [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance)。

默认值为 null。

 **Examples:** 

展示如何在加载期间指定字体替代。

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

展示如何在加载文档时应用字体替代设置。

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


指定是否忽略 OLE 数据。

 **Remarks:** 

忽略 OLE 数据可能在目标格式不支持 OLE 对象的情况下减少内存消耗并提升性能，且不会导致数据丢失。

默认值为 false。

 **Examples:** 

展示如何在加载时忽略 OLE 数据。

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Returns:**
boolean - 相应的 boolean 值。
### getImportUnderlineFormatting() {#getImportUnderlineFormatting}
```
public boolean getImportUnderlineFormatting()
```


获取一个布尔值，指示是否将两个加号字符 \"++\" 的序列识别为下划线文本格式。默认值为 false。

 **Examples:** 

展示如何将加号字符 \"++\" 识别为下划线文本格式。

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
boolean - 一个布尔值，指示是否将两个加号字符 \"++\" 的序列识别为下划线文本格式。
### getLanguagePreferences() {#getLanguagePreferences}
```
public LanguagePreferences getLanguagePreferences()
```


获取在加载文档时将使用的语言首选项。

 **Examples:** 

展示如何在加载文档时应用语言偏好设置。

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


指定要加载的文档格式。默认是 [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO)。

 **Remarks:** 

建议您指定 [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) 值，让 Aspose.Words 自动检测文件格式。如果您已知即将加载的文档格式，可以显式指定该格式，这将略微减少因自动检测格式而产生的开销，从而缩短加载时间。如果您指定了显式的加载格式但结果错误，将会调用自动检测并进行第二次加载尝试。

 **Examples:** 

展示如何在打开 html 文档时指定基础 URI。

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
int - 对应的  int  值。返回的值是 [LoadFormat](../../com.aspose.words/loadformat/) 常量之一。
### getMswVersion() {#getMswVersion}
```
public int getMswVersion()
```


允许指定文档加载过程应匹配特定的 MS Word 版本。默认值是 [MsWordVersion.WORD\\_2019](../../com.aspose.words/mswordversion/\\#WORD-2019)。

 **Remarks:** 

不同的 Word 版本在加载过程中可能会略有不同地处理文档内容和格式的某些方面，这可能导致文档对象模型出现细微差异。

 **Examples:** 

展示如何在文档加载期间模拟特定 Microsoft Word 版本的加载过程。

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
int - 对应的  int  值。返回的值是 [MsWordVersion](../../com.aspose.words/mswordversion/) 常量之一。
### getPassword() {#getPassword}
```
public String getPassword()
```


获取打开加密文档的密码。可以为  null  或空字符串。默认是  null 。

 **Remarks:** 

您需要知道密码才能打开加密文档。如果文档未加密，请将其设置为  null  或空字符串。

 **Examples:** 

展示如何对加密文档文件进行签名。

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
java.lang.String - 打开加密文档的密码。
### getPreserveEmptyLines() {#getPreserveEmptyLines}
```
public boolean getPreserveEmptyLines()
```


获取一个布尔值，指示在加载 [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\\#MARKDOWN) 文档时是否保留空行。默认值是  false 。

通常，Markdown 中块级元素之间的空行会被忽略。文档开头和结尾的空行也会被忽略。此选项允许导入这些空行。

 **Examples:** 

展示如何在加载文档时保留空行。

```

 String mdText = MessageFormat.format("{0}Line1{0}{0}Line2{0}{0}", System.lineSeparator());

 MarkdownLoadOptions loadOptions = new MarkdownLoadOptions();
 loadOptions.setPreserveEmptyLines(true);
 Document doc = new Document(new ByteArrayInputStream(mdText.getBytes()), loadOptions);

 Assert.assertEquals("\rLine1\r\rLine2\r\f", doc.getText());
 
```

**Returns:**
boolean - 一个布尔值，指示在加载 [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\\#MARKDOWN) 文档时是否保留空行。
### getPreserveIncludePictureField() {#getPreserveIncludePictureField}
```
public boolean getPreserveIncludePictureField()
```


获取在读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。默认值是  false 。

 **Remarks:** 

默认情况下，INCLUDEPICTURE 字段会被转换为形状对象。如果需要保留该字段，例如希望以编程方式更新它，可以覆盖此行为。请注意，此方法在 Aspose.Words 中并不常见。使用需自行承担风险。

一种可能的用例是使用 MERGEFIELD 作为子字段来动态更改图片的源路径。在这种情况下，您需要在模型中保留 INCLUDEPICTURE。

 **Examples:** 

展示如何在加载文档时保留或丢弃 INCLUDEPICTURE 字段。

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
boolean - 在读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。
### getProgressCallback() {#getProgressCallback}
```
public IDocumentLoadingCallback getProgressCallback()
```


在加载文档期间调用，并接受有关加载进度的数据。

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

展示如何在文档加载超过预期时间时通知用户。

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


定义在加载期间出现错误时应如何处理文档。使用此属性指定系统是尝试恢复文档还是遵循其他定义的行为。默认值是 [DocumentRecoveryMode.TRY\\_RECOVER](../../com.aspose.words/documentrecoverymode/\\#TRY-RECOVER)。

 **Examples:** 

展示如何在加载期间出现错误时尝试恢复文档。

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Returns:**
int - 对应的  int  值。返回的值是 [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/) 常量之一。
### getResourceLoadingCallback() {#getResourceLoadingCallback}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


允许控制在文档从 HTML、MHTML 导入时外部资源（图像、样式表）的加载方式。

 **Examples:** 

展示如何在加载 Html 文档时处理外部资源。

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


获取表示软换行的字符值。默认值是  SPACE (U+0020) 。

 **Remarks:** 

注意，将此选项设置为 [ControlChar.LINE\\_BREAK\\_CHAR](../../com.aspose.words/controlchar/\\#LINE-BREAK-CHAR) 可将软换行加载为硬换行。

 **Examples:** 

展示如何设置软换行字符。

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
char - 表示软换行的字符值。
### getTempFolder() {#getTempFolder}
```
public String getTempFolder()
```


允许在读取文档时使用临时文件。默认情况下，此属性为  null ，不使用临时文件。

 **Remarks:** 

文件夹必须存在且可写，否则将抛出异常。

Aspose.Words 在读取完成后会自动删除所有临时文件。

 **Examples:** 

展示如何使用临时文件加载文档。

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

展示在加载文档时如何使用硬盘而不是内存。

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
java.lang.String - 相应的 java.lang.String 值。
### getUpdateDirtyFields() {#getUpdateDirtyFields}
```
public boolean getUpdateDirtyFields()
```


指定是否使用 dirty 属性更新字段。

 **Examples:** 

展示如何使用特殊属性来更新字段结果。

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
boolean - 相应的 boolean 值。
### getUseSystemLcid() {#getUseSystemLcid}
```
public boolean getUseSystemLcid()
```


获取是否使用从 Windows 注册表获取的 LCID 值来确定页面设置的默认边距。

 **Remarks:** 

如果设置为  true ，则模拟 MS Word 行为，从 Windows 注册表获取 LCID 值。

默认值为 false。

**Returns:**
boolean - 是否使用从 Windows 注册表获取的 LCID 值来确定页面设置的默认边距。
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


在加载操作期间调用，当检测到可能导致数据或格式保真度丢失的问题时。

 **Examples:** 

展示如何打印并存储文档加载期间出现的警告。

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


设置将在需要时用于将文档中找到的相对 URI 解析为绝对 URI 的字符串。可以为  null  或空字符串。默认是  null 。

 **Remarks:** 

此属性用于在以下情况下将相对 URI 解析为绝对 URI：

1.  当从流加载 HTML 文档且文档包含具有相对 URI 的图像且在 BASE HTML 元素中未指定基准 URI 时。
2.  当将文档保存为 PDF 等格式时，检索使用相对 URI 链接的图像，以便将这些图像保存到输出文档中。

 **Examples:** 

展示如何使用基准 URI 从流中打开带有图像的 HTML 文档。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 将在需要时用于将文档中找到的相对 URI 解析为绝对 URI 的字符串。 |

### setConvertMetafilesToPng(boolean value) {#setConvertMetafilesToPng-boolean}
```
public void setConvertMetafilesToPng(boolean value)
```


设置是否将元文件（**F:Aspose.FileFormat.Wmf** 或 **F:Aspose.FileFormat.Emf**）图像转换为 **F:Aspose.FileFormat.Png** 图像格式。

 **Remarks:** 

元文件（ **F:Aspose.FileFormat.Wmf** 或 **F:Aspose.FileFormat.Emf**）是一种未压缩的图像格式，有时需要大量 RAM 来保存和处理文档。此选项允许在文档加载时将所有元文件图像转换为 **F:Aspose.FileFormat.Png**。请注意——将矢量图形转换为光栅图会降低图像质量。

 **Examples:** 

展示如何在加载文档时将 WMF/EMF 转换为 PNG。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否将元文件（ **F:Aspose.FileFormat.Wmf** 或 **F:Aspose.FileFormat.Emf**）图像转换为 **F:Aspose.FileFormat.Png** 图像格式。 |

### setConvertShapeToOfficeMath(boolean value) {#setConvertShapeToOfficeMath-boolean}
```
public void setConvertShapeToOfficeMath(boolean value)
```


设置是否将带有 EquationXML 的形状转换为 Office Math 对象。

 **Examples:** 

展示如何将 EquationXML 形状转换为 Office Math 对象。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否将带有 EquationXML 的形状转换为 Office Math 对象。 |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset}
```
public void setEncoding(Charset value)
```


设置在文档内部未指定编码时用于加载 HTML、TXT 或 CHM 文档的编码。可以为  null 。默认是  null 。

 **Remarks:** 

此属性仅在加载 HTML、TXT 或 CHM 文档时使用。

如果文档内部未指定编码且此属性为 null，则系统将尝试自动检测编码。

 **Examples:** 

展示如何设置打开文档时使用的编码。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.nio.charset.Charset | 在文档内部未指定编码时，用于加载 HTML、TXT 或 CHM 文档的编码。 |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


允许指定文档字体设置。

 **Remarks:** 

加载某些格式时，Aspose.Words 可能需要解析字体。例如，加载 HTML 文档时，Aspose.Words 可能解析字体以执行字体回退。

如果设置为 null，将使用默认的静态字体设置 [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance)。

默认值为 null。

 **Examples:** 

展示如何在加载期间指定字体替代。

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

展示如何在加载文档时应用字体替代设置。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | 对应的[FontSettings](../../com.aspose.words/fontsettings/)值。 |

### setIgnoreOleData(boolean value) {#setIgnoreOleData-boolean}
```
public void setIgnoreOleData(boolean value)
```


指定是否忽略 OLE 数据。

 **Remarks:** 

忽略 OLE 数据可能在目标格式不支持 OLE 对象的情况下减少内存消耗并提升性能，且不会导致数据丢失。

默认值为 false。

 **Examples:** 

展示如何在加载时忽略 OLE 数据。

```

 // Ignoring OLE data may reduce memory consumption and increase performance
 // without data lost in a case when destination format does not support OLE objects.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setIgnoreOleData(true);
 Document doc = new Document(getMyDir() + "OLE objects.docx", loadOptions);

 doc.save(getArtifactsDir() + "LoadOptions.IgnoreOleData.docx");
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 相应的 boolean 值。 |

### setImportUnderlineFormatting(boolean value) {#setImportUnderlineFormatting-boolean}
```
public void setImportUnderlineFormatting(boolean value)
```


设置一个布尔值，指示是否将两个加号字符 "++" 的序列识别为下划线文本格式。默认值为  false 。

 **Examples:** 

展示如何将加号字符 \"++\" 识别为下划线文本格式。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示是否将两个加号字符 "++" 的序列识别为下划线文本格式。 |

### setLoadFormat(int value) {#setLoadFormat-int}
```
public void setLoadFormat(int value)
```


指定要加载的文档格式。默认是 [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO)。

 **Remarks:** 

建议您指定 [LoadFormat.AUTO](../../com.aspose.words/loadformat/\#AUTO) 值，让 Aspose.Words 自动检测文件格式。如果您已知即将加载的文档格式，可以显式指定该格式，这将略微减少因自动检测格式而产生的开销，从而缩短加载时间。如果您指定了显式的加载格式但结果错误，将会调用自动检测并进行第二次加载尝试。

 **Examples:** 

展示如何在打开 html 文档时指定基础 URI。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的  int  值。该值必须是 [LoadFormat](../../com.aspose.words/loadformat/) 常量之一。 |

### setMswVersion(int value) {#setMswVersion-int}
```
public void setMswVersion(int value)
```


允许指定文档加载过程应匹配特定的 MS Word 版本。默认值是 [MsWordVersion.WORD\\_2019](../../com.aspose.words/mswordversion/\\#WORD-2019)。

 **Remarks:** 

不同的 Word 版本在加载过程中可能会略有不同地处理文档内容和格式的某些方面，这可能导致文档对象模型出现细微差异。

 **Examples:** 

展示如何在文档加载期间模拟特定 Microsoft Word 版本的加载过程。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的  int  值。该值必须是 [MsWordVersion](../../com.aspose.words/mswordversion/) 常量之一。 |

### setPassword(String value) {#setPassword-java.lang.String}
```
public void setPassword(String value)
```


设置打开加密文档的密码。可以为  null  或空字符串。默认是  null 。

 **Remarks:** 

您需要知道密码才能打开加密文档。如果文档未加密，请将其设置为  null  或空字符串。

 **Examples:** 

展示如何对加密文档文件进行签名。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 打开加密文档的密码。 |

### setPreserveEmptyLines(boolean value) {#setPreserveEmptyLines-boolean}
```
public void setPreserveEmptyLines(boolean value)
```


设置一个布尔值，指示在加载 [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN) 文档时是否保留空行。默认值为  false 。

通常，Markdown 中块级元素之间的空行会被忽略。文档开头和结尾的空行也会被忽略。此选项允许导入这些空行。

 **Examples:** 

展示如何在加载文档时保留空行。

```

 String mdText = MessageFormat.format("{0}Line1{0}{0}Line2{0}{0}", System.lineSeparator());

 MarkdownLoadOptions loadOptions = new MarkdownLoadOptions();
 loadOptions.setPreserveEmptyLines(true);
 Document doc = new Document(new ByteArrayInputStream(mdText.getBytes()), loadOptions);

 Assert.assertEquals("\rLine1\r\rLine2\r\f", doc.getText());
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示在加载 [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN) 文档时是否保留空行。 |

### setPreserveIncludePictureField(boolean value) {#setPreserveIncludePictureField-boolean}
```
public void setPreserveIncludePictureField(boolean value)
```


设置在读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。默认值为 false。

 **Remarks:** 

默认情况下，INCLUDEPICTURE 字段会被转换为形状对象。如果需要保留该字段，例如希望以编程方式更新它，可以覆盖此行为。请注意，此方法在 Aspose.Words 中并不常见。使用需自行承担风险。

一种可能的用例是使用 MERGEFIELD 作为子字段来动态更改图片的源路径。在这种情况下，您需要在模型中保留 INCLUDEPICTURE。

 **Examples:** 

展示如何在加载文档时保留或丢弃 INCLUDEPICTURE 字段。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 在读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。 |

### setProgressCallback(IDocumentLoadingCallback value) {#setProgressCallback-com.aspose.words.IDocumentLoadingCallback}
```
public void setProgressCallback(IDocumentLoadingCallback value)
```


在加载文档期间调用，并接受有关加载进度的数据。

 **Remarks:** 

[LoadFormat.DOCX](../../com.aspose.words/loadformat/\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat/\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat/\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat/\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat/\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat/\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat/\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat/\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat/\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat/\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat/\#OTT) formats supported.

 **Examples:** 

展示如何在文档加载超过预期时间时通知用户。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) | 对应的 [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback/) 值。 |

### setRecoveryMode(int value) {#setRecoveryMode-int}
```
public void setRecoveryMode(int value)
```


定义在加载期间出现错误时应如何处理文档。使用此属性指定系统是尝试恢复文档还是遵循其他定义的行为。默认值是 [DocumentRecoveryMode.TRY\\_RECOVER](../../com.aspose.words/documentrecoverymode/\\#TRY-RECOVER)。

 **Examples:** 

展示如何在加载期间出现错误时尝试恢复文档。

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是 [DocumentRecoveryMode](../../com.aspose.words/documentrecoverymode/) 常量之一。 |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


允许控制在文档从 HTML、MHTML 导入时外部资源（图像、样式表）的加载方式。

 **Examples:** 

展示如何在加载 Html 文档时处理外部资源。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) | 对应的 [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) 值。 |

### setSoftLineBreakCharacter(char value) {#setSoftLineBreakCharacter-char}
```
public void setSoftLineBreakCharacter(char value)
```


设置表示软换行的字符值。默认值为 SPACE (U+0020)。

 **Remarks:** 

注意，将此选项设置为 [ControlChar.LINE\\_BREAK\\_CHAR](../../com.aspose.words/controlchar/\\#LINE-BREAK-CHAR) 可将软换行加载为硬换行。

 **Examples:** 

展示如何设置软换行字符。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | char | 表示软换行的字符值。 |

### setTempFolder(String value) {#setTempFolder-java.lang.String}
```
public void setTempFolder(String value)
```


允许在读取文档时使用临时文件。默认情况下，此属性为  null ，不使用临时文件。

 **Remarks:** 

文件夹必须存在且可写，否则将抛出异常。

Aspose.Words 在读取完成后会自动删除所有临时文件。

 **Examples:** 

展示如何使用临时文件加载文档。

```

 // Note that such an approach can reduce memory usage but degrades speed.
 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setTempFolder("C:\\TempFolder\\");

 // Ensure that the directory exists and load.
 new File(loadOptions.getTempFolder()).mkdir();

 Document doc = new Document(getMyDir() + "Document.docx", loadOptions);
 
```

展示在加载文档时如何使用硬盘而不是内存。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setUpdateDirtyFields(boolean value) {#setUpdateDirtyFields-boolean}
```
public void setUpdateDirtyFields(boolean value)
```


指定是否使用 dirty 属性更新字段。

 **Examples:** 

展示如何使用特殊属性来更新字段结果。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 相应的 boolean 值。 |

### setUseSystemLcid(boolean value) {#setUseSystemLcid-boolean}
```
public void setUseSystemLcid(boolean value)
```


设置是否使用从 Windows 注册表获取的 LCID 值来确定页面设置的默认边距。

 **Remarks:** 

如果设置为  true ，则模拟 MS Word 行为，从 Windows 注册表获取 LCID 值。

默认值为 false。

**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否使用从 Windows 注册表获取的 LCID 值来确定页面设置的默认边距。 |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


在加载操作期间调用，当检测到可能导致数据或格式保真度丢失的问题时。

 **Examples:** 

展示如何打印并存储文档加载期间出现的警告。

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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | 对应的[IWarningCallback](../../com.aspose.words/iwarningcallback/)值。 |

