---
title: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark 方法"
linktitle: "get_ActualReferenceMark"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::Footnote::get_ActualReferenceMark 方法。获取在文档中显示的此脚注的引用标记的实际文本（C++）。"
type: docs
weight: 3834
url: /zh/cpp/aspose.words.notes/footnote/get_actualreferencemark/
---
## Footnote::get_ActualReferenceMark method


获取此脚注在文档中显示的引用标记的实际文本。

```cpp
System::String Aspose::Words::Notes::Footnote::get_ActualReferenceMark()
```


## 示例



展示如何获取实际的脚注引用标记。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

auto footnote = System::ExplicitCast<Aspose::Words::Notes::Footnote>(doc->GetChild(Aspose::Words::NodeType::Footnote, 1, true));
doc->UpdateFields();
doc->UpdateActualReferenceMarks();

ASSERT_EQ(u"1", footnote->get_ActualReferenceMark());
```

## 另见

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
