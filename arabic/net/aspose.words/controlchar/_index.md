---
title: Class ControlChar
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.ControlChar فصل. غالبًا ما يتم العثور على أحرف التحكم في المستندات.
type: docs
weight: 340
url: /ar/net/aspose.words/controlchar/
---
## ControlChar class

غالبًا ما يتم العثور على أحرف التحكم في المستندات.

```csharp
public static class ControlChar
```

## مجالات

| اسم | وصف |
| --- | --- |
| static readonly [Cell](../../aspose.words/controlchar/cell/) | نهاية خلية الجدول أو نهاية حرف صف الجدول: "\ x0007" أو "\ a" . |
| const [CellChar](../../aspose.words/controlchar/cellchar/) | نهاية خلية الجدول أو حرف نهاية صف الجدول: (char) 7 أو "\ a" . |
| static readonly [ColumnBreak](../../aspose.words/controlchar/columnbreak/) | نهاية حرف العمود: "\ x000e" . |
| const [ColumnBreakChar](../../aspose.words/controlchar/columnbreakchar/) | نهاية حرف العمود: (حرف) 14. |
| static readonly [Cr](../../aspose.words/controlchar/cr/) | حرف إرجاع السطر: "\ x000d" أو "\ r". مثل[`ParagraphBreak`](./paragraphbreak/) . |
| static readonly [CrLf](../../aspose.words/controlchar/crlf/) | إرجاع السطر متبوعًا بحرف تغذية الأسطر: "\ x000d \ x000a" أو "\ r \ n" . غير مستخدم على هذا النحو في مستندات Microsoft Word ، ولكنه شائع الاستخدام في الملفات النصية لفواصل الفقرات . |
| const [DefaultTextInputChar](../../aspose.words/controlchar/defaulttextinputchar/) | هذا هو الحرف "o" المستخدم كقيمة افتراضية في حقول نموذج إدخال النص. |
| const [FieldEndChar](../../aspose.words/controlchar/fieldendchar/) | نهاية حرف حقل MS Word: (char) 21. |
| const [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) | يفصل حرف فاصل الحقل رمز الحقل عن قيمة الحقل. اختياري في بعض المجالات. القيمة: (شار) 20. |
| const [FieldStartChar](../../aspose.words/controlchar/fieldstartchar/) | بداية حرف حقل MS Word: (char) 19. |
| static readonly [Lf](../../aspose.words/controlchar/lf/) | حرف تغذية السطر: "\ x000a" أو "\ n". مثل[`LineFeed`](./linefeed/) . |
| static readonly [LineBreak](../../aspose.words/controlchar/linebreak/) | حرف فاصل الأسطر: "\ x000b" أو "\ v" . |
| const [LineBreakChar](../../aspose.words/controlchar/linebreakchar/) | حرف فاصل الأسطر: (حرف) 11 أو "\ v" . |
| static readonly [LineFeed](../../aspose.words/controlchar/linefeed/) | حرف تغذية السطر: "\ x000a" أو "\ n". مثل[`Lf`](./lf/) . |
| const [LineFeedChar](../../aspose.words/controlchar/linefeedchar/) | حرف موجز السطر: (char) 10 أو "\ n" . |
| const [NonBreakingHyphenChar](../../aspose.words/controlchar/nonbreakinghyphenchar/) | واصلة غير منقسمة في Microsoft Word هي (حرف) 30. |
| static readonly [NonBreakingSpace](../../aspose.words/controlchar/nonbreakingspace/) | حرف مسافة غير منقسمة: "\ x00a0" . |
| const [NonBreakingSpaceChar](../../aspose.words/controlchar/nonbreakingspacechar/) | حرف مسافة غير منقسمة: (char) 160. |
| const [OptionalHyphenChar](../../aspose.words/controlchar/optionalhyphenchar/) | واصلة اختيارية في Microsoft Word هي (حرف) 31. |
| static readonly [PageBreak](../../aspose.words/controlchar/pagebreak/) | حرف فاصل الصفحة: "\ x000c" أو "\ f". لاحظ أن لها نفس القيمة مثل[`SectionBreak`](./sectionbreak/) . |
| const [PageBreakChar](../../aspose.words/controlchar/pagebreakchar/) | حرف فاصل الصفحة: (char) 12 أو "\ f" . |
| static readonly [ParagraphBreak](../../aspose.words/controlchar/paragraphbreak/) | نهاية حرف الفقرة: "\ x000d" أو "\ r". مثل[`Cr`](./cr/) |
| const [ParagraphBreakChar](../../aspose.words/controlchar/paragraphbreakchar/) | نهاية حرف الفقرة: (حرف) 13 أو "\ r" . |
| static readonly [SectionBreak](../../aspose.words/controlchar/sectionbreak/) | نهاية حرف القسم: "\ x000c" أو "\ f". لاحظ أن لها نفس القيمة مثل[`PageBreak`](./pagebreak/) . |
| const [SectionBreakChar](../../aspose.words/controlchar/sectionbreakchar/) | حرف نهاية المقطع: (char) 12 أو "\ f" . |
| const [SpaceChar](../../aspose.words/controlchar/spacechar/) | حرف مسافة: (حرف) 32. |
| static readonly [Tab](../../aspose.words/controlchar/tab/) | حرف الجدولة: "\ x0009" أو "\ t" . |
| const [TabChar](../../aspose.words/controlchar/tabchar/) | حرف الجدولة: (char) 9 أو "\ t" . |

### ملاحظات

يوفر كلاً من إصدارات الأحرف والسلسلة لنفس الثوابت. على سبيل المثال: string ControlChar.LineBreak و char ControlChar.LineBreakChar لهما نفس القيمة.

### أمثلة

يوضح كيفية استخدام أحرف التحكم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل فقرات مع نص باستخدام DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// تحويل المستند إلى نموذج نصي يكشف عن التحكم في الأحرف
// تمثل بعض العناصر الهيكلية للمستند ، مثل فواصل الصفحات.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// عند تحويل مستند إلى شكل سلسلة ،
// يمكننا حذف بعض أحرف التحكم باستخدام طريقة Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


