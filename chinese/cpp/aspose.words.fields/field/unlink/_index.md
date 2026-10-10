---
title: "Aspose::Words::Fields::Field::Unlink 方法"
linktitle: "取消链接"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::Field::Unlink 方法。在 C++ 中执行字段取消链接。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words.fields/field/unlink/
---
## Field::Unlink method


执行字段的取消链接。

```cpp
bool Aspose::Words::Fields::Field::Unlink()
```


### ReturnValue

**true** if the field has been unlinked, otherwise **false**.
## 备注


用字段的最新结果替换该字段。

某些字段，例如 XE（索引条目）字段和 SEQ（序列）字段，无法取消链接。

## 示例



展示如何取消链接字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Linked fields.docx");
doc->get_Range()->get_Fields()->idx_get(1)->Unlink();
```

## 另见

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
