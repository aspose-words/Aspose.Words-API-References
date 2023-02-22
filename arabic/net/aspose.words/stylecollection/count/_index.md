---
title: StyleCollection.Count
second_title: Aspose.Words لمراجع .NET API
description: StyleCollection ملكية. الحصول على عدد الأنماط في المجموعة.
type: docs
weight: 10
url: /ar/net/aspose.words/stylecollection/count/
---
## StyleCollection.Count property

الحصول على عدد الأنماط في المجموعة.

```csharp
public int Count { get; }
```

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

* class [StyleCollection](../)
* مساحة الاسم [Aspose.Words](../../stylecollection/)
* المجسم [Aspose.Words](../../../)


