---
title: Border.LineStyle
second_title: Aspose.Words لمراجع .NET API
description: Border ملكية. الحصول على نمط الحدود أو تعيينه .
type: docs
weight: 40
url: /ar/net/aspose.words/border/linestyle/
---
## Border.LineStyle property

الحصول على نمط الحدود أو تعيينه .

```csharp
public LineStyle LineStyle { get; set; }
```

### ملاحظات

إذا قمت بتعيين نمط الخط إلى لا شيء ، فسيتم تغيير عرض الخط تلقائيًا إلى صفر.

### أمثلة

يوضح كيفية إدراج سلسلة محاطة بحد في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### أنظر أيضا

* enum [LineStyle](../../linestyle/)
* class [Border](../)
* مساحة الاسم [Aspose.Words](../../border/)
* المجسم [Aspose.Words](../../../)


