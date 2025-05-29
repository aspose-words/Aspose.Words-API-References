---
title: ShadowFormat.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: استكشف خاصية "نوع تنسيق الظل" لتخصيص تأثيرات الظل بسهولة. احصل على "نوع الظل" أو عيّنه لتحسين مرونة التصميم.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/shadowformat/type/
---
## ShadowFormat.Type property

يحصل على المحدد أو يعينه[`ShadowType`](../../shadowtype/) لـ ShadowFormat.

```csharp
public ShadowType Type { get; set; }
```

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

* enum [ShadowType](../../shadowtype/)
* class [ShadowFormat](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
