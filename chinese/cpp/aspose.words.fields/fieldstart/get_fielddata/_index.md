---
title: "Aspose::Words::Fields::FieldStart::get_FieldData 方法"
linktitle: "get_FieldData"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldStart::get_FieldData 方法。获取与字段关联的自定义字段数据（C++）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.fields/fieldstart/get_fielddata/
---
## FieldStart::get_FieldData method


获取与该字段关联的自定义字段数据。

```cpp
const System::ArrayPtr<uint8_t> & Aspose::Words::Fields::FieldStart::get_FieldData() const
```


## 示例



展示如何获取与字段关联的数据。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - Field with data.docx");

System::SharedPtr<Aspose::Words::Fields::Field> field = doc->get_Range()->get_Fields()->idx_get(2);
std::cout << System::Text::Encoding::get_Default()->GetString(field->get_Start()->get_FieldData()) << std::endl;
```

## 另见

* Class [FieldStart](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
