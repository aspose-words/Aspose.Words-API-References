---
title: "Aspose::Words::Fields::FieldRD::get_FileName 方法"
linktitle: "get_FileName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldRD::get_FileName 方法。获取或设置在 C++ 中生成目录、权威表或索引时要包含的文件名。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldrd/get_filename/
---
## FieldRD::get_FileName method


获取或设置在生成目录、权威目录或索引时要包含的文件名。

```cpp
System::String Aspose::Words::Fields::FieldRD::get_FileName()
```


## 示例



展示如何使用 RD 字段从其他文档的标题创建目录条目。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用文档生成器插入目录，
// 然后在下一页为目录添加一个条目。
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
builder->Writeln(u"TOC entry from within this document");

// 插入 RD 字段，该字段在其 FileName 属性中引用另一个本地文件系统文档。
// 目录现在也会接受来自被引用文档的所有标题作为其表格的条目。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldRD>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRefDoc, true));
field->set_FileName(get_ArtifactsDir() + u"ReferencedDocument.docx");

ASSERT_EQ(System::String::Format(u" RD  {0}ReferencedDocument.docx", get_ArtifactsDir().Replace(u"\\", u"\\\\")), field->GetFieldCode());

// 创建 RD 字段所引用的文档并插入标题。
// 此标题将在我们的第一个文档的目录字段中显示为条目。
auto referencedDoc = System::MakeObject<Aspose::Words::Document>();
auto refDocBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(referencedDoc);
refDocBuilder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
refDocBuilder->Writeln(u"TOC entry from referenced document");
referencedDoc->Save(get_ArtifactsDir() + u"ReferencedDocument.docx");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.RD.docx");
```

## 另见

* Class [FieldRD](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
