---
title: "Aspose::Words::Document::UnlinkFields 方法"
linktitle: "UnlinkFields"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::UnlinkFields 方法。在 C++ 中解除文档中所有字段的链接。"
type: docs
weight: 94000
url: /zh/cpp/aspose.words/document/unlinkfields/
---
## Document::UnlinkFields method


取消链接文档中的所有字段。

```cpp
void Aspose::Words::Document::UnlinkFields()
```

## 备注


将文档中所有字段替换为其最新的结果。

要在文档的特定部分解除字段链接，请使用 [UnlinkFields](../../range/unlinkfields/)。

## 示例



展示如何解除文档中所有字段的链接。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

doc->UnlinkFields();
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
