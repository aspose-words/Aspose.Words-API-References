---
title: "Aspose::Words::Fonts::TableSubstitutionRule class"
linktitle: "TableSubstitutionRule"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::TableSubstitutionRule class. 表格字体替换规则。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class


表格字体替换规则。欲了解更多，请访问[Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/)文档文章。

```cpp
class TableSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [AddSubstitutes](./addsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | 为给定的原始字体名称添加替代字体名称。 |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | 指定规则是否已启用。 |
| [GetSubstitutes](./getsubstitutes/)(const System::String\&) | 返回包含指定原始字体名称的替代字体名称的数组。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Load](./load/)(const System::String\&) | 从 XML 文件加载表格替换设置。 |
| [Load](./load/)(const System::SharedPtr\<System::IO::Stream\>\&) | 从 XML 流加载表格替换设置。 |
| [LoadAndroidSettings](./loadandroidsettings/)() | 加载 Android 平台的预定义表替换设置。 |
| [LoadLinuxSettings](./loadlinuxsettings/)() | 加载 Linux 平台的预定义表替换设置。 |
| [LoadWindowsSettings](./loadwindowssettings/)() | 加载 Windows 平台的预定义表替换设置。 |
| [Save](./save/)(const System::String\&) | 将当前表替换设置保存到文件。 |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | 将当前表替换设置保存到流。 |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | 设置器用于 [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/)。 |
| [SetSubstitutes](./setsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | 覆盖给定原始字体名称的替代字体名称。 |
| static [Type](./type/)() |  |

## 示例



展示如何访问 Windows 和 Linux 的字体替换表。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// 创建新的表替换规则并加载默认的 Microsoft Windows 字体替换表。
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();
tableSubstitutionRule->LoadWindowsSettings();

// 在 Windows 中，"Times New Roman CE" 字体的默认替代字体是 "Times New Roman"。
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Times New Roman"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// 我们可以将表保存为 XML 文档的形式。
tableSubstitutionRule->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Windows.xml");

// Linux 有其自己的替换表。
// "Times New Roman CE" 有多个替代字体。
// 如果第一个替代字体 "FreeSerif" 也不可用，
// 此规则将遍历数组中的其他字体，直到找到可用的为止。
tableSubstitutionRule->LoadLinuxSettings();
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"FreeSerif", u"Liberation Serif", u"DejaVu Serif"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// 使用流将 Linux 替换表保存为 XML 文档的形式。
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Linux.xml", System::IO::FileMode::Create);
    tableSubstitutionRule->Save(fileStream);
}
```

## 另见

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
