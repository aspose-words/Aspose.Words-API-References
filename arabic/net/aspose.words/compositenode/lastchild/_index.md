---
title: CompositeNode.LastChild
second_title: Aspose.Words لمراجع .NET API
description: CompositeNode ملكية. الحصول على آخر تابع للعقدة .
type: docs
weight: 60
url: /ar/net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

الحصول على آخر تابع للعقدة .

```csharp
public Node LastChild { get; }
```

### ملاحظات

إذا لم تكن هناك عقدة فرعية أخيرة ، فسيتم إرجاع قيمة فارغة .

### أمثلة

يوضح كيفية استخدام طرق العقدة والعقدة المركبة لإزالة قسم قبل القسم الأخير في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// كلا القسمين أشقاء لبعضهما البعض.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// إزالة قسم بناءً على علاقته بأخيه مع قسم آخر.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// كان القسم الذي أزلناه هو الأول ، تاركًا المستند مع الثاني فقط.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### أنظر أيضا

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../compositenode/)
* المجسم [Aspose.Words](../../../)


