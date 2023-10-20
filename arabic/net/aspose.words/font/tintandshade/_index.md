---
title: Font.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words لـ .NET
description: Font TintAndShade ملكية. الحصول على أو تعيين قيمة مزدوجة تعمل على تفتيح اللون أو تغميقه في C#.
type: docs
weight: 520
url: /ar/net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

الحصول على أو تعيين قيمة مزدوجة تعمل على تفتيح اللون أو تغميقه.

```csharp
public double TintAndShade { get; set; }
```

## ملاحظات

تتراوح القيم المسموح بها من -1 (الأغمق) إلى 1 (الأفتح) لهذه الخاصية. الصفر (0) محايد. محاولة تعيين هذه الخاصية إلى قيمة أقل من -1 أو أكثر من 1 تؤدي إلىArgumentOutOfRangeException.

تعيين هذه الخاصية ل[`Font`](../) كائن ذو ألوان غير موضوعية يؤدي إلى aInvalidOperationException.

## أمثلة

يوضح كيفية إنشاء واستخدام النمط الموضوعي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// قم بإنشاء نمط ما باستخدام خصائص خط السمة.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
