---
title: StyleCollection.DefaultParagraphFormat
linktitle: DefaultParagraphFormat
articleTitle: DefaultParagraphFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية StyleCollection DefaultParagraphFormat للوصول بسهولة إلى تنسيق الفقرة الافتراضية للمستند وتخصيصها لتحسين قابلية القراءة.
type: docs
weight: 30
url: /ar/net/aspose.words/stylecollection/defaultparagraphformat/
---
## StyleCollection.DefaultParagraphFormat property

يحصل على تنسيق الفقرة الافتراضي للمستند.

```csharp
public ParagraphFormat DefaultParagraphFormat { get; }
```

## ملاحظات

لاحظ أنه تم تقديم الإعدادات الافتراضية على مستوى المستند في Microsoft Word 2007 وهي مدعومة بالكامل في تنسيقات OOXML (Docx) فقط. لا تدعم تنسيقات المستندات السابقة تنسيق الفقرة الافتراضية للمستند.

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

* class [ParagraphFormat](../../paragraphformat/)
* class [StyleCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
