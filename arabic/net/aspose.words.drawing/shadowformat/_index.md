---
title: ShadowFormat Class
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Drawing.ShadowFormat لتحسين تأثيرات ظلال الكائنات. حسّن تصميم مستندك مع خيارات تنسيق ظلال قابلة للتخصيص.
type: docs
weight: 1620
url: /ar/net/aspose.words.drawing/shadowformat/
---
## ShadowFormat class

يمثل تنسيق الظل لكائن.

لمعرفة المزيد، قم بزيارة[العمل مع العناصر الرسومية](https://docs.aspose.com/words/net/working-with-graphic-elements/) مقالة توثيقية.

```csharp
public class ShadowFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Color](../../aspose.words.drawing/shadowformat/color/) { get; } | يحصل علىColor الكائن الذي يمثل لون الظل. القيمة الافتراضية هيBlack . |
| [Type](../../aspose.words.drawing/shadowformat/type/) { get; set; } | يحصل على المحدد أو يعينه[`ShadowType`](../shadowtype/) لـ ShadowFormat. |
| [Visible](../../aspose.words.drawing/shadowformat/visible/) { get; } | إرجاع`حقيقي` إذا كان التنسيق المطبق على هذه الحالة مرئيًا. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clear](../../aspose.words.drawing/shadowformat/clear/)() | يمسح تنسيق الظل. |

## أمثلة

يوضح كيفية الحصول على لون الظل.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
