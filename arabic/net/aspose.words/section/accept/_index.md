---
title: Section.Accept
second_title: Aspose.Words لمراجع .NET API
description: Section طريقة. يقبل الزائر .
type: docs
weight: 70
url: /ar/net/aspose.words/section/accept/
---
## Section.Accept method

يقبل الزائر .

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| visitor | DocumentVisitor | الزائر الذي سيزور العقد. |

### قيمة الإرجاع

صحيح إذا تمت زيارة جميع العقد ؛ خطأ إذا أوقف برنامج DocumentVisitor العملية قبل زيارة جميع العقد.

### ملاحظات

يعدّ فوق هذه العقدة وجميع توابعها. تستدعي كل عقدة طريقة مقابلة في DocumentVisitor.

لمزيد من المعلومات ، راجع نمط تصميم الزائر.

Calls DocumentVisitor.VisitSectionStart ، ثم استدعاء Accept لجميع العقد الفرعية من section واستدعاء DocumentVisitor.VisitSectionEnd في النهاية.

### أنظر أيضا

* class [DocumentVisitor](../../documentvisitor/)
* class [Section](../)
* مساحة الاسم [Aspose.Words](../../section/)
* المجسم [Aspose.Words](../../../)


