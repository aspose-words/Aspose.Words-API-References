---
title: CompositeNode.RemoveChild
linktitle: RemoveChild
articleTitle: RemoveChild
second_title: Aspose.Words لـ .NET
description: قم بإدارة CompositeNode الخاص بك بسهولة باستخدام طريقة RemoveChild، المصممة لتبسيط إزالة العقد لتحسين الأداء والكفاءة.
type: docs
weight: 190
url: /ar/net/aspose.words/compositenode/removechild/
---
## CompositeNode.RemoveChild&lt;T&gt; method

يزيل العقدة الفرعية المحددة.

```csharp
public T RemoveChild<T>(T oldChild)
    where T : Node
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| oldChild | T | العقدة المراد إزالتها. |

### قيمة الإرجاع

العقدة التي تمت إزالتها.

## ملاحظات

والد*oldChild* تم ضبطه على`باطل` بعد إزالة العقدة.

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
