---
title: "Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes 方法"
linktitle: "get_IsInMegabytes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes 方法。获取或设置是否在 C++ 中以兆字节显示文件大小。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.fields/fieldfilesize/get_isinmegabytes/
---
## FieldFileSize::get_IsInMegabytes method


获取或设置是否以兆字节显示文件大小。

```cpp
bool Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes()
```


## 示例



展示如何使用 FILESIZE 域显示文档的文件大小。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(18105, doc->get_BuiltInDocumentProperties()->get_Bytes());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertParagraph();

// 以下是三种不同的计量单位
// FILESIZE 域可以使用这些单位显示文档的文件大小。
// 1 - 字节：
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->Update();

ASSERT_EQ(u" FILESIZE ", field->GetFieldCode());
ASSERT_EQ(u"18105", field->get_Result());

// 2 - 千字节：
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInKilobytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\k", field->GetFieldCode());
ASSERT_EQ(u"18", field->get_Result());

// 3 - 兆字节：
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInMegabytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\m", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

// 在 Microsoft Word 中编辑时更新这些字段的值，
// 我们必须先保存更改，然后手动更新这些字段。
doc->Save(get_ArtifactsDir() + u"Field.FILESIZE.docx");
```

## 另见

* Class [FieldFileSize](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
