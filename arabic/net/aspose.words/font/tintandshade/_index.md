---
title: Font.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Font TintAndShade لتعديل الألوان بسهولة! خفّض أو غمّق درجات الألوان لتصاميم نابضة بالحياة. حسّن مشاريعك بسهولة!
type: docs
weight: 530
url: /ar/net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

يحصل على قيمة مزدوجة لتفتيح اللون أو تعتيمه أو تعيينها.

```csharp
public double TintAndShade { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | قم بالرمي إذا قمت بتعيين هذه الخاصية إلى قيمة أقل من -1 أو أكثر من 1. |
| InvalidOperationException | قم برمي إذا قمت بتعيين هذه الخاصية لـ[`Font`](../) كائن بألوان غير موضوعية. |

## ملاحظات

تتراوح القيم المسموح بها من -1 (الأغمق) إلى 1 (الأفتح) لهذه الخاصية.

الصفر (0) محايد.

## أمثلة

يوضح كيفية إنشاء النمط الموضوعي واستخدامه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// قم بإنشاء بعض الأنماط باستخدام خصائص الخط الخاص بالموضوع.
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
