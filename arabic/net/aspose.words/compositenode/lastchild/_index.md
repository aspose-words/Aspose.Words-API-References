---
title: CompositeNode.LastChild
linktitle: LastChild
articleTitle: LastChild
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية CompositeNode LastChild للوصول بسهولة إلى آخر عقدة فرعية ومعالجتها، مما يؤدي إلى تحسين إدارة بنية البيانات لديك.
type: docs
weight: 50
url: /ar/net/aspose.words/compositenode/lastchild/
---
## CompositeNode.LastChild property

يحصل على آخر طفل للعقدة.

```csharp
public Node LastChild { get; }
```

## ملاحظات

إذا لم تكن هناك عقدة فرعية أخيرة،`باطل` تم إرجاعه.

## أمثلة

يوضح كيفية استخدام طرق Node و CompositeNode لإزالة قسم قبل القسم الأخير في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1 text.");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("Section 2 text.");

// كلا القسمين شقيقان لبعضهما البعض.
Section lastSection = (Section)doc.LastChild;
Section firstSection = (Section)lastSection.PreviousSibling;

// قم بإزالة قسم بناءً على علاقته الشقيقة بقسم آخر.
if (lastSection.PreviousSibling != null)
    doc.RemoveChild(firstSection);

// القسم الذي قمنا بإزالته هو القسم الأول، ولم يتبق للمستند سوى القسم الثاني.
Assert.AreEqual("Section 2 text.", doc.GetText().Trim());
```

### أنظر أيضا

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
