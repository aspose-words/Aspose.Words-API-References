---
title: Style.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words لـ .NET
description: تخلص بسهولة من الأنماط غير المرغوب فيها في مستندك باستخدام طريقة "إزالة الأنماط". حسّن مظهر محتواك وحافظ على تناسقه!
type: docs
weight: 230
url: /ar/net/aspose.words/style/remove/
---
## Style.Remove method

يزيل النمط المحدد من المستند.

```csharp
public void Remove()
```

## ملاحظات

يؤدي إزالة النمط إلى التأثيرات التالية على نموذج المستند:

* تمت إزالة جميع الإشارات إلى الأسلوب من الفقرات والمسارات والجداول المقابلة.
* إذا تمت إزالة النمط الأساسي، فسيتم نقل تنسيقه إلى الأنماط الفرعية.
* إذا كان النمط الذي سيتم حذفه يحتوي على نمط مرتبط، فسيتم حذف كلا النمطين.

## أمثلة

يوضح كيفية إنشاء نمط مخصص وتطبيقه.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
//إعادة تعريف النمط تلقائيًا.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتطبيق أحد الأنماط الموجودة في المستند على الفقرة التي يقوم منشئ المستند بإنشائها.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
