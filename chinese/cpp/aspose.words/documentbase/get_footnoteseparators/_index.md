---
title: "Aspose::Words::DocumentBase::get_FootnoteSeparators 方法"
linktitle: "get_FootnoteSeparators"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBase::get_FootnoteSeparators 方法。提供对文档中定义的脚注/尾注分隔符的访问（C++）。"
type: docs
weight: 4500
url: /zh/cpp/aspose.words/documentbase/get_footnoteseparators/
---
## DocumentBase::get_FootnoteSeparators method


提供对文档中定义的脚注/尾注分隔符的访问。

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteSeparatorCollection> Aspose::Words::DocumentBase::get_FootnoteSeparators() const
```


## 示例



展示如何移除尾注分隔符。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> endnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::EndnoteSeparator);
// 移除尾注分隔符。
endnoteSeparator->get_FirstParagraph()->get_FirstChild()->Remove();
```


展示如何管理脚注分隔符格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// 对齐脚注分隔符。
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## 另见

* Class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
