---
title: "طريقة Aspose::Words::Drawing::Charts::Chart::get_SourceFullName"
linktitle: "get_SourceFullName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Charts::Chart::get_SourceFullName. تحصل على المسار واسم ملف xls/xlsx المرتبط بهذا المخطط في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.drawing.charts/chart/get_sourcefullname/
---
## Chart::get_SourceFullName method


يحصل على مسار واسم ملف xls/xlsx المرتبط بهذا المخطط.

```cpp
System::String Aspose::Words::Drawing::Charts::Chart::get_SourceFullName()
```


## أمثلة



يوضح كيفية الحصول على الاسم الكامل أو تعيينه للمستند الخارجي xls/xlsx إذا كان المخطط مرتبطًا.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::String sourceFullName = shape->get_Chart()->get_SourceFullName();
ASSERT_TRUE(sourceFullName.Contains(u"Examples\\Data\\Spreadsheet.xlsx"));
```

## انظر أيضًا

* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
