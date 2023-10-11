---
title: DocumentBase.PageColor
second_title: Aspose.Words لمراجع .NET API
description: DocumentBase ملكية. الحصول على أو تعيين لون صفحة المستند. هذه الخاصية هي نسخة أبسط منBackgroundShape .
type: docs
weight: 60
url: /ar/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

الحصول على أو تعيين لون صفحة المستند. هذه الخاصية هي نسخة أبسط من[`BackgroundShape`](../backgroundshape/) .

```csharp
public Color PageColor { get; set; }
```

### ملاحظات

توفر هذه الخاصية طريقة بسيطة لتحديد لون صفحة خالص للمستند. يؤدي تعيين هذه الخاصية إلى إنشاء وتعيين لون مناسب[`BackgroundShape`](../backgroundshape/).

إذا لم يتم تعيين لون الصفحة (على سبيل المثال، لا يوجد شكل خلفية في المستند) ترجع Empty.

### أمثلة

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
* مساحة الاسم [Aspose.Words](../../documentbase/)
* المجسم [Aspose.Words](../../../)


