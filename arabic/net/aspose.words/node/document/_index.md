---
title: Node.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية مستند العقدة، وقم بالوصول بسهولة إلى المستند المرتبط بالعقدة الخاصة بك لإدارة البيانات بسلاسة وتعزيز الإنتاجية.
type: docs
weight: 20
url: /ar/net/aspose.words/node/document/
---
## Node.Document property

يحصل على المستند الذي تنتمي إليه هذه العقدة.

```csharp
public virtual DocumentBase Document { get; }
```

## ملاحظات

تنتمي العقدة دائمًا إلى مستند حتى لو تم إنشاؤها للتو ولم تتم إضافتها إلى الشجرة بعد، أو إذا تمت إزالتها من الشجرة.

## أمثلة

يوضح كيفية إنشاء عقدة وتعيين المستند الخاص بها.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// لم نقم بعد بإضافة هذه الفقرة كفقرة فرعية إلى أي عقدة مركبة.
Assert.IsNull(para.ParentNode);

// إذا كانت العقدة هي نوع عقدة فرعية مناسب لعقدة مركبة أخرى،
// يمكننا إرفاقه كطفل فقط إذا كان لدى كلتا العقدتين نفس مستند المالك.
//مستند المالك هو المستند الذي مررناه إلى منشئ العقدة.
// لم نقم بإرفاق هذه الفقرة بالمستند، وبالتالي فإن المستند لا يحتوي على نصها.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// بما أن المستند يمتلك هذه الفقرة، فيمكننا تطبيق أحد أنماطه على محتويات الفقرة.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

//أضف هذه العقدة إلى المستند، ثم تحقق من محتوياته.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### أنظر أيضا

* class [DocumentBase](../../documentbase/)
* class [Node](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
