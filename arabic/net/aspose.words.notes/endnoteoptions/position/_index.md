---
title: EndnoteOptions.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية EndnoteOptions Position تخطيط مستندك بتحديد الموضع الأمثل للملاحظات الختامية. حسّن كتابتك اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words.notes/endnoteoptions/position/
---
## EndnoteOptions.Position property

يحدد موضع الملاحظات الختامية.

```csharp
public EndnotePosition Position { get; set; }
```

## أمثلة

يوضح كيفية تحديد مكان مختلف حيث يتم تجميع المستند وعرض ملاحظاته الختامية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// الحاشية الختامية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
 // لا يتعارض مع تدفق النص الرئيسي.
// يؤدي إدراج حاشية ختامية إلى إضافة رمز مرجعي علوي صغير
// في نص الموضوع الرئيسي حيث نقوم بإدراج الحاشية الختامية.
// كما أن كل حاشية ختامية تنشئ أيضًا إدخالاً في نهاية المستند، يتكون من رمز
// الذي يتطابق مع رمز المرجع في النص الرئيسي.
// نص المرجع الذي نمرره إلى طريقة "InsertEndnote" الخاصة بمنشئ المستند.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// يمكننا استخدام خاصية "الموضع" لتحديد المكان الذي ستضع فيه الوثيقة جميع ملاحظاتها الختامية.
// إذا قمنا بتعيين قيمة خاصية "Position" إلى "EndnotePosition.EndOfDocument"،
// ستظهر كل حاشية سفلية في مجموعة في نهاية المستند. هذه هي القيمة الافتراضية.
// إذا قمنا بتعيين قيمة خاصية "Position" إلى "EndnotePosition.EndOfSection"،
// ستظهر كل حاشية سفلية في مجموعة في نهاية القسم الذي يحتوي نصه على علامة مرجع الحاشية السفلية.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

### أنظر أيضا

* enum [EndnotePosition](../../endnoteposition/)
* class [EndnoteOptions](../)
* مساحة الاسم [Aspose.Words.Notes](../../../aspose.words.notes/)
* المجسم [Aspose.Words](../../../)
