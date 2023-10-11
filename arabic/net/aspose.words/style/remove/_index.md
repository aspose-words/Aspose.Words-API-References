---
title: Style.Remove
second_title: Aspose.Words لمراجع .NET API
description: Style طريقة. إزالة النمط المحدد من المستند.
type: docs
weight: 200
url: /ar/net/aspose.words/style/remove/
---
## Style.Remove method

إزالة النمط المحدد من المستند.

```csharp
public void Remove()
```

### ملاحظات

إزالة النمط لها التأثيرات التالية على طراز المستند:

* تتم إزالة جميع المراجع إلى النمط من الفقرات والجداول والجداول المقابلة.
* إذا تمت إزالة النمط الأساسي، فسيتم نقل تنسيقه إلى الأنماط الفرعية.
* إذا كان النمط المراد حذفه يحتوي على نمط مرتبط، فسيتم حذف كليهما.

### أمثلة

يوضح كيفية إنشاء نمط مخصص وتطبيقه.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// إعادة تعريف النمط تلقائيًا.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتطبيق أحد الأنماط من المستند على الفقرة التي يقوم منشئ المستند بإنشائها.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// قم بإزالة النمط المخصص لدينا من مجموعة أنماط المستند.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// أي نص يستخدم نمطًا تمت إزالته يعود إلى التنسيق الافتراضي.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### أنظر أيضا

* class [Style](../)
* مساحة الاسم [Aspose.Words](../../style/)
* المجسم [Aspose.Words](../../../)


