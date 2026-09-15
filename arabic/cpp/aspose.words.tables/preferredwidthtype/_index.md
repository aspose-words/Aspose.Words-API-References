---
title: "Aspose::Words::Tables::PreferredWidthType enum"
linktitle: "PreferredWidthType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::PreferredWidthType enum. يحدد وحدة القياس للعرض المفضل لجدول أو خلية في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enum


يحدد وحدة القياس للعرض المفضل للجدول أو الخلية.

```cpp
enum class PreferredWidthType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| تلقائي | 1 | العرض المفضل غير محدد. العرض الفعلي للجدول أو الخلية إما يتم تحديده باستخدام العرض الصريح أو سيُحدد تلقائيًا بواسطة خوارزمية تخطيط الجدول عند عرض الجدول، اعتمادًا على إعداد الضبط التلقائي للجدول. |
| النسبة | 2 | قِس عرض العنصر الحالي باستخدام نسبة مئوية محددة. |
| نقاط | 3 | قِس عرض العنصر الحالي باستخدام عدد محدد من النقاط (1/72 بوصة). |


## أمثلة



يظهر كيفية التحقق من نوع العرض المفضل وقيمته لخلية جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(Aspose::Words::Tables::PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## انظر أيضًا

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
