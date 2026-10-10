---
title: "Aspose::Words::Document::AcceptAllRevisions 方法"
linktitle: "AcceptAllRevisions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::AcceptAllRevisions 方法。接受文档中所有的修订更改（C++）。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/document/acceptallrevisions/
---
## Document::AcceptAllRevisions method


接受文档中所有已跟踪的更改。

```cpp
void Aspose::Words::Document::AcceptAllRevisions()
```


## 示例



展示如何接受文档中的所有跟踪更改。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 在跟踪更改的同时编辑文档，以创建一些修订。
doc->StartTrackRevisions(u"John Doe");
builder->Write(u"Hello world! ");
builder->Write(u"Hello again! ");
builder->Write(u"This is another revision.");
doc->StopTrackRevisions();

ASSERT_EQ(3, doc->get_Revisions()->get_Count());

// 我们可以遍历每个修订，并在文档中接受或拒绝它们。
// 如果我们知道想要接受所有修订，可以通过调用此方法更直接地完成。
doc->AcceptAllRevisions();

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"Hello world! Hello again! This is another revision.", doc->GetText().Trim());
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
