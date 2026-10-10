---
title: "Aspose::Words::Fields::FormField::RemoveField 方法"
linktitle: "RemoveField"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FormField::RemoveField 方法。删除完整的表单字段，而不仅仅是 C++ 中的表单字段特殊字符。"
type: docs
weight: 27000
url: /zh/cpp/aspose.words.fields/formfield/removefield/
---
## FormField::RemoveField method


删除整个表单字段，而不仅仅是表单字段的特殊字符。

```cpp
void Aspose::Words::Fields::FormField::RemoveField()
```


## 示例



展示如何删除表单字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

System::SharedPtr<Aspose::Words::Fields::FormField> formField = doc->get_Range()->get_FormFields()->idx_get(3);
formField->RemoveField();
```

## 另见

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
