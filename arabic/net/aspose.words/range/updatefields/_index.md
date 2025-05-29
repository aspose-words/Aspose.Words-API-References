---
title: Range.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مستنداتك بسهولة باستخدام طريقة Range UpdateFields، وتحديث قيم الحقول بسرعة وفعالية لتحسين الدقة.
type: docs
weight: 130
url: /ar/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

تحديث قيم حقول المستند في هذا النطاق.

```csharp
public void UpdateFields()
```

## ملاحظات

عند فتح مستند وتعديله ثم حفظه، لا يقوم Aspose.Words بتحديث الحقول تلقائيًا، بل يبقيها سليمة. لذلك، قد ترغب عادةً في استدعاء هذه الطريقة قبل الحفظ إذا قمت بتعديل document برمجيًا وتريد التأكد من ظهور قيم الحقول الصحيحة (المحسوبة) في المستند المحفوظ.

ليست هناك حاجة لتحديث الحقول بعد تنفيذ دمج البريد لأن دمج البريد هو نوع من تحديث الحقول ويقوم تلقائيًا بتحديث جميع الحقول في المستند.

لا تُحدِّث هذه الطريقة جميع أنواع الحقول. للاطلاع على قائمة مُفصَّلة بأنواع الحقول المدعومة، راجع دليل المبرمجين.

لا تقوم هذه الطريقة بتحديث الحقول المرتبطة بخوارزميات تخطيط الصفحة (على سبيل المثال PAGE وPAGES وPAGEREF). يتم تحديث الحقول المرتبطة بتخطيط الصفحة عند عرض مستند أو استدعاء[`UpdatePageLayout`](../../document/updatepagelayout/).

لتحديث الحقول في المستند بأكمله استخدم[`UpdateFields`](../../document/updatefields/).

## أمثلة

يوضح كيفية تحديث كافة الحقول في نطاق معين.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// ستعرض حقول DOCPROPERTY أعلاه قيمة خاصية المستند المضمنة هذه.
doc.BuiltInDocumentProperties.Category = "MyCategory";

// إذا قمنا بتحديث قيمة خاصية المستند، فسنحتاج إلى تحديث كافة حقول DOCPROPERTY لعرضها.
Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

//تحديث كافة الحقول الموجودة ضمن نطاق القسم الأول.
doc.FirstSection.Range.UpdateFields();

Assert.AreEqual("MyCategory", doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);
```

### أنظر أيضا

* class [Range](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
