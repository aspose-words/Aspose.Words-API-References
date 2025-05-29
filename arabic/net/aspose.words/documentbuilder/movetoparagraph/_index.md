---
title: DocumentBuilder.MoveToParagraph
linktitle: MoveToParagraph
articleTitle: MoveToParagraph
second_title: Aspose.Words لـ .NET
description: قم بالتنقل بسهولة في مستندك باستخدام طريقة MoveToParagraph في DocumentBuilder، مما يتيح لك تحريك المؤشر بسرعة إلى أي فقرة في قسمك.
type: docs
weight: 600
url: /ar/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

يحرك المؤشر إلى فقرة في القسم الحالي.

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| paragraphIndex | Int32 | فهرس الفقرة التي سيتم الانتقال إليها. |
| characterIndex | Int32 | فهرس الحرف داخل الفقرة. . تسمح لك القيمة السالبة بتحديد موضع من نهاية الفقرة. استخدم -1 للانتقال إلى نهاية الفقرة. |

## ملاحظات

يتم إجراء التنقل داخل القصة الحالية للقسم الحالي. أي إذا قمت بنقل المؤشر إلى العنوان الأساسي للقسم الأول، ثم*paragraphIndex* تم تحديد فهرس الفقرة داخل header لهذا القسم.

متى*paragraphIndex* أكبر من أو يساوي 0، فإنه يحدد فهرسًا من بداية القسم مع كون 0 هي الفقرة الأولى. عندما*paragraphIndex* أقل من 0، لقد حدد فهرسًا من نهاية القسم حيث -1 هي الفقرة الأخيرة.

## أمثلة

يوضح كيفية نقل موضع مؤشر المنشئ إلى فقرة محددة.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// أنشئ مُنشئ مستندات لتحرير المستند. مؤشر المُنشئ،
// وهي النقطة التي سيتم فيها إدراج عقد جديدة عندما نستدعي أساليب إنشاء المستندات الخاصة به،
//يوجد حاليًا في بداية المستند.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// نقل المؤشر إلى فقرة مختلفة سيضع المؤشر أمام تلك الفقرة.
builder.MoveToParagraph(2, 0);
// سيتم إدراج أي محتوى جديد نضيفه في تلك المرحلة.
builder.Writeln("This is a new third paragraph. ");
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
