---
title: EndnoteOptions.Position
second_title: Aspose.Words لمراجع .NET API
description: EndnoteOptions ملكية. يحدد موضع التعليقات الختامية .
type: docs
weight: 20
url: /ar/net/aspose.words.notes/endnoteoptions/position/
---
## EndnoteOptions.Position property

يحدد موضع التعليقات الختامية .

```csharp
public EndnotePosition Position { get; set; }
```

### أمثلة

يوضح كيفية تحديد مكان مختلف حيث يجمع المستند ويعرض التعليقات الختامية الخاصة به.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// التعليقات الختامية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
// لا يتعارض مع انسياب النص الأساسي الرئيسي. 
// يؤدي إدراج تعليق ختامي إلى إضافة رمز مرجعي صغير مرتفع
// في النص الأساسي الرئيسي حيث نقوم بإدخال التعليق الختامي.
// ينشئ كل تعليق ختامي أيضًا إدخالًا في نهاية المستند ، يتكون من رمز
// الذي يطابق رمز المرجع في النص الأساسي الرئيسي.
// النص المرجعي الذي نمرره إلى طريقة "InsertEndnote" لمنشئ المستندات.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote contents.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("This is the second section.");

// يمكننا استخدام خاصية "الموضع" لتحديد المكان الذي ستضع فيه الوثيقة جميع التعليقات الختامية.
// إذا قمنا بتعيين قيمة خاصية "الموضع" على "EndnotePosition.EndOfDocument" ،
// ستظهر كل حاشية سفلية في مجموعة في نهاية المستند. هذه هي القيمة الافتراضية.
// إذا قمنا بتعيين قيمة خاصية "الموضع" على "EndnotePosition.EndOfSection" ،
// ستظهر كل حاشية سفلية في مجموعة في نهاية القسم الذي يحتوي نصه على العلامة المرجعية للتعليق الختامي.
doc.EndnoteOptions.Position = endnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionEndnote.docx");
```

### أنظر أيضا

* enum [EndnotePosition](../../endnoteposition/)
* class [EndnoteOptions](../)
* مساحة الاسم [Aspose.Words.Notes](../../endnoteoptions/)
* المجسم [Aspose.Words](../../../)


