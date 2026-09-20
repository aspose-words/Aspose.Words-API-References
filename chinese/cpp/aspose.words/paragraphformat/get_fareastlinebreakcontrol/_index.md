---
title: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl method"
linktitle: "get_FarEastLineBreakControl"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl 方法。获取或设置一个标志，指示是否在 C++ 中对当前段落应用东亚换行规则。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words/paragraphformat/get_fareastlinebreakcontrol/
---
## ParagraphFormat::get_FarEastLineBreakControl method


获取或设置一个标志，指示是否对当前段落应用东亚换行规则。

```cpp
bool Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl()
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
