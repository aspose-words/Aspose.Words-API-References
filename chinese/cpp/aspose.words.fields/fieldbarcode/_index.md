---
title: "Aspose::Words::Fields::FieldBarcode 类"
linktitle: "FieldBarcode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldBarcode 类。实现 BARCODE 字段。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words.fields/fieldbarcode/
---
## FieldBarcode class


实现 BARCODE 字段。欲了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldBarcode : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FacingIdentificationMark](./get_facingidentificationmark/)() | 获取或设置要插入的面对识别标记 (FIM) 类型。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_IsBookmark](./get_isbookmark/)() | 获取或设置 [PostalAddress](./get_postaladdress/) 是否为书签的名称。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_IsUSPostalAddress](./get_isuspostaladdress/)() | 获取或设置 [PostalAddress](./get_postaladdress/) 是否为美国邮政地址。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_PostalAddress](./get_postaladdress/)() | 获取或设置用于生成条形码的邮政地址或引用它的书签名称。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_FacingIdentificationMark](./set_facingidentificationmark/)(const System::String\&) | 用于 [Aspose::Words::Fields::FieldBarcode::get_FacingIdentificationMark](./get_facingidentificationmark/) 的设置器。 |
| [set_IsBookmark](./set_isbookmark/)(bool) | 用于 [Aspose::Words::Fields::FieldBarcode::get_IsBookmark](./get_isbookmark/) 的设置器。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_IsUSPostalAddress](./set_isuspostaladdress/)(bool) | 用于 [Aspose::Words::Fields::FieldBarcode::get_IsUSPostalAddress](./get_isuspostaladdress/) 的设置器。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_PostalAddress](./set_postaladdress/)(const System::String\&) | 用于 [Aspose::Words::Fields::FieldBarcode::get_PostalAddress](./get_postaladdress/) 的设置器。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
