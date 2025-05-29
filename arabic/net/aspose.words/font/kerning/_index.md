---
title: Font.Kerning
linktitle: Kerning
articleTitle: Kerning
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية تباعد الأحرف في الخط، وتحكم في وقت بدء التباعد لضمان وضوح النص وتصميمه الأمثل. حسّن دقة طباعتك!
type: docs
weight: 180
url: /ar/net/aspose.words/font/kerning/
---
## Font.Kerning property

يحصل على حجم الخط الذي يبدأ عنده التباعد بين الأحرف أو يعينه.

```csharp
public double Kerning { get; set; }
```

## أمثلة

يوضح كيفية تحديد حجم الخط الذي يبدأ عنده تأثير التباعد بين الأحرف.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// تعيين حجم الخط الخاص بالمنشئ، والحجم الأدنى الذي سيتم عنده تطبيق التباعد بين الأحرف.
// يقع حجم الخط أسفل عتبة التباعد بين الأحرف، لذا فإن الخط أدناه لن يحتوي على تباعد بين الأحرف.
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// قم بتعيين حد التباعد بين الأحرف بحيث يكون حجم الخط الحالي للمنشئ أعلى منه.
// أي نص نضيفه من هذه النقطة سيتم تطبيق التباعد بين الأحرف.
//سيتم تعديله، مما يؤدي عادةً إلى تشغيل نص أكثر جمالية إلى حد ما.
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
