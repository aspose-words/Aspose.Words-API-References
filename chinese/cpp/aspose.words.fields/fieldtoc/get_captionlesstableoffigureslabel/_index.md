---
title: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel 方法"
linktitle: "get_CaptionlessTableOfFiguresLabel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel 方法。获取或设置在 C++ 中构建不包含标题标签和编号的图表目录时使用的序列标识符名称。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.fields/fieldtoc/get_captionlesstableoffigureslabel/
---
## FieldToc::get_CaptionlessTableOfFiguresLabel method


获取或设置在构建不包含标题标签和编号的图表目录时使用的序列标识符名称。

```cpp
System::String Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel()
```


## 示例



展示如何设置序列标识符的名称。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));
fieldToc->set_CaptionlessTableOfFiguresLabel(u"Test");

ASSERT_EQ(u" TOC  \\a Test", fieldToc->GetFieldCode());
```

## 另见

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
