---
title: "Aspose::Words::ParagraphFormat::get_HangingPunctuation 方法"
linktitle: "get_HangingPunctuation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_HangingPunctuation 方法。获取或设置一个标志，指示是否为当前段落启用悬挂标点（C++）。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words/paragraphformat/get_hangingpunctuation/
---
## ParagraphFormat::get_HangingPunctuation method


获取或设置一个标志，指示当前段落是否启用悬挂标点。

```cpp
bool Aspose::Words::ParagraphFormat::get_HangingPunctuation()
```


## 示例



展示如何为亚洲排版设置特殊属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_FarEastLineBreakControl(true);
format->set_WordWrap(false);
format->set_HangingPunctuation(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.AsianTypographyProperties.docx");
```

## 另见

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
