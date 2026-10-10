---
title: "Aspose::Words::Range::UnlinkFields 方法"
linktitle: "UnlinkFields"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Range::UnlinkFields 方法。在 C++ 中解除此范围内字段的链接。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words/range/unlinkfields/
---
## Range::UnlinkFields method


解除此范围内字段的链接。

```cpp
void Aspose::Words::Range::UnlinkFields()
```

## 备注


将此范围内的所有字段替换为其最新的结果。

要在整个文档中解除字段链接，请使用 [UnlinkFields](./)。

## 示例



展示如何在范围内解除所有字段的链接。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");

auto newSection = System::ExplicitCast<Aspose::Words::Section>(System::ExplicitCast<Aspose::Words::Node>(doc->get_Sections()->idx_get(0))->Clone(true));
doc->get_Sections()->Add(newSection);

doc->get_Sections()->idx_get(1)->get_Range()->UnlinkFields();
```

## 另见

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
