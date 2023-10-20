---
title: Section.ClearContent
linktitle: ClearContent
articleTitle: ClearContent
second_title: Aspose.Words لـ .NET
description: Section ClearContent طريقة. مسح القسم في C#.
type: docs
weight: 90
url: /ar/net/aspose.words/section/clearcontent/
---
## Section.ClearContent method

مسح القسم.

```csharp
public void ClearContent()
```

## ملاحظات

نص[`Body`](../body/) تم مسحه، ولم يتبق سوى فقرة واحدة فارغة تمثل الفاصل المقطعي.

يتم مسح نص كافة الرؤوس والتذييلات، ولكن[`HeaderFooter`](../../headerfooter/) لا تتم إزالة الكائنات نفسها.

## أمثلة

يوضح كيفية مسح محتويات القسم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// سيؤدي تشغيل طريقة "ClearContent" إلى إزالة كافة محتويات القسم
// لكن اترك فقرة فارغة لإضافة محتوى مرة أخرى.
doc.FirstSection.ClearContent();

Assert.AreEqual(string.Empty, doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);
```

### أنظر أيضا

* class [Section](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
