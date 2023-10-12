---
title: Font.Kerning
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. الحصول على أو تعيين حجم الخط الذي يبدأ عنده تقنين الأحرف.
type: docs
weight: 180
url: /ar/net/aspose.words/font/kerning/
---
## Font.Kerning property

الحصول على أو تعيين حجم الخط الذي يبدأ عنده تقنين الأحرف.

```csharp
public double Kerning { get; set; }
```

### أمثلة

يوضح كيفية تحديد حجم الخط الذي يبدأ عنده تطبيق تقنين الأحرف.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// قم بتعيين حجم خط المنشئ، والحد الأدنى للحجم الذي سيتم تفعيل تقنين الأحرف عنده.
// يقع حجم الخط تحت عتبة تقنين الأحرف، وبالتالي فإن التشغيل أدناه لن يحتوي على تقنين.
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// قم بتعيين حد تقنين الأحرف بحيث يكون حجم الخط الحالي للمنشئ أعلى منه.
// أي نص نضيفه من هذه النقطة سيتم تطبيق تقنين الأحرف عليه. المسافات بين الحروف
// سيتم تعديله، مما يؤدي عادةً إلى تشغيل نص أكثر جمالاً قليلاً.
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


