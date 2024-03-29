---
title: EndnoteOptions.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words لـ .NET
description: EndnoteOptions Position ملكية. يحدد موضع التعليقات الختامية في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.notes/endnoteoptions/position/
---
## EndnoteOptions.Position property

يحدد موضع التعليقات الختامية.

```csharp
public EndnotePosition Position { get; set; }
```

## أمثلة

يوضح كيفية تحديد مكان مختلف حيث يتم تجميع المستند وعرض تعليقاته الختامية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// التعليق الختامي هو وسيلة لإرفاق مرجع أو تعليق جانبي بالنص
 // لا يتعارض مع تدفق النص الأساسي.
// يؤدي إدراج تعليق ختامي إلى إضافة رمز مرجعي مرتفع صغير
// في النص الأساسي حيث نقوم بإدراج التعليق الختامي.
// تقوم كل حاشية ختامية أيضًا بإنشاء إدخال في نهاية المستند يتكون من رمز
// الذي يطابق الرمز المرجعي في النص الأساسي.
// النص المرجعي الذي نمرره إلى طريقة "InsertEndnote" الخاصة بمنشئ المستندات.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// يمكننا استخدام خاصية "الموضع" لتحديد المكان الذي ستضع فيه الوثيقة جميع تعليقاتها الختامية.
// إذا قمنا بتعيين قيمة خاصية "الموضع" على "EndnotePosition.EndOfDocument"،
// ستظهر كل حاشية سفلية في مجموعة في نهاية المستند. هذه هي القيمة الافتراضية.
// إذا قمنا بتعيين قيمة خاصية "الموضع" على "EndnotePosition.EndOfSection"،
// ستظهر كل حاشية سفلية في مجموعة في نهاية القسم الذي يحتوي نصه على العلامة المرجعية للتعليق الختامي.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

### أنظر أيضا

* enum [EndnotePosition](../../endnoteposition/)
* class [EndnoteOptions](../)
* مساحة الاسم [Aspose.Words.Notes](../../../aspose.words.notes/)
* المجسم [Aspose.Words](../../../)
