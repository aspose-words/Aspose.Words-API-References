---
title: "Aspose::Words::Loading::ChmLoadOptions 类"
linktitle: "ChmLoadOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::ChmLoadOptions 类。允许在将 CHM 文档加载到 Document 对象时指定其他选项。欲了解更多，请访问 C++ 中的文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.loading/chmloadoptions/
---
## ChmLoadOptions class


允许在将 CHM 文档加载到 [Document](../../aspose.words/document/) 对象时指定其他选项。欲了解更多，请访问 [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) 文档文章。

```cpp
class ChmLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ChmLoadOptions](./chmloadoptions/)() | 使用默认值初始化此类的新实例。 |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | 确定指定的对象在值上是否等于当前对象。 |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | 获取或设置将在需要时用于将文档中找到的相对 URI 解析为绝对 URI 的字符串。可以为 **null** 或空字符串。默认值为 **null**。 |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | 获取或设置是否将元文件（[Wmf](../) 或 [Emf](../)）图像转换为 [Png](../) 图像格式。 |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | 获取或设置是否将带有 EquationXML 的形状转换为 Office [Math](../../aspose.words.math/) 对象。 |
| [get_Encoding](../loadoptions/get_encoding/)() const | 获取或设置在文档内部未指定编码时用于加载 HTML、TXT 或 CHM 文档的编码。可以为 **null**。默认值为 **null**。 |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | 允许指定文档字体设置。 |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | 指定是否忽略 OLE 数据。 |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | 获取在文档加载时将使用的语言首选项。 |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | 指定要加载的文档格式。默认是 [Auto](../../aspose.words/loadformat/)。 |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | 允许指定文档加载过程应匹配特定的 MS Word 版本。默认值为 [Word2019](../../aspose.words.settings/mswordversion/)。 |
| [get_OriginalFileName](./get_originalfilename/)() const | CHM 文件的名称。默认值为 **null**。 |
| [get_Password](../loadoptions/get_password/)() const | 获取或设置打开加密文档的密码。可以是 **null** 或空字符串。默认值为 **null**。 |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | 获取或设置在读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。默认值为 **false**。 |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | 在加载文档期间调用，并接受有关加载进度的数据。 |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | 定义在加载期间出现错误时应如何处理文档。使用此属性指定系统是应尝试恢复文档还是遵循其他定义的行为。默认值为 [TryRecover](../documentrecoverymode/)。 |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | 允许控制从 HTML、MHTML 导入文档时外部资源（图像、样式表）的加载方式。 |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | 允许在读取文档时使用临时文件。默认情况下此属性为 **null**，不使用临时文件。 |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | 指定是否使用 **dirty** 属性更新字段。 |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | 获取或设置是否使用从 Windows 注册表获取的 LCID 值来确定页面设置的默认边距。 |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | 在加载操作期间调用，当检测到可能导致数据或格式保真度丢失的问题时。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | 使用默认值初始化此类的新实例。 |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | 使用指定密码加载加密文档，以快捷方式初始化此类的新实例。 |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | 使用属性设置为指定值，以快捷方式初始化此类的新实例。 |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/) 的 setter。 |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/) 的 setter。 |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/) 的 setter。 |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | 设置 [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | 设置 [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | 设置 [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | 设置 [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | 设置 [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_OriginalFileName](./set_originalfilename/)(const System::String\&) | 用于 [Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName](./get_originalfilename/) 的 setter。 |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | 设置 [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | 设置 [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | 在加载文档期间调用，并接受有关加载进度的数据。 |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | 设置 [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | 允许控制从 HTML、MHTML 导入文档时外部资源（图像、样式表）的加载方式。 |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | 设置 [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | 设置 [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | 设置 [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | 在加载操作期间调用，当检测到可能导致数据或格式保真度丢失的问题时。 |
| static [Type](./type/)() |  |

## 示例



展示如何解析类似 "ms-its:myfile.chm::/index.htm" 的 URL。
```cpp
// 我们的文档包含类似 "ms-its:amhelp.chm::....htm" 的 URL，但它有不同的名称，
// 将其保存为 HTML 后，so 文件链接无法工作。
// 我们需要在 'ChmLoadOptions' 中定义原始文件名，以避免此行为。
auto loadOptions = System::MakeObject<Aspose::Words::Loading::ChmLoadOptions>();
loadOptions->set_OriginalFileName(u"amhelp.chm");

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::IO::File::ReadAllBytes(get_MyDir() + u"Document with ms-its links.chm")), loadOptions);

doc->Save(get_ArtifactsDir() + u"ExChmLoadOptions.OriginalFileName.html");
```

## 另见

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
