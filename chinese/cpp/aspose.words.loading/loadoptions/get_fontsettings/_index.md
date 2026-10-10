---
title: "Aspose::Words::Loading::LoadOptions::get_FontSettings method"
linktitle: "get_FontSettings"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LoadOptions::get_FontSettings 方法。允许在 C++ 中指定文档字体设置。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.loading/loadoptions/get_fontsettings/
---
## LoadOptions::get_FontSettings method


允许指定文档字体设置。

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Loading::LoadOptions::get_FontSettings() const
```

## 备注


加载某些格式时，Aspose.Words 可能需要解析字体。例如，加载 HTML 文档时，[Aspose.Words](../../../aspose.words/) 可能会解析字体以执行字体回退。

如果设置为 **null**，将使用默认的静态字体设置 [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/)。

默认值是 **null**。

## 示例



展示如何在加载期间指定字体替代。
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// 为 LoadOptions 对象设置字体替代规则。
// 如果我们加载的文档使用了我们没有的字体，
// 此规则将用已有的字体替代不可用的字体。
// 在这种情况下，所有对 \"MissingFont\" 的使用将转换为 \"Comic Sans MS\"。
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> substitutionRule = loadOptions->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution();
substitutionRule->AddSubstitutes(u"MissingFont", System::MakeArray<System::String>({u"Comic Sans MS"}));

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.html", loadOptions);

// 此时，此类文本仍将显示为 \"MissingFont\"。
// 字体替代将在我们渲染文档时发生。
ASSERT_EQ(u"MissingFont", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());

doc->Save(get_ArtifactsDir() + u"FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```


展示如何在加载文档时应用字体替代设置。
```cpp
// 创建一个 FontSettings 对象，用于替代 \"Times New Roman\" 字体
// 使用我们 \"MyFonts\" 文件夹中的 \"Arvo\" 字体。
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));

// 将该 FontSettings 对象设置为新创建的 LoadOptions 对象的属性。
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(fontSettings);

// 加载文档，然后使用字体替代将其渲染为 PDF。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.FontSettings.pdf");
```

## 另见

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
