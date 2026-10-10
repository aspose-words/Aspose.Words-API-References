---
title: "Aspose::Words::WarningType 枚举"
linktitle: "警告类型"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::WarningType enum。指定由 Aspose.Words 在 C++ 中加载或保存文档时发出的警告类型。"
type: docs
weight: 129000
url: /zh/cpp/aspose.words/warningtype/
---
## WarningType enum


指定 Aspose.Words 在文档加载或保存期间发出的警告类型。

```cpp
enum class WarningType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| DataLossCategory | 255 | 在加载后文档树中或在保存后生成的文档中，某些文本/字符/图像或其他数据将会缺失。 |
| DataLoss | 1 | 通用数据丢失，无特定代码。 |
| MajorFormattingLossCategory | 65280 | 生成的文档或其中的特定位置可能与原始文档相比有显著差异。 |
| MajorFormattingLoss | 256 | 通用的重大格式丢失，无特定代码。 |
| MinorFormattingLossCategory | 16711680 | 生成的文档或其中的特定位置可能与原始文档相比有些许差异。 |
| MinorFormattingLoss | 65536 | 通用的轻微格式丢失，无特定代码。 |
| FontSubstitution | 131072 | [Font](../font/) 已被替换。 |
| FontEmbedding | 262144 | 文档保存期间嵌入字体信息丢失。 |
| UnexpectedContentCategory | 251658240 | 源文档中的某些内容无法识别（即不受支持），这可能会导致问题或导致数据/格式丢失，也可能不会。 |
| UnexpectedContent | 16777216 | 通用的意外内容，无特定代码。 |
| 提示 | 268435456 | 提示潜在问题或建议改进。 |


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
