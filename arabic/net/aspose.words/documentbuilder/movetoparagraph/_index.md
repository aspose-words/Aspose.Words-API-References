---
title: DocumentBuilder.MoveToParagraph
linktitle: MoveToParagraph
articleTitle: MoveToParagraph
second_title: Aspose.Words لـ .NET
description: DocumentBuilder MoveToParagraph طريقة. ينقل المؤشر إلى فقرة في القسم الحالي في C#.
type: docs
weight: 560
url: /ar/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

ينقل المؤشر إلى فقرة في القسم الحالي.

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| paragraphIndex | Int32 | فهرس الفقرة المراد الانتقال إليها. |
| characterIndex | Int32 | فهرس الحرف الموجود داخل الفقرة. القيمة السالبة تسمح لك بتحديد موضع من نهاية الفقرة. استخدم -1 للانتقال إلى نهاية الفقرة. |

## ملاحظات

يتم تنفيذ التنقل داخل القصة الحالية للقسم الحالي. أي إذا قمت بتحريك المؤشر إلى الرأس الأساسي للقسم الأول، ثم*paragraphIndex*حدد فهرس الفقرة الموجودة داخل ذلك header لهذا القسم.

متى*paragraphIndex* أكبر من أو يساوي 0، فهو يحدد فهرس from بداية القسم حيث يكون 0 هو الفقرة الأولى. متى*paragraphIndex* أقل من 0, وقد حددت فهرسًا من نهاية القسم حيث تكون -1 هي الفقرة الأخيرة.

## أمثلة

يوضح كيفية نقل موضع مؤشر المنشئ إلى فقرة محددة.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// قم بإنشاء منشئ المستندات لتحرير المستند. مؤشر البناء،
// وهي النقطة التي سيتم فيها إدراج عقد جديدة عندما نطلق على طرق إنشاء المستند الخاصة بها،
// موجود حاليًا في بداية المستند.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// سيؤدي نقل هذا المؤشر إلى فقرة مختلفة إلى وضع هذا المؤشر أمام تلك الفقرة.
builder.MoveToParagraph(2, 0);
// سيتم إدراج أي محتوى جديد نضيفه عند هذه النقطة.
builder.Writeln("This is a new third paragraph. ");
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
