---
title: HtmlLoadOptions
second_title: Aspose.Words for Java API 参考
description: 允许在将 HTML 文档加载到对象时指定其他选项。
type: docs
weight: 328
url: /zh/java/com.aspose.words/htmlloadoptions/
---

**遗产：**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions)
```
public class HtmlLoadOptions extends LoadOptions
```

允许在将 HTML 文档加载到[Document](../../com.aspose.words/document)目的。

要了解更多信息，请访问**Specify Load Options**文档文章。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [HtmlLoadOptions()](#HtmlLoadOptions--) | 使用默认值初始化此类的新实例。 |
| [HtmlLoadOptions(String password)](#HtmlLoadOptions-java.lang.String-) | 使用指定密码初始化此类的新实例以加载加密文档的快捷方式。 |
| [HtmlLoadOptions(int loadFormat, String password, String baseUri)](#HtmlLoadOptions-int-java.lang.String-java.lang.String-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBaseUri()](#getBaseUri--) | 获取将用于在需要时将文档中找到的相对 URI 解析为绝对 URI 的字符串。 |
| [getBlockImportMode()](#getBlockImportMode--) | 获取一个值，该值指定如何导入块级元素的属性。 |
| [getClass()](#getClass--) |  |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng--) | 获取是否转换图元文件（**F:Aspose.FileFormat.Wmf**或者**F:Aspose.FileFormat.Emf** ) 图片到**F:Aspose.FileFormat.Png**图像格式。 |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath--) | 获取是否将带有 EquationXML 的形状转换为 Office Math 对象。 |
| [getConvertSvgToEmf()](#getConvertSvgToEmf--) | 获取一个值，该值指示是否将加载的 SVG 图像转换为 EMF 格式。 |
| [getEncoding()](#getEncoding--) | 如果文档中未指定编码，则获取将用于加载 HTML、TXT 或 CHM 文档的编码。 |
| [getFontSettings()](#getFontSettings--) | 允许指定文档字体设置。 |
| [getIgnoreNoscriptElements()](#getIgnoreNoscriptElements--) | 获取一个值，该值指示是否忽略 HTML 元素。 |
| [getLanguagePreferences()](#getLanguagePreferences--) | 获取将在加载文档时使用的语言首选项。 |
| [getLoadFormat()](#getLoadFormat--) | 指定要加载的文档的格式。 |
| [getMswVersion()](#getMswVersion--) | 允许指定文档加载过程应匹配特定的 MS Word 版本。 |
| [getPassword()](#getPassword--) | 获取打开加密文档的密码。 |
| [getPreferredControlType()](#getPreferredControlType--) | 获取将表示导入和元素的首选类型的文档节点。 |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField--) | 获取在阅读 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。 |
| [getProgressCallback()](#getProgressCallback--) | 在加载文档期间调用并接受有关加载进度的数据。 |
| [getResourceLoadingCallback()](#getResourceLoadingCallback--) | 允许控制从 HTML、MHTML 导入文档时如何加载外部资源（图像、样式表）。 |
| [getSupportVml()](#getSupportVml--) | 获取一个值，该值指示是否支持 VML 图像。 |
| [getTempFolder()](#getTempFolder--) | 允许在阅读文档时使用临时文件。 |
| [getUpdateDirtyFields()](#getUpdateDirtyFields--) | 指定是否更新具有脏属性的字段。 |
| [getWarningCallback()](#getWarningCallback--) | 在加载操作期间调用，当检测到可能导致数据或格式保真度丢失的问题时调用。 |
| [getWebRequestTimeout()](#getWebRequestTimeout--) | Web 请求超时前等待的毫秒数。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBaseUri(String value)](#setBaseUri-java.lang.String-) | 设置将用于在需要时将文档中找到的相对 URI 解析为绝对 URI 的字符串。 |
| [setBlockImportMode(int value)](#setBlockImportMode-int-) | 设置一个值，指定如何导入块级元素的属性。 |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean-) | 设置是否转换图元文件（**F:Aspose.FileFormat.Wmf**或者**F:Aspose.FileFormat.Emf** ) 图片到**F:Aspose.FileFormat.Png**图像格式。 |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean-) | 设置是否将带有 EquationXML 的形状转换为 Office Math 对象。 |
| [setConvertSvgToEmf(boolean value)](#setConvertSvgToEmf-boolean-) | 设置一个值，指示是否将加载的 SVG 图像转换为 EMF 格式。 |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset-) | 如果文档中未指定编码，则设置将用于加载 HTML、TXT 或 CHM 文档的编码。 |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings-) | 允许指定文档字体设置。 |
| [setIgnoreNoscriptElements(boolean value)](#setIgnoreNoscriptElements-boolean-) | 设置一个值，指示是否忽略 HTML 元素。 |
| [setLoadFormat(int value)](#setLoadFormat-int-) | 指定要加载的文档的格式。 |
| [setMswVersion(int value)](#setMswVersion-int-) | 允许指定文档加载过程应匹配特定的 MS Word 版本。 |
| [setPassword(String value)](#setPassword-java.lang.String-) | 设置打开加密文档的密码。 |
| [setPreferredControlType(int value)](#setPreferredControlType-int-) | 设置将代表导入和元素的首选文档节点类型。 |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean-) | 设置在阅读 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。 |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback-) | 在加载文档期间调用并接受有关加载进度的数据。 |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-) | 允许控制从 HTML、MHTML 导入文档时如何加载外部资源（图像、样式表）。 |
| [setSupportVml(boolean value)](#setSupportVml-boolean-) | 设置一个值，指示是否支持 VML 图像。 |
| [setTempFolder(String value)](#setTempFolder-java.lang.String-) | 允许在阅读文档时使用临时文件。 |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean-) | 指定是否更新具有脏属性的字段。 |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | 在加载操作期间调用，当检测到可能导致数据或格式保真度丢失的问题时调用。 |
| [setWebRequestTimeout(int value)](#setWebRequestTimeout-int-) | Web 请求超时前等待的毫秒数。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### HtmlLoadOptions() {#HtmlLoadOptions--}
```
public HtmlLoadOptions()
```


使用默认值初始化此类的新实例。

### HtmlLoadOptions(String password) {#HtmlLoadOptions-java.lang.String-}
```
public HtmlLoadOptions(String password)
```


使用指定密码初始化此类的新实例以加载加密文档的快捷方式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| password | java.lang.String | 打开加密文档的密码。可以为 null 或空字符串。 |

### HtmlLoadOptions(int loadFormat, String password, String baseUri) {#HtmlLoadOptions-int-java.lang.String-java.lang.String-}
```
public HtmlLoadOptions(int loadFormat, String password, String baseUri)
```


初始化此类的新实例。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| loadFormat | int |  |
| password | java.lang.String |  |
| baseUri | java.lang.String |  |

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### getBaseUri() {#getBaseUri--}
```
public String getBaseUri()
```


获取将用于在需要时将文档中找到的相对 URI 解析为绝对 URI 的字符串。可以为 null 或空字符串。默认为空。

在以下情况下，此属性用于将相对 URI 解析为绝对 URI：

1.  从流中加载 HTML 文档时，该文档包含具有相对 URI 的图像，并且没有在 BASE HTML 元素中指定的基本 URI。
2.  将文档保存为 PDF 和其他格式时，检索使用相对 URI 链接的图像，以便将图像保存到输出文档中。

**退货：**
java.lang.String - 将用于在需要时将文档中找到的相对 URI 解析为绝对 URI 的字符串。
### getBlockImportMode() {#getBlockImportMode--}
```
public int getBlockImportMode()
```


获取一个值，该值指定如何导入块级元素的属性。默认值为[BlockImportMode.MERGE](../../com.aspose.words/blockimportmode\#MERGE).

**退货：**
int - 指定如何导入块级元素的属性的值。返回值是其中之一[BlockImportMode](../../com.aspose.words/blockimportmode)常数。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getConvertMetafilesToPng() {#getConvertMetafilesToPng--}
```
public boolean getConvertMetafilesToPng()
```


获取是否转换图元文件（**F:Aspose.FileFormat.Wmf**或者**F:Aspose.FileFormat.Emf** ) 图片到**F:Aspose.FileFormat.Png**图像格式。图元文件 (**F:Aspose.FileFormat.Wmf**或者**F:Aspose.FileFormat.Emf** ) 是一种未压缩的图像格式，有时需要大量 RAM 来保存和处理文档。此选项允许将所有图元文件图像转换为**F:Aspose.FileFormat.Png**关于文档加载。请注意 - 将矢量图形转换为光栅会降低图像质量。

**退货：**
 boolean - 是否转换图元文件 (**F:Aspose.FileFormat.Wmf**或者**F:Aspose.FileFormat.Emf** ) 图片到**F:Aspose.FileFormat.Png**图像格式。
### getConvertShapeToOfficeMath() {#getConvertShapeToOfficeMath--}
```
public boolean getConvertShapeToOfficeMath()
```


获取是否将带有 EquationXML 的形状转换为 Office Math 对象。

**退货：**
布尔值 - 是否将带有 EquationXML 的形状转换为 Office Math 对象。
### getConvertSvgToEmf() {#getConvertSvgToEmf--}
```
public boolean getConvertSvgToEmf()
```


获取一个值，该值指示是否将加载的 SVG 图像转换为 EMF 格式。默认值为 false，如果可能，加载的 SVG 图像将按原样存储而不进行转换。

较新版本的 MS Word 本机支持 SVG 图像。如果加载选项中指定的 MS Word 版本支持 SVG，Aspose.Words 将按原样存储 SVG 图像而不进行转换。如果不支持 SVG，加载的 SVG 图像将被转换为 EMF 格式。

但是，如果此选项设置为 true ，Aspose.Words 会将加载的 SVG 图像转换为 EMF，即使指定版本的 MS Word 支持 SVG 图像。

**退货：**
boolean - 一个值，指示是否将加载的 SVG 图像转换为 EMF 格式。
### getEncoding() {#getEncoding--}
```
public Charset getEncoding()
```


如果文档中未指定编码，则获取将用于加载 HTML、TXT 或 CHM 文档的编码。可以为空。默认为空。

此属性仅在加载 HTML、TXT 或 CHM 文档时使用。

如果文档中未指定编码且此属性为 null ，则系统将尝试自动检测编码。

**退货：**
java.nio.charset.Charset - 如果文档中未指定编码，则用于加载 HTML、TXT 或 CHM 文档的编码。
### getFontSettings() {#getFontSettings--}
```
public FontSettings getFontSettings()
```


允许指定文档字体设置。

加载某些格式时，Aspose.Words 可能需要解析字体。例如，在加载 HTML 文档时，Aspose.Words 可能会解析字体以执行字体回退。

如果设置为空，默认静态字体设置[FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--)将会被使用。

默认值为空。

**退货：**
[FontSettings](../../com.aspose.words/fontsettings) - 相应的[FontSettings](../../com.aspose.words/fontsettings)价值。
### getIgnoreNoscriptElements() {#getIgnoreNoscriptElements--}
```
public boolean getIgnoreNoscriptElements()
```


获取一个值，该值指示是否忽略 HTML 元素。默认值为 false 。与 MS Word 一样，Aspose.Words 不支持脚本，默认情况下会将元素内容加载到生成的文档中。然而，在大多数浏览器中，脚本是受支持的，并且其中的内容是不可见的。将此属性设置为 true 会强制 Aspose.Words 忽略所有元素，并有助于生成看起来更接近浏览器中所见内容的文档。

**退货：**
boolean - 一个指示是否忽略 HTML 元素的值。
### getLanguagePreferences() {#getLanguagePreferences--}
```
public LanguagePreferences getLanguagePreferences()
```


获取将在加载文档时使用的语言首选项。

**退货：**
[LanguagePreferences](../../com.aspose.words/languagepreferences) - 加载文档时将使用的语言首选项。
### getLoadFormat() {#getLoadFormat--}
```
public int getLoadFormat()
```


指定要加载的文档的格式。默认为[LoadFormat.AUTO](../../com.aspose.words/loadformat\#AUTO).

建议您指定[LoadFormat.AUTO](../../com.aspose.words/loadformat\#AUTO)值并让 Aspose.Words 自动检测文件格式。如果您知道要加载的文档的格式，则可以明确指定格式，这将通过与自动检测格式相关的开销稍微减少加载时间。如果您指定了一个显式的加载格式，但它会被证明是错误的，那么将调用自动检测并进行第二次加载文件的尝试。

**退货：**
int - 相应的 int 值。返回值是其中之一[LoadFormat](../../com.aspose.words/loadformat)常数。
### getMswVersion() {#getMswVersion--}
```
public int getMswVersion()
```


允许指定文档加载过程应匹配特定的 MS Word 版本。默认值为[MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion\#WORD-2019)不同的 Word 版本在加载过程中处理文档内容和格式的某些方面可能略有不同，这可能导致文档对象模型中的细微差别。

**退货：**
int - 相应的 int 值。返回值是其中之一[MsWordVersion](../../com.aspose.words/mswordversion)常数。
### getPassword() {#getPassword--}
```
public String getPassword()
```


获取打开加密文档的密码。可以为 null 或空字符串。默认为空。

您需要知道密码才能打开加密文档。如果文档未加密，请将其设置为 null 或空字符串。

**退货：**
java.lang.String - 打开加密文档的密码。
### getPreferredControlType() {#getPreferredControlType--}
```
public int getPreferredControlType()
```


获取将表示导入和元素的首选类型的文档节点。默认值为[HtmlControlType.FORM\_FIELD](../../com.aspose.words/htmlcontroltype\#FORM-FIELD).请注意，设置此属性并不能保证所有导入的控件都是指定的类型。如果 HTML 控件不能用首选类型的文档节点表示，Aspose.Words 将使用兼容的[HtmlControlType](../../com.aspose.words/htmlcontroltype)对于那个控制。

**退货：**
 int - 表示导入和元素的首选文档节点类型。返回值是其中之一[HtmlControlType](../../com.aspose.words/htmlcontroltype)常数。
### getPreserveIncludePictureField() {#getPreserveIncludePictureField--}
```
public boolean getPreserveIncludePictureField()
```


获取在阅读 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。默认值为假。

默认情况下，INCLUDEPICTURE 字段会转换为形状对象。如果您需要保留该字段，例如，如果您希望以编程方式更新它，则可以覆盖它。但是请注意，这种方法在 Aspose.Words 中并不常见。自行承担使用风险。

一种可能的用例可能是使用 MERGEFIELD 作为子字段来动态更改图片的源路径。在这种情况下，您需要将 INCLUDEPICTURE 保留在模型中。

**退货：**
boolean - 在读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。
### getProgressCallback() {#getProgressCallback--}
```
public IDocumentLoadingCallback getProgressCallback()
```


在加载文档期间调用并接受有关加载进度的数据。

[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat\#OTT)支持的格式。

**退货：**
[IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback) - 相应的[IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback)价值。
### getResourceLoadingCallback() {#getResourceLoadingCallback--}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


允许控制从 HTML、MHTML 导入文档时如何加载外部资源（图像、样式表）。

**退货：**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) - 相应的[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback)价值。
### getSupportVml() {#getSupportVml--}
```
public boolean getSupportVml()
```


获取一个值，该值指示是否支持 VML 图像。

**退货：**
boolean - 指示是否支持 VML 图像的值。
### getTempFolder() {#getTempFolder--}
```
public String getTempFolder()
```


允许在阅读文档时使用临时文件。默认情况下，此属性为 null 且不使用临时文件。

该文件夹必须存在且可写，否则会抛出异常。

Aspose.Words 在读取完成后自动删除所有临时文件。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getUpdateDirtyFields() {#getUpdateDirtyFields--}
```
public boolean getUpdateDirtyFields()
```


指定是否更新具有脏属性的字段。

**退货：**
boolean - 相应的布尔值。
### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


在加载操作期间调用，当检测到可能导致数据或格式保真度丢失的问题时调用。

**退货：**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - 相应的[IWarningCallback](../../com.aspose.words/iwarningcallback)价值。
### getWebRequestTimeout() {#getWebRequestTimeout--}
```
public int getWebRequestTimeout()
```


Web 请求超时前等待的毫秒数。默认值为 100000 毫秒（100 秒）。当加载在 HTML 和 MHTML 文档中链接的外部资源（图像、样式表）时，Aspose.Words 等待响应的毫秒数。

**退货：**
int - 相应的 int 值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setBaseUri(String value) {#setBaseUri-java.lang.String-}
```
public void setBaseUri(String value)
```


设置将用于在需要时将文档中找到的相对 URI 解析为绝对 URI 的字符串。可以为 null 或空字符串。默认为空。

在以下情况下，此属性用于将相对 URI 解析为绝对 URI：

1.  从流中加载 HTML 文档时，该文档包含具有相对 URI 的图像，并且没有在 BASE HTML 元素中指定的基本 URI。
2.  将文档保存为 PDF 和其他格式时，检索使用相对 URI 链接的图像，以便将图像保存到输出文档中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 需要时将用于将文档中找到的相对 URI 解析为绝对 URI 的字符串。 |

### setBlockImportMode(int value) {#setBlockImportMode-int-}
```
public void setBlockImportMode(int value)
```


设置一个值，指定如何导入块级元素的属性。默认值为[BlockImportMode.MERGE](../../com.aspose.words/blockimportmode\#MERGE).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 一个值，指定如何导入块级元素的属性。该值必须是其中之一[BlockImportMode](../../com.aspose.words/blockimportmode)常数。 |

### setConvertMetafilesToPng(boolean value) {#setConvertMetafilesToPng-boolean-}
```
public void setConvertMetafilesToPng(boolean value)
```


设置是否转换图元文件（**F:Aspose.FileFormat.Wmf**或者**F:Aspose.FileFormat.Emf** ) 图片到**F:Aspose.FileFormat.Png**图像格式。图元文件 (**F:Aspose.FileFormat.Wmf**或者**F:Aspose.FileFormat.Emf** ) 是一种未压缩的图像格式，有时需要大量 RAM 来保存和处理文档。此选项允许将所有图元文件图像转换为**F:Aspose.FileFormat.Png**关于文档加载。请注意 - 将矢量图形转换为光栅会降低图像质量。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否转换元文件（**F:Aspose.FileFormat.Wmf**或者**F:Aspose.FileFormat.Emf** ) 图片到**F:Aspose.FileFormat.Png**图像格式。 |

### setConvertShapeToOfficeMath(boolean value) {#setConvertShapeToOfficeMath-boolean-}
```
public void setConvertShapeToOfficeMath(boolean value)
```


设置是否将带有 EquationXML 的形状转换为 Office Math 对象。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 是否将带有 EquationXML 的形状转换为 Office Math 对象。 |

### setConvertSvgToEmf(boolean value) {#setConvertSvgToEmf-boolean-}
```
public void setConvertSvgToEmf(boolean value)
```


设置一个值，指示是否将加载的 SVG 图像转换为 EMF 格式。默认值为 false，如果可能，加载的 SVG 图像将按原样存储而不进行转换。

较新版本的 MS Word 本机支持 SVG 图像。如果加载选项中指定的 MS Word 版本支持 SVG，Aspose.Words 将按原样存储 SVG 图像而不进行转换。如果不支持 SVG，加载的 SVG 图像将被转换为 EMF 格式。

但是，如果此选项设置为 true ，Aspose.Words 会将加载的 SVG 图像转换为 EMF，即使指定版本的 MS Word 支持 SVG 图像。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值，指示是否将加载的 SVG 图像转换为 EMF 格式。 |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset-}
```
public void setEncoding(Charset value)
```


如果文档中未指定编码，则设置将用于加载 HTML、TXT 或 CHM 文档的编码。可以为空。默认为空。

此属性仅在加载 HTML、TXT 或 CHM 文档时使用。

如果文档中未指定编码且此属性为 null ，则系统将尝试自动检测编码。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.nio.charset.Charset | 如果未在文档中指定编码，则将用于加载 HTML、TXT 或 CHM 文档的编码。 |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings-}
```
public void setFontSettings(FontSettings value)
```


允许指定文档字体设置。

加载某些格式时，Aspose.Words 可能需要解析字体。例如，在加载 HTML 文档时，Aspose.Words 可能会解析字体以执行字体回退。

如果设置为空，默认静态字体设置[FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--)将会被使用。

默认值为空。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings) | 相应的[FontSettings](../../com.aspose.words/fontsettings)价值。 |

### setIgnoreNoscriptElements(boolean value) {#setIgnoreNoscriptElements-boolean-}
```
public void setIgnoreNoscriptElements(boolean value)
```


设置一个值，指示是否忽略 HTML 元素。默认值为 false 。与 MS Word 一样，Aspose.Words 不支持脚本，默认情况下会将元素内容加载到生成的文档中。然而，在大多数浏览器中，脚本是受支持的，并且其中的内容是不可见的。将此属性设置为 true 会强制 Aspose.Words 忽略所有元素，并有助于生成看起来更接近浏览器中所见内容的文档。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示是否忽略 HTML 元素的值。 |

### setLoadFormat(int value) {#setLoadFormat-int-}
```
public void setLoadFormat(int value)
```


指定要加载的文档的格式。默认为[LoadFormat.AUTO](../../com.aspose.words/loadformat\#AUTO).

建议您指定[LoadFormat.AUTO](../../com.aspose.words/loadformat\#AUTO)值并让 Aspose.Words 自动检测文件格式。如果您知道要加载的文档的格式，则可以明确指定格式，这将通过与自动检测格式相关的开销稍微减少加载时间。如果您指定了一个显式的加载格式，但它会被证明是错误的，那么将调用自动检测并进行第二次加载文件的尝试。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[LoadFormat](../../com.aspose.words/loadformat)常数。 |

### setMswVersion(int value) {#setMswVersion-int-}
```
public void setMswVersion(int value)
```


允许指定文档加载过程应匹配特定的 MS Word 版本。默认值为[MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion\#WORD-2019)不同的 Word 版本在加载过程中处理文档内容和格式的某些方面可能略有不同，这可能导致文档对象模型中的细微差别。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[MsWordVersion](../../com.aspose.words/mswordversion)常数。 |

### setPassword(String value) {#setPassword-java.lang.String-}
```
public void setPassword(String value)
```


设置打开加密文档的密码。可以为 null 或空字符串。默认为空。

您需要知道密码才能打开加密文档。如果文档未加密，请将其设置为 null 或空字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 打开加密文档的密码。 |

### setPreferredControlType(int value) {#setPreferredControlType-int-}
```
public void setPreferredControlType(int value)
```


设置将代表导入和元素的首选文档节点类型。默认值为[HtmlControlType.FORM\_FIELD](../../com.aspose.words/htmlcontroltype\#FORM-FIELD).请注意，设置此属性并不能保证所有导入的控件都是指定的类型。如果 HTML 控件不能用首选类型的文档节点表示，Aspose.Words 将使用兼容的[HtmlControlType](../../com.aspose.words/htmlcontroltype)对于那个控制。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 表示导入和元素的首选文档节点类型。该值必须是其中之一[HtmlControlType](../../com.aspose.words/htmlcontroltype)常数。 |

### setPreserveIncludePictureField(boolean value) {#setPreserveIncludePictureField-boolean-}
```
public void setPreserveIncludePictureField(boolean value)
```


设置在阅读 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。默认值为假。

默认情况下，INCLUDEPICTURE 字段会转换为形状对象。如果您需要保留该字段，例如，如果您希望以编程方式更新它，则可以覆盖它。但是请注意，这种方法在 Aspose.Words 中并不常见。自行承担使用风险。

一种可能的用例可能是使用 MERGEFIELD 作为子字段来动态更改图片的源路径。在这种情况下，您需要将 INCLUDEPICTURE 保留在模型中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。 |

### setProgressCallback(IDocumentLoadingCallback value) {#setProgressCallback-com.aspose.words.IDocumentLoadingCallback-}
```
public void setProgressCallback(IDocumentLoadingCallback value)
```


在加载文档期间调用并接受有关加载进度的数据。

[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat\#OTT)支持的格式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback) | 相应的[IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback)价值。 |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


允许控制从 HTML、MHTML 导入文档时如何加载外部资源（图像、样式表）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) | 相应的[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback)价值。 |

### setSupportVml(boolean value) {#setSupportVml-boolean-}
```
public void setSupportVml(boolean value)
```


设置一个值，指示是否支持 VML 图像。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示是否支持 VML 图像的值。 |

### setTempFolder(String value) {#setTempFolder-java.lang.String-}
```
public void setTempFolder(String value)
```


允许在阅读文档时使用临时文件。默认情况下，此属性为 null 且不使用临时文件。

该文件夹必须存在且可写，否则会抛出异常。

Aspose.Words 在读取完成后自动删除所有临时文件。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setUpdateDirtyFields(boolean value) {#setUpdateDirtyFields-boolean-}
```
public void setUpdateDirtyFields(boolean value)
```


指定是否更新具有脏属性的字段。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


在加载操作期间调用，当检测到可能导致数据或格式保真度丢失的问题时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) | 相应的[IWarningCallback](../../com.aspose.words/iwarningcallback)价值。 |

### setWebRequestTimeout(int value) {#setWebRequestTimeout-int-}
```
public void setWebRequestTimeout(int value)
```


Web 请求超时前等待的毫秒数。默认值为 100000 毫秒（100 秒）。当加载在 HTML 和 MHTML 文档中链接的外部资源（图像、样式表）时，Aspose.Words 等待响应的毫秒数。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。 |

### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
