---
title: ControlChar Class
linktitle: ControlChar
articleTitle: ControlChar
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.ControlChar لإدارة أحرف التحكم في مستنداتك بفعالية لتحسين التنسيق وسهولة القراءة.
type: docs
weight: 550
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
| static readonly [Cell](../../aspose.words/controlchar/cell/) | نهاية خلية الجدول أو نهاية صف الجدول: "\x0007" أو "\a". |
| const [CellChar](../../aspose.words/controlchar/cellchar/) | نهاية خلية الجدول أو نهاية صف الجدول: (char)7 أو "\a". |
| static readonly [ColumnBreak](../../aspose.words/controlchar/columnbreak/) | حرف نهاية العمود: "\x000e". |
| const [ColumnBreakChar](../../aspose.words/controlchar/columnbreakchar/) | نهاية حرف العمود: (char)14. |
| static readonly [Cr](../../aspose.words/controlchar/cr/) | حرف إرجاع العربة: "\x000d" أو "\r". نفس[`ParagraphBreak`](./paragraphbreak/) . |
| static readonly [CrLf](../../aspose.words/controlchar/crlf/) | إرجاع العربة متبوعًا بحرف تغذية السطر: "\x000d\x000a" أو "\r\n". لا يتم استخدامه على هذا النحو في مستندات Microsoft Word، ولكن يتم استخدامه عادةً في ملفات النصوص لفواصل الفقرات. |
| const [DefaultTextInputChar](../../aspose.words/controlchar/defaulttextinputchar/) | هذا هو الحرف "o" المستخدم كقيمة افتراضية في حقول نموذج إدخال النص. |
| const [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) | نهاية حرف حقل MS Word: (char)21. |
| const [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) | يفصل حرف فاصل الحقل رمز الحقل عن قيمته. اختياري في بعض الحقول. القيمة: (char)20. |
| const [FieldStartChar](../../aspose.words/controlchar/fieldstartchar/) | بداية حرف حقل MS Word: (char)19. |
| static readonly [Lf](../../aspose.words/controlchar/lf/) | حرف تغذية السطر: "\x000a" أو "\n". نفس[`LineFeed`](./linefeed/) . |
| static readonly [LineBreak](../../aspose.words/controlchar/linebreak/) | حرف كسر السطر: "\x000b" أو "\v". |
| const [LineBreakChar](../../aspose.words/controlchar/linebreakchar/) | حرف كسر السطر: (char)11 أو "\v". |
| static readonly [LineFeed](../../aspose.words/controlchar/linefeed/) | حرف تغذية السطر: "\x000a" أو "\n". نفس[`Lf`](./lf/) . |
| const [LineFeedChar](../../aspose.words/controlchar/linefeedchar/) | حرف تغذية السطر: (char)10 أو "\n". |
| const [NonBreakingHyphenChar](../../aspose.words/controlchar/nonbreakinghyphenchar/) | الشرطة غير القابلة للكسر في Microsoft Word هي (char)30. |
| static readonly [NonBreakingSpace](../../aspose.words/controlchar/nonbreakingspace/) | حرف مسافة غير قابلة للكسر: "\x00a0". |
| const [NonBreakingSpaceChar](../../aspose.words/controlchar/nonbreakingspacechar/) | حرف مسافة غير قابلة للكسر: (char)160. |
| const [OptionalHyphenChar](../../aspose.words/controlchar/optionalhyphenchar/) | الشرطة الاختيارية في Microsoft Word هي (char)31. |
| static readonly [PageBreak](../../aspose.words/controlchar/pagebreak/) | حرف فاصل الصفحة : "\x000c" أو "\f". لاحظ أن قيمته هي نفسها[`SectionBreak`](./sectionbreak/) . |
| const [PageBreakChar](../../aspose.words/controlchar/pagebreakchar/) | حرف فاصل الصفحة: (char)12 أو "\f". |
| static readonly [ParagraphBreak](../../aspose.words/controlchar/paragraphbreak/) | حرف نهاية الفقرة: "\x000d" أو "\r". نفس[`Cr`](./cr/) |
| const [ParagraphBreakChar](../../aspose.words/controlchar/paragraphbreakchar/) | حرف نهاية الفقرة: (char)13 أو "\r". |
| static readonly [SectionBreak](../../aspose.words/controlchar/sectionbreak/) | حرف نهاية المقطع: "\x000c" أو "\f". لاحظ أن قيمته هي نفسها[`PageBreak`](./pagebreak/) . |
| const [SectionBreakChar](../../aspose.words/controlchar/sectionbreakchar/) | حرف نهاية القسم: (char)12 أو "\f". |
| const [SpaceChar](../../aspose.words/controlchar/spacechar/) | حرف المسافة: (char)32. |
| static readonly [Tab](../../aspose.words/controlchar/tab/) | حرف علامة التبويب: "\x0009" أو "\t". |
| const [TabChar](../../aspose.words/controlchar/tabchar/) | حرف علامة التبويب: (char)9 أو "\t". |

## ملاحظات

يوفر نسختين من نفس الثوابت: char وstring. على سبيل المثال: string[`LineBreak`](./linebreak/) و حرف[`LineBreakChar`](./linebreakchar/) لها نفس القيمة.

## أمثلة

يوضح كيفية استخدام أحرف التحكم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج فقرات تحتوي على نص باستخدام DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// يؤدي تحويل المستند إلى نموذج نصي إلى إظهار أن أحرف التحكم
// تمثل بعض العناصر الهيكلية للمستند، مثل فواصل الصفحات.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// عند تحويل مستند إلى شكل سلسلة،
// يمكننا حذف بعض أحرف التحكم باستخدام طريقة Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
