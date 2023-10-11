---
title: Range.Text
second_title: Aspose.Words لمراجع .NET API
description: Range ملكية. يحصل على نص النطاق.
type: docs
weight: 60
url: /ar/net/aspose.words/range/text/
---
## Range.Text property

يحصل على نص النطاق.

```csharp
public string Text { get; }
```

### ملاحظات

تتضمن السلسلة التي تم إرجاعها جميع عناصر التحكم والأحرف الخاصة كما هو موضح في[`ControlChar`](../../controlchar/).

### أمثلة

يوضح كيفية الحصول على محتويات النص لجميع العقد التي يغطيها النطاق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### أنظر أيضا

* class [Range](../)
* مساحة الاسم [Aspose.Words](../../range/)
* المجسم [Aspose.Words](../../../)


