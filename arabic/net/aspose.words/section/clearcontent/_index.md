---
title: Section.ClearContent
linktitle: ClearContent
articleTitle: ClearContent
second_title: Aspose.Words لـ .NET
description: نظّف الأقسام بسهولة باستخدام طريقة ClearContent. حسّن سير عملك وحسّن كفاءة إدارة المحتوى اليوم!
type: docs
weight: 110
url: /ar/net/aspose.words/section/clearcontent/
---
## Section.ClearContent method

يمسح القسم.

```csharp
public void ClearContent()
```

## ملاحظات

نص[`Body`](../body/) إذا تم مسحها، تبقى فقرة فارغة واحدة فقط تمثل فاصل القسم.

تم مسح نص جميع الرؤوس والتذييلات، ولكن[`HeaderFooter`](../../headerfooter/) لا تتم إزالة الأشياء نفسها.

## أمثلة

يوضح كيفية مسح محتويات القسم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// سيؤدي تشغيل طريقة "ClearContent" إلى إزالة جميع محتويات القسم
// ولكن اترك فقرة فارغة لإضافة المحتوى مرة أخرى.
doc.FirstSection.ClearContent();

Assert.AreEqual(string.Empty, doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);
```

### أنظر أيضا

* class [Section](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
