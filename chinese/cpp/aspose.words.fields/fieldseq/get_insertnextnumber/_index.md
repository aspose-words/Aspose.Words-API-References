---
title: "Aspose::Words::Fields::FieldSeq::get_InsertNextNumber 方法"
linktitle: "get_InsertNextNumber"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldSeq::get_InsertNextNumber 方法。获取或设置是否在 C++ 中为指定项目插入下一个序列号。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.fields/fieldseq/get_insertnextnumber/
---
## FieldSeq::get_InsertNextNumber method


获取或设置是否为指定项目插入下一个序列号。

```cpp
bool Aspose::Words::Fields::FieldSeq::get_InsertNextNumber()
```


## 示例



展示使用 SEQ 字段创建编号。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// SEQ 字段显示一个在每个 SEQ 字段处递增的计数。
// 这些字段还为每个唯一命名的序列维护独立的计数
// 由 SEQ 字段的 "SequenceIdentifier" 属性标识。
// 插入一个 SEQ 字段，以显示 "MySequence" 的当前计数值，
// 在使用 "ResetNumber" 属性将其设置为 100 之后。
builder->Write(u"#");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetNumber(u"100");
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\r 100", fieldSeq->GetFieldCode());
ASSERT_EQ(u"100", fieldSeq->get_Result());

// 使用另一个 SEQ 字段显示此序列的下一个数字。
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->Update();

ASSERT_EQ(u"101", fieldSeq->get_Result());

// 插入一级标题。
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"This level 1 heading will reset MySequence to 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// 插入同一序列的另一个 SEQ 字段，并将其配置为在每个标题处将计数重置为 1。
builder->Write(u"\n#");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetHeadingLevel(u"1");
fieldSeq->Update();

// 上述标题是一级标题，因此此序列的计数被重置为 1。
ASSERT_EQ(u" SEQ  MySequence \\s 1", fieldSeq->GetFieldCode());
ASSERT_EQ(u"1", fieldSeq->get_Result());

// 移动到此序列的下一个数字。
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_InsertNextNumber(true);
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\n", fieldSeq->GetFieldCode());
ASSERT_EQ(u"2", fieldSeq->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.ResetNumbering.docx");
```

## 另见

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
