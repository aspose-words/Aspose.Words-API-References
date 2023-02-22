---
title: StyleCollection.DefaultParagraphFormat
second_title: Aspose.Words لمراجع .NET API
description: StyleCollection ملكية. الحصول على تنسيق الفقرة الافتراضي للوثيقة.
type: docs
weight: 30
url: /ar/net/aspose.words/stylecollection/defaultparagraphformat/
---
## StyleCollection.DefaultParagraphFormat property

الحصول على تنسيق الفقرة الافتراضي للوثيقة.

```csharp
public ParagraphFormat DefaultParagraphFormat { get; }
```

### ملاحظات

لاحظ أنه تم تقديم الإعدادات الافتراضية على مستوى المستند في Microsoft Word 2007 وهي مدعومة بالكامل في تنسيقات OOXML (Docx) only. لا تدعم تنسيقات المستندات السابقة التنسيق الافتراضي للفقرة في المستند.

### أمثلة

يوضح كيفية إضافة نمط إلى مجموعة أنماط المستند.

```csharp
Document doc = new Document();
StyleCollection styles = doc.Styles;

// تعيين المعلمات الافتراضية للأنماط الجديدة التي قد نضيفها لاحقًا إلى هذه المجموعة.
styles.DefaultFont.Name = "Courier New";

// إذا أضفنا نمطًا من "StyleType.Paragraph" ، فستطبق المجموعة قيم
// الخاصية "DefaultParagraphFormat" الخاصة بها إلى خاصية "تنسيق ParagraphFormat" الخاصة بالنمط.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;

// أضف نمطًا ، ثم تحقق من أنه يحتوي على الإعدادات الافتراضية.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### أنظر أيضا

* class [ParagraphFormat](../../paragraphformat/)
* class [StyleCollection](../)
* مساحة الاسم [Aspose.Words](../../stylecollection/)
* المجسم [Aspose.Words](../../../)


