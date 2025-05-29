---
title: EndnotePosition Enum
linktitle: EndnotePosition
articleTitle: EndnotePosition
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words EndnotePosition للتحكم الدقيق في وضع الملاحظات الختامية في المستندات، مما يعزز قدرات تنسيق النص لديك.
type: docs
weight: 4940
url: /ar/net/aspose.words.notes/endnoteposition/
---
## EndnotePosition enumeration

يحدد موضع الحاشية الختامية.

```csharp
public enum EndnotePosition
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| EndOfSection | `0` | يتم إخراج الحواشي في نهاية القسم. |
| EndOfDocument | `3` | يتم إخراج الحواشي في نهاية المستند. |

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

* class [EndnoteOptions](../endnoteoptions/)
* مساحة الاسم [Aspose.Words.Notes](../../aspose.words.notes/)
* المجسم [Aspose.Words](../../)
