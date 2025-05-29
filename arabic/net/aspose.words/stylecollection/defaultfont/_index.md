---
title: StyleCollection.DefaultFont
linktitle: DefaultFont
articleTitle: DefaultFont
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية StyleCollection DefaultFont لتنسيق نصوص المستندات بسلاسة. حسّن مستنداتك بأسلوب احترافي ومتناسق.
type: docs
weight: 20
url: /ar/net/aspose.words/stylecollection/defaultfont/
---
## StyleCollection.DefaultFont property

يحصل على تنسيق النص الافتراضي للمستند.

```csharp
public Font DefaultFont { get; }
```

## ملاحظات

لاحظ أنه تم تقديم الإعدادات الافتراضية على مستوى المستند في Microsoft Word 2007 وهي مدعومة بالكامل في تنسيقات OOXML (Docx) فقط. كانت تنسيقات المستندات السابقة تدعم هذه الميزة بشكل محدود ولا يمكن تخزين سوى أسماء الخطوط.

## أمثلة

يوضح كيفية إضافة نمط إلى مجموعة أنماط المستند.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// تعيين المعلمات الافتراضية للأنماط الجديدة التي قد نضيفها لاحقًا إلى هذه المجموعة.
styles.DefaultFont.Name = "Courier New";
// إذا أضفنا نمط "StyleType.Paragraph"، ستطبق المجموعة قيم
// خاصية "DefaultParagraphFormat" الخاصة بها إلى خاصية "ParagraphFormat" الخاصة بالنمط.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
//أضف نمطًا، ثم تأكد من أنه يحتوي على الإعدادات الافتراضية.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### أنظر أيضا

* class [Font](../../font/)
* class [StyleCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
