---
title: "Aspose::Words::ParagraphFormat::get_WordWrap 方法"
linktitle: "get_WordWrap"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_WordWrap 方法。如果此属性为 false，则当前段落中的单词中间的拉丁文字可以换行。否则，拉丁文字将按完整单词换行（在 C++ 中）。"
type: docs
weight: 42000
url: /zh/cpp/aspose.words/paragraphformat/get_wordwrap/
---
## ParagraphFormat::get_WordWrap method


如果此属性为 **false**，则当前段落中单词中间的拉丁文本可以换行。否则，拉丁文本将按完整单词换行。

```cpp
bool Aspose::Words::ParagraphFormat::get_WordWrap()
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
