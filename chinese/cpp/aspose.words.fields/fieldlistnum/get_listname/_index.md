---
title: "Aspose::Words::Fields::FieldListNum::get_ListName 方法"
linktitle: "get_ListName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldListNum::get_ListName 方法。获取或设置用于编号的抽象编号定义的名称（在 C++ 中）。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.fields/fieldlistnum/get_listname/
---
## FieldListNum::get_ListName method


获取或设置用于编号的抽象编号定义的名称。

```cpp
System::String Aspose::Words::Fields::FieldListNum::get_ListName()
```


## 示例



展示如何使用 LISTNUM 字段为段落编号。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// LISTNUM 字段显示一个在每个 LISTNUM 字段递增的数字。
// 这些字段还具有多种选项，使我们能够使用它们来模拟编号列表。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));

// 列表默认从 1 开始计数，但我们可以将此数字设置为其他值，例如 0。
// 此字段将显示 "0)"。
field->set_StartingNumber(u"0");
builder->Writeln(u"Paragraph 1");

ASSERT_EQ(u" LISTNUM  \\s 0", field->GetFieldCode());

// LISTNUM 字段为每个列表级别维护独立计数。
// 在与另一个 LISTNUM 字段相同的段落中插入 LISTNUM 字段
// 会增加列表级别而不是计数。
// 下一个字段将继续我们在上面开始的计数，并在列表级别 1 显示值 \"1\"。
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// 此字段将在列表级别 2 开始计数。它将显示值 \"1\"。
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// 此字段将在列表级别 3 开始计数。它将显示值 \"1\"。
// 不同的列表级别有不同的格式，
// 因此这些字段组合后将显示值 \"1)a)i)\"。
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);
builder->Writeln(u"Paragraph 2");

// 我们插入的下一个 LISTNUM 字段将继续该列表级别的计数
// 即前一个 LISTNUM 字段所在的列表级别。
// 我们可以使用 \"ListLevel\" 属性跳转到不同的列表级别。
// 如果此 LISTNUM 字段保持在列表级别 3，它将显示 \"ii)\"，
// 但由于我们已将其移动到列表级别 2，它将在该级别继续计数并显示 \"b)\"。
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListLevel(u"2");
builder->Writeln(u"Paragraph 3");

ASSERT_EQ(u" LISTNUM  \\l 2", field->GetFieldCode());

// 我们可以设置 ListName 属性，使字段模拟不同的 AUTONUM 字段类型。
// \"NumberDefault\" 模拟 AUTONUM，\"OutlineDefault\" 模拟 AUTONUMOUT，
// 并且 \"LegalDefault\" 模拟 AUTONUMLGL 字段。
// 使用起始数字 1 的 \"OutlineDefault\" 列表名称将显示为 \"I.\"。
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_StartingNumber(u"1");
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 4");

ASSERT_TRUE(field->get_HasListName());
ASSERT_EQ(u" LISTNUM  OutlineDefault \\s 1", field->GetFieldCode());

// ListName 不会从前一个字段继承，因此我们需要为每个新字段设置它。
// 此字段使用不同的列表名称继续计数，并显示 \"II.\"。
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 5");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.LISTNUM.docx");
```

## 另见

* Class [FieldListNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
