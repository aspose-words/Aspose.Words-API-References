---
title: "Aspose::Words::Fonts::FontInfoSubstitutionRule 类"
linktitle: "FontInfoSubstitutionRule"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontInfoSubstitutionRule 类。字体信息替代规则。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.fonts/fontinfosubstitutionrule/
---
## FontInfoSubstitutionRule class


[Font](../../aspose.words/font/) info substitution rule. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontInfoSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | 指定规则是否已启用。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | 设置器用于 [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/)。 |
| static [Type](./type/)() |  |

## 示例



展示如何设置属性，以在可用字体源中查找缺失字体的最接近匹配。
```cpp
// 打开一个包含使用在任何字体源中都不存在的字体格式化的文本的文档。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// 分配回调以处理字体替代警告。
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// 设置默认字体名称并启用字体替代。
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// 在字体替换后应使用原始字体度量。
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// 如果我们保存的文档缺少字体，将会收到字体替换警告。
doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.EnableFontSubstitution.pdf");

for (auto&& info : warningCollector)
{
    if (info->get_WarningType() == Aspose::Words::WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```

## 另见

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
