---
title: "Aspose::Words::WarningInfo 类"
linktitle: "WarningInfo"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::WarningInfo 类。包含有关 Aspose.Words 在文档加载或保存期间发出的警告的信息。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 74000
url: /zh/cpp/aspose.words/warninginfo/
---
## WarningInfo class


包含 Aspose.Words 在文档加载或保存期间发出的警告信息。要了解更多，请访问 [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) 文档文章。

```cpp
class WarningInfo : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Description](./get_description/)() const | 返回警告的描述。 |
| [get_Source](./get_source/)() const | 返回警告的来源。 |
| [get_WarningType](./get_warningtype/)() const | 返回警告的类型。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 备注


您不能创建此类的实例。此类的对象由 Aspose.Words 创建并传递给 [Warning()](../iwarningcallback/warning/) 方法。

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
