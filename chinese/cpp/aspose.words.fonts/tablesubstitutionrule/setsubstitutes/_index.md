---
title: "Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes 方法"
linktitle: "SetSubstitutes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes 方法。覆盖给定原始字体名称的替代字体名称（在 C++ 中）。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule::SetSubstitutes method


覆盖给定原始字体名称的替代字体名称。

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes(const System::String &originalFontName, const System::ArrayPtr<System::String> &substituteFontNames)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| originalFontName | const System::String\& | 原始字体名称。 |
| substituteFontNames | const System::ArrayPtr\<System::String\>\& | 替代字体名称列表。 |

## 示例



展示如何设置字体替换规则。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// 默认的字体来源包含文档使用的第一种字体。
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// 第二种字体 "Amethysta" 不可用。
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// 我们可以配置一个字体替换表，用于确定
// Aspose.Words 将使用哪些字体来替代不可用的字体。
// 为 "Amethysta" 设置两个替代字体："Arvo", 和 "Courier New"。
// 如果第一个替代字体不可用，Aspose.Words 将尝试使用第二个替代字体，依此类推。
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->SetSubstitutes(u"Amethysta", System::MakeArray<System::String>({u"Arvo", u"Courier New"}));

// "Amethysta" 不可用，替换规则指出第一个使用的替代字体是 "Arvo"。
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// "Arvo" 也不可用，但 "Courier New" 可用。
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// 输出文档将显示使用 "Amethysta" 字体的文本，但会以 "Courier New" 格式呈现。
doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitution.pdf");
```


展示如何使用自定义字体替换表。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// 创建一个新的表替换规则并加载默认的 Windows 字体替换表。
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();

// 如果我们仅从自己的文件夹中选择字体，则需要自定义替换表。
// 我们将不再能够访问 Microsoft Windows 字体，
// 例如 "Arial" 或 "Times New Roman"，因为它们在我们的新字体文件夹中不存在。
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// 以下是从本地文件系统中的文件加载替换表的两种方式。
// 1 -  从流中加载：
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font substitution rules.xml", System::IO::FileMode::Open);
    tableSubstitutionRule->Load(fileStream);
}

// 2 -  直接从文件加载：
tableSubstitutionRule->Load(get_MyDir() + u"Font substitution rules.xml");

// 由于我们不再能够访问 "Arial"，我们的字体表将首先尝试用 "Nonexistent Font" 替代它。
// 我们没有该字体，因此会转而使用下一个替代字体 "Kreon"，它位于 "MyFonts" 文件夹中。
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Missing Font", u"Kreon"}), tableSubstitutionRule->GetSubstitutes(u"Arial")->LINQ_ToArray());

// 我们可以以编程方式扩展此表。我们将添加一条将 "Times New Roman" 替换为 "Arvo" 的条目。
ASSERT_TRUE(System::TestTools::IsNull(tableSubstitutionRule->GetSubstitutes(u"Times New Roman")));
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// 我们可以使用 AddSubstitutes() 为现有字体条目添加二级回退替代。
// 如果 "Arvo" 不可用，我们的表将查找 "M+ 2m" 作为第二个替代选项。
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// SetSubstitutes() 可以为某个字体设置新的替代字体列表。
tableSubstitutionRule->SetSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// 使用我们无法访问的字体编写文本时，将触发我们的替代规则。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Text written in Arial, to be substituted by Kreon.");

builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Custom.pdf");
```

## 另见

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
