---
title: BorderCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words لـ .NET
description: BorderCollection GetEnumerator طريقة. يُرجع كائن العداد الذي يمكن استخدامه للتكرار عبر كافة الحدود في المجموعة في C#.
type: docs
weight: 160
url: /ar/net/aspose.words/bordercollection/getenumerator/
---
## BorderCollection.GetEnumerator method

يُرجع كائن العداد الذي يمكن استخدامه للتكرار عبر كافة الحدود في المجموعة.

```csharp
public IEnumerator<Border> GetEnumerator()
```

## أمثلة

يوضح كيفية التكرار وتحرير كل الحدود في كائن تنسيق الفقرة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتكوين إعدادات تنسيق الفقرة الخاصة بالمنشئ لإنشاء حد موجة خضراء من جميع الجوانب.
BorderCollection borders = builder.ParagraphFormat.Borders;

using (IEnumerator<Border> enumerator = borders.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Border border = enumerator.Current;
        border.Color = Color.Green;
        border.LineStyle = LineStyle.Wave;
        border.LineWidth = 3;
    }
}

// أدخل فقرة. ستحدد إعدادات الحدود لدينا مظهر حدودها.
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "BorderCollection.GetBordersEnumerator.docx");
```

### أنظر أيضا

* class [Border](../../border/)
* class [BorderCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
