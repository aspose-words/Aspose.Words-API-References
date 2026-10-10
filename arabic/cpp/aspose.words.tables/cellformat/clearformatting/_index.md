---
title: "طريقة Aspose::Words::Tables::CellFormat::ClearFormatting"
linktitle: "ClearFormatting"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::CellFormat::ClearFormatting. يعيد تنسيق الخلية إلى الوضع الافتراضي. لا يغيّر عرض الخلية في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat::ClearFormatting method


يعيد تنسيق الخلية إلى الإعدادات الافتراضية. لا يغيّر عرض الخلية.

```cpp
void Aspose::Words::Tables::CellFormat::ClearFormatting()
```


## أمثلة



يوضح كيفية دمج الصفوف من جدولين في جدول واحد.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// فيما يلي طريقتان للحصول على جدول من مستند.
// 1 - من مجموعة \"Tables\" لعقدة Body:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 - باستخدام طريقة \"GetChild\":
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// إلحاق جميع الصفوف من الجدول الحالي إلى التالي.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// إزالة حاوية الجدول الفارغة.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## انظر أيضًا

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
