---
title: "Aspose::Words::Tables::CellFormat::SetPaddings طريقة"
linktitle: "SetPaddings"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::CellFormat::SetPaddings طريقة. تُعيّن مقدار المسافة (بالنقاط) لإضافتها إلى اليسار/الأعلى/اليمين/الأسفل من محتويات الخلية في C++."
type: docs
weight: 31000
url: /ar/cpp/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat::SetPaddings method


يضبط مقدار المسافة (بالنقاط) لإضافتها إلى اليسار/الأعلى/اليمين/الأسفل لمحتويات الخلية.

```cpp
void Aspose::Words::Tables::CellFormat::SetPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


## أمثلة



يعرض كيفية إضافة مسافات إلى محتويات خلية باستخدام الفراغ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// حدد مسافة الحشو (بالنقاط) بين الحد ومحتوى النص
// لكل خلية جدول نقوم بإنشائها باستخدام مُنشئ المستند.
builder->get_CellFormat()->SetPaddings(5, 10, 40, 50);

// أنشئ جدولاً بخلية واحدة يكون محتواها محاطاً بحشو فراغ.
builder->StartTable();
builder->InsertCell();
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"CellFormat.Padding.docx");
```

## انظر أيضًا

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
