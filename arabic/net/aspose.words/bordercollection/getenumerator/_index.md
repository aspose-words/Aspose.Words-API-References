---
title: BorderCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة BorderCollection GetEnumerator للتنقل بسهولة عبر كافة الحدود، مما يعزز كفاءة الترميز وإدارة المجموعة.
type: docs
weight: 160
url: /ar/net/aspose.words/bordercollection/getenumerator/
---
## BorderCollection.GetEnumerator method

يعيد كائن عداد يمكن استخدامه للتكرار عبر جميع الحدود في المجموعة.

```csharp
public IEnumerator<Border> GetEnumerator()
```

## أمثلة

يوضح كيفية تكرار وتحرير كافة الحدود في كائن تنسيق الفقرة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتكوين إعدادات تنسيق فقرة المنشئ لإنشاء حدود موجة خضراء على جميع الجوانب.
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

// أدرج فقرة. إعدادات حدودنا ستحدد مظهر حدودها.
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "BorderCollection.GetBordersEnumerator.docx");
```

### أنظر أيضا

* class [Border](../../border/)
* class [BorderCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
