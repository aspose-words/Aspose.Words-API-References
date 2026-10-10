---
title: "Aspose::Words::Fonts::TableSubstitutionRule::LoadLinuxSettings 方法"
linktitle: "LoadLinuxSettings"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::TableSubstitutionRule::LoadLinuxSettings 方法。 加载针对 Linux 平台的预定义表替换设置（C++）。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/
---
## TableSubstitutionRule::LoadLinuxSettings method


加载 Linux 平台的预定义表替换设置。

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::LoadLinuxSettings()
```


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

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
