---
title: "Aspose::Words::Tables::Table::EnsureMinimum طريقة"
linktitle: "EnsureMinimum"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::Table::EnsureMinimum method. إذا لم يحتوي الجدول على أي صفوف، ينشئ ويضيف صفًا واحدًا في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.tables/table/ensureminimum/
---
## Table::EnsureMinimum method


إذا لم يحتوي الجدول على أي صفوف، ينشئ ويضيف [Row](../../row/) واحدًا.

```cpp
void Aspose::Words::Tables::Table::EnsureMinimum()
```


## أمثلة



يوضح كيفية التأكد من أن عقدة الجدول تحتوي على العقد التي نحتاجها لإضافة محتوى.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// الجداول تحتوي على صفوف، التي تحتوي على خلايا، والتي قد تحتوي على فقرات
// مع عناصر نمطية مثل السلاسل، الأشكال، وحتى جداول أخرى.
// جدولنا الجديد لا يحتوي على أي من هذه العقد، ولا يمكننا إضافة محتوى إليه حتى يحتويها.
ASSERT_EQ(0, table->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// استدعاء طريقة "EnsureMinimum" على جدول سيضمن أن
// الجدول يحتوي على صف واحد على الأقل وخلية واحدة مع فقرة فارغة.
table->EnsureMinimum();
table->get_FirstRow()->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## انظر أيضًا

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
