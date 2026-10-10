---
title: "Aspose::Words::Fields::FieldBarcode::get_FacingIdentificationMark 方法"
linktitle: "get_FacingIdentificationMark"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldBarcode::get_FacingIdentificationMark 方法。获取或设置要在 C++ 中插入的面向识别标记 (FIM) 的类型。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldbarcode/get_facingidentificationmark/
---
## FieldBarcode::get_FacingIdentificationMark method


获取或设置要插入的面对识别标记 (FIM) 类型。

```cpp
System::String Aspose::Words::Fields::FieldBarcode::get_FacingIdentificationMark()
```


## 示例



展示如何使用 BARCODE 字段以条形码形式显示美国邮政编码。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// 下面展示了使用 BARCODE 字段显示自定义值为条形码的两种方法。
// 1 - 将条形码将显示的值存储在 PostalAddress 属性中：
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));

// 此值必须是有效的邮政编码。
field->set_PostalAddress(u"96801");
field->set_IsUSPostalAddress(true);
field->set_FacingIdentificationMark(u"C");

ASSERT_EQ(u" BARCODE  96801 \\u \\f C", field->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::LineBreak);

// 2 - 引用存储此条形码将显示的值的书签：
field = System::ExplicitCast<Aspose::Words::Fields::FieldBarcode>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldBarcode, true));
field->set_PostalAddress(u"BarcodeBookmark");
field->set_IsBookmark(true);

ASSERT_EQ(u" BARCODE  BarcodeBookmark \\b", field->GetFieldCode());

// BARCODE 字段在其 PostalAddress 属性中引用的书签
// 必须仅包含有效的邮政编码。
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"BarcodeBookmark");
builder->Writeln(u"968877");
builder->EndBookmark(u"BarcodeBookmark");

doc->Save(get_ArtifactsDir() + u"Field.BARCODE.docx");
```

## 另见

* Class [FieldBarcode](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
