---
title: Fill.Solid
second_title: Aspose.Words لمراجع .NET API
description: Fill طريقة. يضبط التعبئة على لون موحد.
type: docs
weight: 260
url: /ar/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

يضبط التعبئة على لون موحد.

```csharp
public void Solid()
```

### ملاحظات

استخدم هذه الطريقة لتحويل أي من عمليات التعبئة مرة أخرى إلى تعبئة صلبة.

### أنظر أيضا

* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../fill/)
* المجسم [Aspose.Words](../../../)

---

## Solid(Color) {#solid_1}

يضبط التعبئة على لون موحد محدد.

```csharp
public void Solid(Color color)
```

### ملاحظات

استخدم هذه الطريقة لتحويل أي من عمليات التعبئة مرة أخرى إلى تعبئة صلبة.

### أمثلة

يوضح كيفية تحويل أي من عمليات التعبئة مرة أخرى إلى تعبئة صلبة.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// احصل على كائن التعبئة لخط التشغيل الأول.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// التحقق من خصائص التعبئة للخط.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// قم بتغيير نوع التعبئة إلى صلب بلون أخضر موحد.
fill.Solid(Color.Green);
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### أنظر أيضا

* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../fill/)
* المجسم [Aspose.Words](../../../)


