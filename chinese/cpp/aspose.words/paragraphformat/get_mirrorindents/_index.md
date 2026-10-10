---
title: "Aspose::Words::ParagraphFormat::get_MirrorIndents 方法"
linktitle: "get_MirrorIndents"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_MirrorIndents 方法。获取或设置一个标志，指示左右缩进是否具有相同宽度（C++）。"
type: docs
weight: 24500
url: /zh/cpp/aspose.words/paragraphformat/get_mirrorindents/
---
## ParagraphFormat::get_MirrorIndents method


获取或设置指示左、右缩进是否具有相同宽度的标志。

```cpp
bool Aspose::Words::ParagraphFormat::get_MirrorIndents()
```


## 示例



展示如何使左右缩进相同。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();

format->set_MirrorIndents(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.MirrorIndents.docx");
```

## 另见

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
