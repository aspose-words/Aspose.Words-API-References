---
title: LayoutFlow Enum
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Drawing.LayoutFlow للتحكم في تخطيط النص في مربعات النص، مما يعزز تصميم مستندك وقابليته للقراءة بسهولة.
type: docs
weight: 1430
url: /ar/net/aspose.words.drawing/layoutflow/
---
## LayoutFlow enumeration

يحدد تدفق تخطيط النص في مربع النص.

```csharp
public enum LayoutFlow
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Horizontal | `0` | يتم عرض النص أفقيًا. |
| TopToBottomIdeographic | `1` | يتم عرض النص الأيديوغرافي عموديًا. |
| BottomToTop | `2` | يتم عرض النص عموديًا. |
| TopToBottom | `3` | يتم عرض النص عموديًا. |
| HorizontalIdeographic | `4` | يتم عرض النص الأيديوغرافي أفقيًا. |
| Vertical | `5` | يتم عرض النص عموديًا. |

## أمثلة

يوضح كيفية إضافة نص إلى مربع نص وتغيير اتجاهه

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textbox = new Shape(doc, ShapeType.TextBox)
{
    Width = 100,
    Height = 100
};
textbox.TextBox.LayoutFlow = LayoutFlow.BottomToTop;

textbox.AppendChild(new Paragraph(doc));
builder.InsertNode(textbox);

builder.MoveTo(textbox.FirstParagraph);
builder.Write("This text is flipped 90 degrees to the left.");

doc.Save(ArtifactsDir + "Drawing.TextBox.docx");
```

### أنظر أيضا

* property [LayoutFlow](../textbox/layoutflow/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
