---
title: "Aspose::Words::Tables::Table::Table مُنشئ"
linktitle: "Table"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::Table::Table مُنشئ. يهيئ نسخة جديدة من فئة Table في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.tables/table/table/
---
## Table::Table constructor


يهيئ نسخة جديدة من الفئة [Table](../).

```cpp
Aspose::Words::Tables::Table::Table(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | المستند المالك. |
## ملاحظات


عند إنشاء [Table](../)، ينتمي إلى المستند المحدد، لكنه ليس جزءًا من المستند بعد و[ParentNode](../../../aspose.words/node/get_parentnode/) هو **null**.

لإضافة [Table](../) إلى المستند استخدم [InsertAfter1()</see> أو <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) في القصة حيث تريد إدراج الجدول.

## أمثلة



يعرض كيفية إنشاء جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// الجداول تحتوي على صفوف، والتي تحتوي على خلايا، والتي قد تحتوي على فقرات
// مع عناصر نمطية مثل السلاسل، الأشكال، وحتى جداول أخرى.
// استدعاء طريقة "EnsureMinimum" على جدول سيضمن أن
// الجدول يحتوي على صف واحد على الأقل، وخلية، وفقرة.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// أضف نصًا إلى الخلية الأولى في الصف الأول من الجدول.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```

## انظر أيضًا

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
