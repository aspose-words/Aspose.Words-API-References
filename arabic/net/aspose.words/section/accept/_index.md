---
title: Section.Accept
second_title: Aspose.Words لمراجع .NET API
description: Section طريقة. يقبل الزائر.
type: docs
weight: 70
url: /ar/net/aspose.words/section/accept/
---
## Section.Accept method

يقبل الزائر.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| visitor | DocumentVisitor | الزائر الذي سيزور العقد. |

### قيمة الإرجاع

صحيح إذا تمت زيارة جميع العقد؛ كاذبة إذا[`DocumentVisitor`](../../documentvisitor/) أوقفت العملية قبل زيارة كافة العقد.

### ملاحظات

يعدد هذه العقدة وجميع أبنائها. تستدعي كل عقدة الطريقة المقابلة لها[`DocumentVisitor`](../../documentvisitor/).

لمزيد من المعلومات، راجع نمط تصميم الزائر.

المكالمات[`VisitSectionStart`](../../documentvisitor/visitsectionstart/) ، ثم يتصل[`Accept`](../../node/accept/) لجميع العقد التابعة للقسم والمكالمات[`VisitSectionEnd`](../../documentvisitor/visitsectionend/) في النهاية.

### أنظر أيضا

* class [DocumentVisitor](../../documentvisitor/)
* class [Section](../)
* مساحة الاسم [Aspose.Words](../../section/)
* المجسم [Aspose.Words](../../../)


