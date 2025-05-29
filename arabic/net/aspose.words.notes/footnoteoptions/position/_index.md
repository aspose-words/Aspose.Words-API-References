---
title: FootnoteOptions.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية FootnoteOptions Position على تحسين تخطيط المستند الخاص بك من خلال التحكم بدقة في وضع الحاشية السفلية لتحسين إمكانية القراءة.
type: docs
weight: 30
url: /ar/net/aspose.words.notes/footnoteoptions/position/
---
## FootnoteOptions.Position property

يحدد موضع الحواشي السفلية.

```csharp
public FootnotePosition Position { get; set; }
```

## أمثلة

يوضح كيفية تحديد مكان مختلف لجمع المستند وعرض حواشيه السفلية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// الحاشية السفلية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
 // لا يتعارض مع تدفق النص الرئيسي.
// يؤدي إدراج حاشية سفلية إلى إضافة رمز مرجعي علوي صغير
// في نص الموضوع الرئيسي حيث نقوم بإدراج الحاشية السفلية.
// كما أن كل حاشية سفلية تنشئ إدخالاً في أسفل الصفحة، يتكون من رمز
// الذي يتطابق مع رمز المرجع في النص الرئيسي.
// نص المرجع الذي نمرره إلى طريقة "InsertFootnote" الخاصة بمنشئ المستند.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// يمكننا استخدام خاصية "الموضع" لتحديد المكان الذي ستضع فيه الوثيقة جميع حواشيها السفلية.
// إذا قمنا بتعيين قيمة خاصية "Position" إلى "FootnotePosition.BottomOfPage"،
// ستظهر كل حاشية سفلية أسفل الصفحة التي تحتوي على علامتها المرجعية. هذه هي القيمة الافتراضية.
// إذا قمنا بتعيين قيمة خاصية "Position" إلى "FootnotePosition.BeneathText"،
// ستظهر كل حاشية سفلية في نهاية نص الصفحة الذي يحتوي على علامة مرجعية لها.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### أنظر أيضا

* enum [FootnotePosition](../../footnoteposition/)
* class [FootnoteOptions](../)
* مساحة الاسم [Aspose.Words.Notes](../../../aspose.words.notes/)
* المجسم [Aspose.Words](../../../)
