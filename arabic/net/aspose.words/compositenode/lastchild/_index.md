---
title: CompositeNode.LastChild
linktitle: LastChild
articleTitle: LastChild
second_title: Aspose.Words لـ .NET
description: CompositeNode LastChild ملكية. يحصل على الطفل الأخير للعقدة في C#.
type: docs
weight: 50
url: /ar/net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

يحصل على الطفل الأخير للعقدة.

```csharp
public Node LastChild { get; }
```

## ملاحظات

إذا لم تكن هناك عقدة تابعة أخيرة، أ`باطل` تم إرجاعها.

## أمثلة

يوضح كيفية استخدام طريقتي Node وCompositeNode لإزالة قسم قبل القسم الأخير في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// كلا القسمين أشقاء لبعضهما البعض.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// إزالة قسم بناءً على علاقة الأخوة مع قسم آخر.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// القسم الذي أزلناه هو الأول، وتركنا الوثيقة مع الثاني فقط.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### أنظر أيضا

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
