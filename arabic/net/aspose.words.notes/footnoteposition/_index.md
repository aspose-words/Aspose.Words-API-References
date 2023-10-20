---
title: FootnotePosition Enum
linktitle: FootnotePosition
articleTitle: FootnotePosition
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Notes.FootnotePosition تعداد. يحدد موضع الحاشية السفلية في C#.
type: docs
weight: 4290
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
| BottomOfPage | `1` | يتم إخراج الحواشي أسفل كل صفحة. |
| BeneathText | `2` | يتم إخراج الحواشي أسفل النص في كل صفحة. |

## أمثلة

يوضح كيفية تحديد مكان مختلف حيث يتم تجميع المستند وعرض حواشيه السفلية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// الحاشية السفلية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
 // لا يتعارض مع تدفق النص الأساسي.
// يؤدي إدراج حاشية سفلية إلى إضافة رمز مرجعي مرتفع صغير
// في النص الرئيسي حيث نقوم بإدراج الحاشية السفلية.
// تنشئ كل حاشية سفلية أيضًا إدخالاً في أسفل الصفحة يتكون من رمز
// الذي يطابق الرمز المرجعي في النص الأساسي.
// النص المرجعي الذي نمرره إلى طريقة "InsertFootnote" الخاصة بمنشئ المستندات.
builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote contents.");

// يمكننا استخدام خاصية "الموضع" لتحديد المكان الذي ستضع فيه الوثيقة جميع الحواشي السفلية.
// إذا قمنا بتعيين قيمة خاصية "الموضع" على "FootnotePosition.BottomOfPage"،
// ستظهر كل حاشية سفلية في أسفل الصفحة التي تحتوي على العلامة المرجعية الخاصة بها. هذه هي القيمة الافتراضية.
// إذا قمنا بتعيين قيمة خاصية "الموضع" على "FootnotePosition.BeneathText"،
// ستظهر كل حاشية سفلية في نهاية نص الصفحة الذي يحتوي على العلامة المرجعية الخاصة بها.
doc.FootnoteOptions.Position = footnotePosition;

doc.Save(ArtifactsDir + "InlineStory.PositionFootnote.docx");
```

### أنظر أيضا

* class [FootnoteOptions](../footnoteoptions/)
* مساحة الاسم [Aspose.Words.Notes](../../aspose.words.notes/)
* المجسم [Aspose.Words](../../)
