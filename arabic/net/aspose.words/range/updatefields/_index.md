---
title: Range.UpdateFields
second_title: Aspose.Words لمراجع .NET API
description: Range طريقة. يقوم بتحديث قيم حقول المستند في هذا النطاق.
type: docs
weight: 120
url: /ar/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

يقوم بتحديث قيم حقول المستند في هذا النطاق.

```csharp
public void UpdateFields()
```

### ملاحظات

عند فتح مستند وتعديله ثم حفظه، لا يقوم Aspose.Words بتحديث الحقول تلقائيًا، بل يبقيها سليمة. لذلك، عادةً ما تريد استدعاء هذه الطريقة قبل الحفظ إذا قمت بتعديل document برمجيًا وتريد التأكد تظهر قيم الحقول المناسبة (المحسوبة) في المستند المحفوظ.

ليست هناك حاجة لتحديث الحقول بعد تنفيذ دمج البريد لأن دمج البريد هو نوع من تحديث الحقل ويقوم تلقائيًا بتحديث كافة الحقول في المستند.

لا يقوم هذا الأسلوب بتحديث كافة أنواع الحقول. للحصول على قائمة مفصلة بأنواع الحقول المدعومة، راجع دليل المبرمجين.

لا تقوم هذه الطريقة بتحديث الحقول المرتبطة بخوارزميات تخطيط الصفحة (مثل PAGE وPAGES وPAGEREF). يتم تحديث الحقول المرتبطة بتخطيط الصفحة عند عرض مستند أو الاتصال[`UpdatePageLayout`](../../document/updatepagelayout/).

لتحديث الحقول في استخدام الوثيقة بأكملها[`UpdateFields`](../../document/updatefields/).

### أمثلة

يوضح كيفية تحديث كافة الحقول في النطاق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// ستعرض حقول DOCPROPERTY أعلاه قيمة خاصية المستند المضمنة هذه.
doc.BuiltInDocumentProperties.Category = "MyCategory";

// إذا قمنا بتحديث قيمة خاصية مستند، فسنحتاج إلى تحديث جميع حقول DOCPROPERTY لعرضها.
Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

// قم بتحديث كافة الحقول الموجودة في نطاق القسم الأول.
doc.FirstSection.Range.UpdateFields();

Assert.AreEqual("MyCategory", doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);
```

### أنظر أيضا

* class [Range](../)
* مساحة الاسم [Aspose.Words](../../range/)
* المجسم [Aspose.Words](../../../)


