---
title: "Aspose::Words::Document::UpdateActualReferenceMarks 方法"
linktitle: "UpdateActualReferenceMarks"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::UpdateActualReferenceMarks 方法。更新文档中所有脚注和尾注的 ActualReferenceMark 属性（C++）。"
type: docs
weight: 95500
url: /zh/cpp/aspose.words/document/updateactualreferencemarks/
---
## Document::UpdateActualReferenceMarks method


更新文档中所有脚注和尾注的 [ActualReferenceMark](../../../aspose.words.notes/footnote/get_actualreferencemark/) 属性。

```cpp
void Aspose::Words::Document::UpdateActualReferenceMarks()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
