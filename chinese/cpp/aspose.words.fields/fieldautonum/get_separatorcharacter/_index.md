---
title: "Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter 方法"
linktitle: "get_SeparatorCharacter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter 方法。获取或设置在 C++ 中使用的分隔符字符。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldautonum/get_separatorcharacter/
---
## FieldAutoNum::get_SeparatorCharacter method


获取或设置要使用的分隔符字符。

```cpp
System::String Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter()
```


## 示例



展示如何使用 autonum 字段对段落进行编号。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 每个 AUTONUM 字段显示 AUTONUM 字段运行计数的当前值，
// 允许我们像编号列表一样自动为项目编号。
// 此字段将显示数字 "1."。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 1.");

ASSERT_EQ(u" AUTONUM ", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 2.");

// 分隔符字符默认是句点，它出现在字段结果中数字后紧接的位置。
// 如果我们将此属性设为 null，我们的第二个 AUTONUM 字段将在文档中显示 "2."。
ASSERT_TRUE(System::TestTools::IsNull(field->get_SeparatorCharacter()));

// 我们可以设置此属性，以将其字符串的第一个字符用作新的分隔符字符。
// 在这种情况下，我们的 AUTONUM 字段现在将显示 "2:"。
field->set_SeparatorCharacter(u":");

ASSERT_EQ(u" AUTONUM  \\s :", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.AUTONUM.docx");
```

## 另见

* Class [FieldAutoNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
