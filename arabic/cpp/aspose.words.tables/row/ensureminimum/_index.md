---
title: "طريقة Aspose::Words::Tables::Row::EnsureMinimum"
linktitle: "EnsureMinimum"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::Row::EnsureMinimum. إذا لم يحتوي الصف على خلايا، ينشئ ويضيف خلية واحدة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.tables/row/ensureminimum/
---
## Row::EnsureMinimum method


إذا لم يحتوي [Row](../) على خلايا، ينشئ ويضيف [Cell](../../cell/) واحدة.

```cpp
void Aspose::Words::Tables::Row::EnsureMinimum()
```


## أمثلة



يوضح كيفية التأكد من أن عقدة الصف تحتوي على العقد التي نحتاجها لبدء إضافة المحتوى إليها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// تحتوي الصفوف على خلايا، تحتوي على فقرات مع عناصر نموذجية مثل النصوص المتتابعة، الأشكال، وحتى جداول أخرى.
// الصف الجديد لدينا لا يحتوي على أي من هذه العقد، ولا يمكننا إضافة محتوى إليه حتى يتوفر ذلك.
ASSERT_EQ(0, row->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// استدعاء طريقة "EnsureMinimum" على جدول سيضمن أن
// الجدول يحتوي على خلية واحدة على الأقل مع فقرة فارغة.
row->EnsureMinimum();
row->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## انظر أيضًا

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
