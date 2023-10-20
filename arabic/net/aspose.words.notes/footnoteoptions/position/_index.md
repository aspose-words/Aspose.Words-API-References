---
title: FootnoteOptions.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words لـ .NET
description: FootnoteOptions Position ملكية. يحدد موضع الحواشي السفلية في C#.
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

* enum [FootnotePosition](../../footnoteposition/)
* class [FootnoteOptions](../)
* مساحة الاسم [Aspose.Words.Notes](../../../aspose.words.notes/)
* المجسم [Aspose.Words](../../../)
