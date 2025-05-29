---
title: Range.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية نطاق النص لاسترجاع النص ومعالجته بسهولة ضمن نطاق محدد لتحسين إدارة المحتوى.
type: docs
weight: 60
url: /ar/net/aspose.words/range/text/
---
## Range.Text property

يحصل على نص النطاق.

```csharp
public string Text { get; }
```

## ملاحظات

تتضمن السلسلة المرتجعة جميع أحرف التحكم والأحرف الخاصة كما هو موضح في[`ControlChar`](../../controlchar/).

## أمثلة

يوضح كيفية الحصول على محتويات النص لجميع العقد التي يغطيها النطاق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### أنظر أيضا

* class [Range](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
