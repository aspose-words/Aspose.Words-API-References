---
title: "طريقة Aspose::Words::DocumentBuilder::MoveToCell"
linktitle: "MoveToCell"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::MoveToCell. ينقل المؤشر إلى خلية جدول في القسم الحالي في C++."
type: docs
weight: 53000
url: /ar/cpp/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder::MoveToCell method


ينقل المؤشر إلى خلية جدول في القسم الحالي.

```cpp
void Aspose::Words::DocumentBuilder::MoveToCell(int32_t tableIndex, int32_t rowIndex, int32_t columnIndex, int32_t characterIndex)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| tableIndex | int32_t | فهرس الجدول للانتقال إليه. |
| rowIndex | int32_t | فهرس الصف في الجدول. |
| columnIndex | int32_t | فهرس العمود في الجدول. |
| characterIndex | int32_t | فهرس الحرف داخل الخلية. القيمة السالبة تسمح بتحديد موضع من نهاية الخلية. استخدم -1 للانتقال إلى نهاية الخلية. |
## ملاحظات


يتم تنفيذ التنقل داخل القصة الحالية للقسم الحالي.

بالنسبة إلى معلمات الفهرس، عندما يكون الفهرس أكبر من أو يساوي 0، فإنه يحدد فهرسًا من البداية حيث 0 هو العنصر الأول. عندما يكون الفهرس أقل من 0، فإنه يحدد فهرسًا من النهاية حيث -1 هو العنصر الأخير.

## أمثلة



يوضح كيفية نقل مؤشر منشئ المستند إلى خلية في جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء جدول فارغ 2×2.
builder->StartTable();
builder->InsertCell();
builder->InsertCell();
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

// لأننا أنهينا الجدول باستخدام طريقة EndTable،
// مؤشر منشئ المستند حاليًا خارج الجدول.
// هذا المؤشر له نفس وظيفة مؤشر النص الوامض في Microsoft Word.
// يمكن أيضًا نقله إلى موقع مختلف في المستند باستخدام طرق MoveTo للمنشئ.
// يمكننا نقل المؤشر مرة أخرى داخل الجدول إلى خلية محددة.
builder->MoveToCell(0, 1, 1, 0);
builder->Write(u"Column 2, cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MoveToCell.docx");
```

## انظر أيضًا

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
