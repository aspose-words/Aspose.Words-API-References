---
title: "طريقة Aspose::Words::Tables::Cell::EnsureMinimum"
linktitle: "EnsureMinimum"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::Cell::EnsureMinimum. إذا لم يكن الطفل الأخير فقرة، فإنها تنشئ وتضيف فقرة فارغة واحدة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.tables/cell/ensureminimum/
---
## Cell::EnsureMinimum method


إذا لم يكن العنصر الفرعي الأخير فقرة، ينشئ ويضيف فقرة فارغة واحدة.

```cpp
void Aspose::Words::Tables::Cell::EnsureMinimum()
```


## أمثلة



يوضح كيفية التأكد من أن عقدة الخلية تحتوي على العقد التي نحتاجها لبدء إضافة محتوى إليها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);
auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

// قد تحتوي الخلايا على فقرات بعناصر نمطية مثل المقاطع، الأشكال، وحتى جداول أخرى.
// خليةنا الجديدة لا تحتوي على أي فقرات، ولا يمكننا إضافة محتويات مثل عقد المقاطع والأشكال إليها حتى تتوفر.
ASSERT_EQ(0, cell->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// استدعاء طريقة "EnsureMinimum" على خلية سيضمن أن
// الخلية لديها على الأقل فقرة فارغة واحدة، والتي يمكننا بعد ذلك إضافة محتويات إليها.
cell->EnsureMinimum();
cell->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## انظر أيضًا

* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
