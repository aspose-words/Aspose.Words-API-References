---
title: DocumentBase.PageColor
linktitle: PageColor
articleTitle: PageColor
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية لون صفحة DocumentBase لتخصيص لون صفحة مستندك بسهولة. بسّط التصميم مع هذه الميزة سهلة الاستخدام!
type: docs
weight: 70
url: /ar/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

يُحدِّد لون صفحة المستند أو يُحدِّده. هذه الخاصية هي نسخة أبسط من[`BackgroundShape`](../backgroundshape/) .

```csharp
public Color PageColor { get; set; }
```

## ملاحظات

توفر هذه الخاصية طريقة بسيطة لتحديد لون صفحة صلبة للمستند. يؤدي تعيين هذه الخاصية إلى إنشاء وتعيين لون صفحة مناسب[`BackgroundShape`](../backgroundshape/).

إذا لم يتم تعيين لون الصفحة (على سبيل المثال، لا يوجد شكل خلفية في المستند) returns Empty.

## أمثلة

يوضح كيفية تعيين لون الخلفية لجميع صفحات المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.PageColor = System.Drawing.Color.LightGray;

doc.Save(ArtifactsDir + "DocumentBase.SetPageColor.docx");
```

### أنظر أيضا

* class [DocumentBase](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
