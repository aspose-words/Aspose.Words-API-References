---
title: "Aspose::Words::ParagraphFormat::get_BaselineAlignment method"
linktitle: "get_BaselineAlignment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_BaselineAlignment method. 获取或设置字体在行上的垂直位置（C++）。"
type: docs
weight: 5500
url: /zh/cpp/aspose.words/paragraphformat/get_baselinealignment/
---
## ParagraphFormat::get_BaselineAlignment method


获取或设置字体在行上的垂直位置。

```cpp
Aspose::Words::BaselineAlignment Aspose::Words::ParagraphFormat::get_BaselineAlignment()
```


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

* Enum [BaselineAlignment](../../baselinealignment/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
