---
title: DocumentBuilder.MoveToParagraph
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. تحريك المؤشر إلى فقرة في القسم الحالي.
type: docs
weight: 540
url: /ar/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

تحريك المؤشر إلى فقرة في القسم الحالي.

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| paragraphIndex | Int32 | فهرس الفقرة للانتقال إليها. |
| characterIndex | Int32 | فهرس الحرف داخل الفقرة . تسمح لك القيمة السالبة بتحديد موضع من نهاية الفقرة. استخدم -1 للانتقال إلى نهاية الفقرة. |

### ملاحظات

يتم إجراء التنقل داخل القصة الحالية للقسم الحالي. أي ، إذا قمت بنقل المؤشر إلى العنوان الرئيسي للقسم الأول ، ثم حدد فقرة الفهرس فهرس الفقرة داخل هذا العنوان من هذا القسم.

عندما تكون فقرة الفهرس أكبر من أو تساوي 0 ، فإنها تحدد فهرس from بداية القسم بحيث تكون القيمة 0 هي الفقرة الأولى. عندما تكون فقرة الفهرس أقل من 0 ، فإن تحدد فهرسًا من نهاية القسم بحيث تكون -1 هي الفقرة الأخيرة.

### أمثلة

يوضح كيفية نقل موضع مؤشر المنشئ إلى فقرة محددة.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// إنشاء منشئ مستند لتحرير المستند. مؤشر الباني ،
// وهي النقطة التي ستدرج فيها عقدًا جديدة عندما نسمي طرق بناء المستندات الخاصة بها ،
// حاليًا في بداية المستند.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// تحريك هذا المؤشر إلى فقرة مختلفة سيضع هذا المؤشر أمام تلك الفقرة.
builder.MoveToParagraph(2, 0);
// سيتم إدراج أي محتوى جديد نضيفه في تلك المرحلة.
builder.Writeln("This is a new third paragraph. ");
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


