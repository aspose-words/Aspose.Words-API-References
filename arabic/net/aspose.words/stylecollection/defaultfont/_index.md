---
title: StyleCollection.DefaultFont
linktitle: DefaultFont
articleTitle: DefaultFont
second_title: Aspose.Words لـ .NET
description: StyleCollection DefaultFont ملكية. الحصول على تنسيق النص الافتراضي للمستند في C#.
type: docs
weight: 20
url: /ar/net/aspose.words/stylecollection/defaultfont/
---
## StyleCollection.DefaultFont property

الحصول على تنسيق النص الافتراضي للمستند.

```csharp
public Font DefaultFont { get; }
```

## ملاحظات

لاحظ أنه تم تقديم الإعدادات الافتراضية على مستوى المستند في Microsoft Word 2007 وهي مدعومة بالكامل بتنسيقات OOXML (Docx) فقط. تتمتع تنسيقات المستندات السابقة بدعم محدود لهذه الميزة ويمكن تخزين أسماء الخطوط فقط.

## أمثلة

يوضح كيفية إضافة نمط إلى مجموعة أنماط المستند.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// قم بتعيين المعلمات الافتراضية للأنماط الجديدة التي قد نضيفها لاحقًا إلى هذه المجموعة.
styles.DefaultFont.Name = "Courier New";
// إذا أضفنا نمطًا من "StyleType.Paragraph"، فستطبق المجموعة قيم
// الخاصية "DefaultParagraphFormat" الخاصة بها إلى خاصية "ParagraphFormat" الخاصة بالنمط.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// أضف نمطًا، ثم تحقق من أنه يحتوي على الإعدادات الافتراضية.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### أنظر أيضا

* class [Font](../../font/)
* class [StyleCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
