---
title: ControlChar Class
linktitle: ControlChar
articleTitle: ControlChar
second_title: Aspose.Words لـ .NET
description: Aspose.Words.ControlChar فصل. أحرف التحكم التي يتم مواجهتها غالبًا في المستندات في C#.
type: docs
weight: 350
url: /ar/net/aspose.words/controlchar/
---
## ControlChar class

أحرف التحكم التي يتم مواجهتها غالبًا في المستندات.

لمعرفة المزيد، قم بزيارة[العمل مع أحرف التحكم](https://docs.aspose.com/words/net/working-with-control-characters/) مقالة توثيقية.

```csharp
public static class ControlChar
```

## مجالات

| اسم | وصف |
| --- | --- |
| static readonly [Cell](../../aspose.words/controlchar/cell/) | حرف نهاية خلية الجدول أو نهاية صف الجدول: "\x0007" أو "\a". |
| const [CellChar](../../aspose.words/controlchar/cellchar/) | نهاية خلية الجدول أو نهاية حرف صف الجدول: (char)7 أو "\a". |
| static readonly [ColumnBreak](../../aspose.words/controlchar/columnbreak/) | حرف نهاية العمود: "\x000e". |
| const [ColumnBreakChar](../../aspose.words/controlchar/columnbreakchar/) | حرف نهاية العمود: (char)14. |
| static readonly [Cr](../../aspose.words/controlchar/cr/) | حرف الإرجاع: "\x000d" أو "\r". مثل[`ParagraphBreak`](./paragraphbreak/) . |
| static readonly [CrLf](../../aspose.words/controlchar/crlf/) | حرف إرجاع متبوعًا بحرف تغذية الأسطر: "\x000d\x000a" أو "\r\n". لا يستخدم على هذا النحو في مستندات Microsoft Word، ولكنه شائع الاستخدام في الملفات النصية لفواصل الفقرات. |
| const [DefaultTextInputChar](../../aspose.words/controlchar/defaulttextinputchar/) | هذا هو الحرف "o" المستخدم كقيمة افتراضية في حقول نموذج إدخال النص. |
| const [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) | نهاية حرف حقل MS Word: (char)21. |
| const [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) | حرف فاصل الحقل يفصل رمز الحقل عن قيمة الحقل. اختيارية في بعض المجالات. القيمة: (شار)20. |
| const [FieldStartChar](../../aspose.words/controlchar/fieldstartchar/) | بداية حرف حقل MS Word: (char)19. |
| static readonly [Lf](../../aspose.words/controlchar/lf/) | حرف تغذية السطر: "\x000a" أو "\n". مثل[`LineFeed`](./linefeed/) . |
| static readonly [LineBreak](../../aspose.words/controlchar/linebreak/) | حرف فاصل الأسطر: "\x000b" أو "\v". |
| const [LineBreakChar](../../aspose.words/controlchar/linebreakchar/) | حرف فاصل الأسطر: (char)11 أو "\v". |
| static readonly [LineFeed](../../aspose.words/controlchar/linefeed/) | حرف تغذية السطر: "\x000a" أو "\n". مثل[`Lf`](./lf/) . |
| const [LineFeedChar](../../aspose.words/controlchar/linefeedchar/) | حرف تغذية السطر: (char)10 أو "\n". |
| const [NonBreakingHyphenChar](../../aspose.words/controlchar/nonbreakinghyphenchar/) | الواصلة غير منقسمة في Microsoft Word هي (char)30. |
| static readonly [NonBreakingSpace](../../aspose.words/controlchar/nonbreakingspace/) | حرف مسافة غير منقسمة: "\x00a0". |
| const [NonBreakingSpaceChar](../../aspose.words/controlchar/nonbreakingspacechar/) | حرف مسافة غير منقسمة: (char)160. |
| const [OptionalHyphenChar](../../aspose.words/controlchar/optionalhyphenchar/) | الواصلة الاختيارية في Microsoft Word هي (char)31. |
| static readonly [PageBreak](../../aspose.words/controlchar/pagebreak/) | حرف فاصل الصفحات: "\x000c" أو "\f". لاحظ أن لها نفس القيمة[`SectionBreak`](./sectionbreak/) . |
| const [PageBreakChar](../../aspose.words/controlchar/pagebreakchar/) | حرف فاصل الصفحات: (char)12 أو "\f". |
| static readonly [ParagraphBreak](../../aspose.words/controlchar/paragraphbreak/) | حرف نهاية الفقرة: "\x000d" أو "\r". مثل[`Cr`](./cr/) |
| const [ParagraphBreakChar](../../aspose.words/controlchar/paragraphbreakchar/) | حرف نهاية الفقرة: (char)13 أو "\r". |
| static readonly [SectionBreak](../../aspose.words/controlchar/sectionbreak/) | حرف نهاية القسم: "\x000c" أو "\f". لاحظ أن لها نفس القيمة[`PageBreak`](./pagebreak/) . |
| const [SectionBreakChar](../../aspose.words/controlchar/sectionbreakchar/) | حرف نهاية القسم: (char)12 أو "\f". |
| const [SpaceChar](../../aspose.words/controlchar/spacechar/) | حرف المسافة: (char)32. |
| static readonly [Tab](../../aspose.words/controlchar/tab/) | حرف علامة التبويب: "\x0009" أو "\t". |
| const [TabChar](../../aspose.words/controlchar/tabchar/) | حرف علامة التبويب: (char)9 أو "\t". |

## ملاحظات

يوفر إصداري char وstring لنفس الثوابت. على سبيل المثال: سلسلة[`LineBreak`](./linebreak/) وشار[`LineBreakChar`](./linebreakchar/) لها نفس القيمة.

## أمثلة

يوضح كيفية استخدام أحرف التحكم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج فقرات تحتوي على نص باستخدام DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// يكشف تحويل المستند إلى نموذج نصي عن أحرف التحكم تلك
// تمثل بعض العناصر الهيكلية للمستند، مثل فواصل الصفحات.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// عند تحويل مستند إلى نموذج سلسلة،
// يمكننا حذف بعض أحرف التحكم باستخدام طريقة القطع.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
