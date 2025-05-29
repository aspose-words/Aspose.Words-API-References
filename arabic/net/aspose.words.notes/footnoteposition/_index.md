---
title: FootnotePosition Enum
linktitle: FootnotePosition
articleTitle: FootnotePosition
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Notes.FootnotePosition لوضع الحواشي السفلية بشكل قابل للتخصيص، مما يعزز تنسيق المستندات وقابليتها للقراءة.
type: docs
weight: 4980
url: /ar/net/aspose.words.notes/footnoteposition/
---
## FootnotePosition enumeration

يحدد موضع الحاشية السفلية.

```csharp
public enum FootnotePosition
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| BottomOfPage | `1` | يتم إخراج الحواشي في أسفل كل صفحة. |
| BeneathText | `2` | يتم إخراج الحواشي أسفل النص في كل صفحة. |

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

* class [FootnoteOptions](../footnoteoptions/)
* مساحة الاسم [Aspose.Words.Notes](../../aspose.words.notes/)
* المجسم [Aspose.Words](../../)
