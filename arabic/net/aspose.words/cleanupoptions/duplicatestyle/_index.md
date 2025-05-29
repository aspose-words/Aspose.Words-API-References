---
title: CleanupOptions.DuplicateStyle
linktitle: DuplicateStyle
articleTitle: DuplicateStyle
second_title: Aspose.Words لـ .NET
description: حسّن مستنداتك باستخدام خاصية DuplicateStyle في CleanupOptions - أزل الأنماط المكررة بسهولة لتنسيق أنظف وأكثر كفاءة. القيمة الافتراضية هي "خطأ".
type: docs
weight: 20
url: /ar/net/aspose.words/cleanupoptions/duplicatestyle/
---
## CleanupOptions.DuplicateStyle property

يحصل على/يعين علامة تشير إلى ما إذا كان يجب إزالة الأنماط المكررة من المستند. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool DuplicateStyle { get; set; }
```

## أمثلة

يوضح كيفية إزالة الأنماط المكررة من المستند.

```csharp
Document doc = new Document();

// أضف نمطين إلى المستند بخصائص متطابقة،
// لكن بأسماء مختلفة. يُعتبر النمط الثاني نسخة مكررة من الأول.
Style myStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

Style duplicateStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle2");
duplicateStyle.Font.Size = 14;
duplicateStyle.Font.Name = "Courier New";
duplicateStyle.Font.Color = Color.Blue;

Assert.AreEqual(6, doc.Styles.Count);

// تطبيق كلا الأسلوبين على فقرات مختلفة داخل المستند.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

builder.ParagraphFormat.StyleName = duplicateStyle.Name;
builder.Writeln("Hello again!");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(duplicateStyle, paragraphs[1].ParagraphFormat.Style);

// قم بتكوين كائن CleanOptions، ثم اتصل بطريقة Cleanup لاستبدال جميع الأنماط المكررة
// مع الأصل وإزالة النسخ المكررة من المستند.
CleanupOptions cleanupOptions = new CleanupOptions { DuplicateStyle = true };

doc.Cleanup(cleanupOptions);

Assert.AreEqual(5, doc.Styles.Count);
Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(myStyle, paragraphs[1].ParagraphFormat.Style);
```

### أنظر أيضا

* class [CleanupOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
