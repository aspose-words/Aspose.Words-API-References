---
title: "Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions 构造函数"
linktitle: "OoxmlSaveOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions 构造函数。初始化此类的一个新实例，可用于在 C++ 中将文档保存为 Docx 格式。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions::OoxmlSaveOptions() constructor


初始化此类的一个新实例，可用于将文档保存为 [Docx](../../../aspose.words/saveformat/) 格式。

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions()
```


## 示例



展示如何为已保存的文档设置 OOXML 合规规范以遵循。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 如果我们将兼容性选项配置为符合 Microsoft Word 2003，
// 插入图像将使用 VML 定义其形状。
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// "ISO/IEC 29500:2008" OOXML 标准不支持 VML 形状。
// 如果我们将 SaveOptions 对象的 \"Compliance\" 属性设置为 \"OoxmlCompliance.Iso29500_2008_Strict\",
// 任何在传递此对象时保存的文档都必须遵循该标准。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// 我们保存的文档使用 DML 定义形状，以符合 \"ISO/IEC 29500:2008\" OOXML 标准。
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```

## 另见

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat) constructor


初始化此类的一个新实例，可用于将文档保存为 [Docx](../../../aspose.words/saveformat/)、[Docm](../../../aspose.words/saveformat/)、[Dotx](../../../aspose.words/saveformat/)、[Dotm](../../../aspose.words/saveformat/) 或 [FlatOpc](../../../aspose.words/saveformat/) 格式。

```cpp
Aspose::Words::Saving::OoxmlSaveOptions::OoxmlSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | 可以是 [Docx](../../../aspose.words/saveformat/)、[Docm](../../../aspose.words/saveformat/)、[Dotx](../../../aspose.words/saveformat/)、[Dotm](../../../aspose.words/saveformat/) 或 [FlatOpc](../../../aspose.words/saveformat/)。 |

## 示例



展示如何在转换为 .docx 时支持旧版控制字符。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy control character.doc");

// 当我们将文档保存为 OOXML 格式时，可以创建一个 OoxmlSaveOptions 对象
// 然后将其传递给文档的保存方法，以修改文档的保存方式。
// 将 "KeepLegacyControlChars" 属性设置为 "true" 以保留
// 在保存时保留 "ShortDateTime" 旧版字符。
// 将 "KeepLegacyControlChars" 属性设置为 "false" 以移除
// 输出文档中的 "ShortDateTime" 旧版字符。
auto so = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? System::String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : System::String(u"\u001e\f"), doc->get_FirstSection()->get_Body()->GetText());
```

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
