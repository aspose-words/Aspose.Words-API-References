---
title: "Aspose::Words::IWarningCallback::Warning 方法"
linktitle: "警告"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::IWarningCallback::Warning 方法。当 Aspose.Words 在 C++ 中加载或保存文档时遇到可能导致格式或数据完整性丢失的问题时，会调用此方法。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/iwarningcallback/warning/
---
## IWarningCallback::Warning method


Aspose.Words 在文档加载或保存期间遇到可能导致格式或数据保真度丢失的问题时调用此方法。

```cpp
virtual void Aspose::Words::IWarningCallback::Warning(System::SharedPtr<Aspose::Words::WarningInfo> info)=0
```


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

* Class [WarningInfo](../../warninginfo/)
* Interface [IWarningCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
