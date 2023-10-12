---
title: BorderCollection.ClearFormatting
second_title: Aspose.Words لمراجع .NET API
description: BorderCollection طريقة. إزالة كافة حدود الكائن.
type: docs
weight: 140
url: /ar/net/aspose.words/bordercollection/clearformatting/
---
## BorderCollection.ClearFormatting method

إزالة كافة حدود الكائن.

```csharp
public void ClearFormatting()
```

### أمثلة

يوضح كيفية إزالة كافة الحدود من جميع الفقرات في المستند.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

// تحتوي الفقرة الأولى من هذا المستند على حدود مرئية بهذه الإعدادات.
BorderCollection firstParagraphBorders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), firstParagraphBorders.Color.ToArgb());
Assert.AreEqual(LineStyle.Single, firstParagraphBorders.LineStyle);
Assert.AreEqual(3.0d, firstParagraphBorders.LineWidth);

// استخدم طريقة "ClearFormatting" في كل فقرة لإزالة كافة الحدود.
foreach (Paragraph paragraph in doc.FirstSection.Body.Paragraphs)
{
    paragraph.ParagraphFormat.Borders.ClearFormatting();

    foreach (Border border in paragraph.ParagraphFormat.Borders)
    {
        Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
        Assert.AreEqual(LineStyle.None, border.LineStyle);
        Assert.AreEqual(0.0d, border.LineWidth);
    }
}

doc.Save(ArtifactsDir + "BorderCollection.RemoveAllBorders.docx");
```

### أنظر أيضا

* class [BorderCollection](../)
* مساحة الاسم [Aspose.Words](../../bordercollection/)
* المجسم [Aspose.Words](../../../)


