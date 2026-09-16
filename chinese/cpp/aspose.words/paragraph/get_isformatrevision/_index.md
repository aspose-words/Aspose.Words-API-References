---
title: "Aspose::Words::Paragraph::get_IsFormatRevision method"
linktitle: "get_IsFormatRevision"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Paragraph::get_IsFormatRevision 方法。如果在启用更改跟踪时 Microsoft Word 中对象的格式被更改，则返回 true（C++）。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words/paragraph/get_isformatrevision/
---
## Paragraph::get_IsFormatRevision method


如果在启用更改跟踪时，Microsoft Word 中对象的格式被更改，则返回 true。

```cpp
bool Aspose::Words::Paragraph::get_IsFormatRevision()
```


## 示例



展示如何检查段落是否为格式修订。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Format revision.docx");

// 此段落是\"Format\"修订，当我们更改现有文本的格式时会出现此情况
// 在 Microsoft Word 中通过 "Review" -> "Track changes" 跟踪修订。
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_IsFormatRevision());
```

## 另见

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
