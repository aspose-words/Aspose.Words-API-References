---
title: "Aspose::Words::Loading::LoadOptions 类"
linktitle: "LoadOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LoadOptions 类。允许在将文档加载到 Document 对象时指定其他选项（例如密码或基础 URI）。欲了解更多，请访问 C++ 中的文档文章。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.loading/loadoptions/
---
## LoadOptions class


允许在将文档加载到 [Document](../../aspose.words/document/) 对象时指定其他选项（例如密码或基础 URI）。欲了解更多，请访问 [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) 文档文章。

```cpp
class LoadOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | 确定指定的对象在值上是否等于当前对象。 |
| [get_BaseUri](./get_baseuri/)() const | 获取或设置将在需要时用于将文档中找到的相对 URI 解析为绝对 URI 的字符串。可以为 **null** 或空字符串。默认值为 **null**。 |
| [get_ConvertMetafilesToPng](./get_convertmetafilestopng/)() const | 获取或设置是否将元文件（[Wmf](../) 或 [Emf](../)）图像转换为 [Png](../) 图像格式。 |
| [get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/)() const | 获取或设置是否将带有 EquationXML 的形状转换为 Office [Math](../../aspose.words.math/) 对象。 |
| [get_Encoding](./get_encoding/)() const | 获取或设置在文档内部未指定编码时用于加载 HTML、TXT 或 CHM 文档的编码。可以为 **null**。默认值为 **null**。 |
| [get_FontSettings](./get_fontsettings/)() const | 允许指定文档字体设置。 |
| [get_IgnoreOleData](./get_ignoreoledata/)() const | 指定是否忽略 OLE 数据。 |
| [get_LanguagePreferences](./get_languagepreferences/)() const | 获取在文档加载时将使用的语言首选项。 |
| [get_LoadFormat](./get_loadformat/)() const | 指定要加载的文档格式。默认是 [Auto](../../aspose.words/loadformat/)。 |
| [get_MswVersion](./get_mswversion/)() const | 允许指定文档加载过程应匹配特定的 MS Word 版本。默认值为 [Word2019](../../aspose.words.settings/mswordversion/)。 |
| [get_Password](./get_password/)() const | 获取或设置打开加密文档的密码。可以是 **null** 或空字符串。默认值为 **null**。 |
| [get_PreserveIncludePictureField](./get_preserveincludepicturefield/)() const | 获取或设置在读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。默认值为 **false**。 |
| [get_ProgressCallback](./get_progresscallback/)() const | 在加载文档期间调用，并接受有关加载进度的数据。 |
| [get_RecoveryMode](./get_recoverymode/)() const | 定义在加载期间出现错误时应如何处理文档。使用此属性指定系统是应尝试恢复文档还是遵循其他定义的行为。默认值为 [TryRecover](../documentrecoverymode/)。 |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | 允许控制从 HTML、MHTML 导入文档时外部资源（图像、样式表）的加载方式。 |
| [get_TempFolder](./get_tempfolder/)() const | 允许在读取文档时使用临时文件。默认情况下此属性为 **null**，不使用临时文件。 |
| [get_UpdateDirtyFields](./get_updatedirtyfields/)() const | 指定是否使用 **dirty** 属性更新字段。 |
| [get_UseSystemLcid](./get_usesystemlcid/)() const | 获取或设置是否使用从 Windows 注册表获取的 LCID 值来确定页面设置的默认边距。 |
| [get_WarningCallback](./get_warningcallback/)() const | 在加载操作期间调用，当检测到可能导致数据或格式保真度丢失的问题时。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](./loadoptions/)() | 使用默认值初始化此类的新实例。 |
| [LoadOptions](./loadoptions/)(const System::String\&) | 使用指定密码加载加密文档，以快捷方式初始化此类的新实例。 |
| [LoadOptions](./loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | 使用属性设置为指定值，以快捷方式初始化此类的新实例。 |
| [set_BaseUri](./set_baseuri/)(const System::String\&) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_BaseUri](./get_baseuri/) 的 setter。 |
| [set_ConvertMetafilesToPng](./set_convertmetafilestopng/)(bool) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](./get_convertmetafilestopng/) 的 setter。 |
| [set_ConvertShapeToOfficeMath](./set_convertshapetoofficemath/)(bool) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/) 的 setter。 |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_Encoding](./get_encoding/) 的 setter。 |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_FontSettings](./get_fontsettings/) 的 setter。 |
| [set_IgnoreOleData](./set_ignoreoledata/)(bool) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](./get_ignoreoledata/) 的 setter。 |
| [set_LoadFormat](./set_loadformat/)(Aspose::Words::LoadFormat) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_LoadFormat](./get_loadformat/) 的 setter。 |
| [set_MswVersion](./set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_MswVersion](./get_mswversion/) 的 setter。 |
| [set_Password](./set_password/)(const System::String\&) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_Password](./get_password/) 的 setter。 |
| [set_PreserveIncludePictureField](./set_preserveincludepicturefield/)(bool) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](./get_preserveincludepicturefield/) 的 setter。 |
| [set_ProgressCallback](./set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | 在加载文档期间调用，并接受有关加载进度的数据。 |
| [set_RecoveryMode](./set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](./get_recoverymode/) 的 setter。 |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | 允许控制从 HTML、MHTML 导入文档时外部资源（图像、样式表）的加载方式。 |
| [set_TempFolder](./set_tempfolder/)(const System::String\&) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_TempFolder](./get_tempfolder/) 的 setter。 |
| [set_UpdateDirtyFields](./set_updatedirtyfields/)(bool) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](./get_updatedirtyfields/)。 |
| [set_UseSystemLcid](./set_usesystemlcid/)(bool) | 用于设置 [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](./get_usesystemlcid/)。 |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | 在加载操作期间调用，当检测到可能导致数据或格式保真度丢失的问题时。 |
| static [Type](./type/)() |  |

## 示例



展示如何加载加密的 Microsoft Word 文档。
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// 如果尝试在没有密码的情况下打开加密文档，Aspose.Words 会抛出异常。
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// 在加载此类文档时，密码通过 LoadOptions 对象传递给文档的构造函数。
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// 使用 LoadOptions 对象加载加密文档有两种方式。
// 1 -  通过文件名从本地文件系统加载文档：
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  从流中加载文档：
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## 另见

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
