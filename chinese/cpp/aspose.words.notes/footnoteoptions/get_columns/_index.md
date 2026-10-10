---
title: "Aspose::Words::Notes::FootnoteOptions::get_Columns 方法"
linktitle: "get_Columns"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::FootnoteOptions::get_Columns 方法。指定 C++ 中脚注区域的列数。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.notes/footnoteoptions/get_columns/
---
## FootnoteOptions::get_Columns method


指定脚注区域的列数。

```cpp
int32_t Aspose::Words::Notes::FootnoteOptions::get_Columns()
```


## 示例



展示如何将脚注部分拆分为指定数量的列。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

doc->get_FootnoteOptions()->set_Columns(2);
doc->Save(get_ArtifactsDir() + u"Document.FootnoteColumns.docx");
```

## 另见

* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
