---
title: "Aspose::Words::BaselineAlignment 枚举"
linktitle: "BaselineAlignment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BaselineAlignment 枚举。指定 C++ 中字体在行上的垂直位置。"
type: docs
weight: 80500
url: /zh/cpp/aspose.words/baselinealignment/
---
## BaselineAlignment enum


指定字体在行上的垂直位置。

```cpp
enum class BaselineAlignment
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 顶部 | 0 | 对齐每个字体的顶部。 |
| 居中 | 1 | 对齐每个字体的中心点。 |
| 基线 | 2 | 对齐到段落的基线。 |
| 底部 | 3 | 对齐每个字体的底部。 |
| 自动 | 4 | 基线会自动调整。 |


## 示例



展示如何设置字体在行上的垂直位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();
if (format->get_BaselineAlignment() == Aspose::Words::BaselineAlignment::Auto)
{
    format->set_BaselineAlignment(Aspose::Words::BaselineAlignment::Top);
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphBaselineAlignment.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
