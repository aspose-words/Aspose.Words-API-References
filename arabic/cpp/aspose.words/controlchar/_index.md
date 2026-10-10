---
title: "Aspose::Words::ControlChar فئة"
linktitle: "ControlChar"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ControlChar فئة. الأحرف التحكمية غالبًا ما تُواجه في المستندات. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words/controlchar/
---
## ControlChar class


أحرف التحكم التي تُواجه كثيرًا في المستندات. لمعرفة المزيد، قم بزيارة مقالة الوثائق [Working With Control Characters](https://docs.aspose.com/words/cpp/working-with-control-characters/).

```cpp
class ControlChar
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| static [Cell](./cell/)() | حرف نهاية خلية جدول أو نهاية صف جدول: "\x0007" أو "\a". |
| static [ColumnBreak](./columnbreak/)() | حرف نهاية العمود: "\x000e". |
| [ControlChar](./controlchar/)() |  |
| static [Cr](./cr/)() | حرف عودة السطر: "\x000d" أو "\r". نفس [ParagraphBreak](./paragraphbreak/). |
| static [CrLf](./crlf/)() | عودة السطر متبوعة بحرف تغذية السطر: "\x000d\x000a" أو "\r\n". لا يُستخدم بهذه الطريقة في مستندات Microsoft Word، لكنه يُستعمل عادةً في ملفات النص للفواصل الفقرية. |
| static [Lf](./lf/)() | حرف تغذية السطر: "\x000a" أو "\n". نفس [LineFeed](./linefeed/). |
| static [LineBreak](./linebreak/)() | حرف فاصل السطر: "\x000b" أو "\v". |
| static [LineFeed](./linefeed/)() | حرف تغذية السطر: "\x000a" أو "\n". نفس [Lf](./lf/). |
| static [NonBreakingSpace](./nonbreakingspace/)() | حرف مساحة غير قابلة للكسر: "\x00a0". |
| static [PageBreak](./pagebreak/)() | حرف فاصل الصفحة: "\x000c" أو "\f". لاحظ أن له نفس القيمة مثل [SectionBreak](./sectionbreak/). |
| static [ParagraphBreak](./paragraphbreak/)() | حرف نهاية الفقرة: "\x000d" أو "\r". نفس [Cr](./cr/) |
| static [SectionBreak](./sectionbreak/)() | حرف نهاية القسم: "\x000c" أو "\f". لاحظ أن له نفس القيمة مثل [PageBreak](./pagebreak/). |
| static [Tab](./tab/)() | حرف الجدولة: "\x0009" أو "\t". |
## الحقول

| حقل | الوصف |
| --- | --- |
| static constexpr [CellChar](./cellchar/) | حرف نهاية خلية جدول أو نهاية صف جدول: (char)7 أو "\a". |
| static constexpr [ColumnBreakChar](./columnbreakchar/) | حرف نهاية العمود: (char)14. |
| static constexpr [DefaultTextInputChar](./defaulttextinputchar/) | هذا هو الحرف "o" المستخدم كقيمة افتراضية في حقول نماذج إدخال النص. |
| static constexpr [FieldEndChar](./fieldendchar/) | حرف نهاية حقل MS Word: (char)21. |
| static constexpr [FieldSeparatorChar](./fieldseparatorchar/) | حرف فاصل الحقل يفصل رمز الحقل عن قيمته. اختياري في بعض الحقول. القيمة: (char)20. |
| static constexpr [FieldStartChar](./fieldstartchar/) | حرف بداية حقل MS Word: (char)19. |
| static constexpr [LineBreakChar](./linebreakchar/) | حرف فاصل السطر: (char)11 أو "\v". |
| static constexpr [LineFeedChar](./linefeedchar/) | حرف سطر جديد: (char)10 أو "\n". |
| static constexpr [NonBreakingHyphenChar](./nonbreakinghyphenchar/) | الواصلة غير القابلة للكسر في Microsoft Word هي (char)30. |
| static constexpr [NonBreakingSpaceChar](./nonbreakingspacechar/) | حرف المسافة غير القابلة للكسر: (char)160. |
| static constexpr [OptionalHyphenChar](./optionalhyphenchar/) | الواصلة الاختيارية في Microsoft Word هي (char)31. |
| static constexpr [PageBreakChar](./pagebreakchar/) | حرف فاصل الصفحة: (char)12 أو "\f". |
| static constexpr [ParagraphBreakChar](./paragraphbreakchar/) | حرف نهاية الفقرة: (char)13 أو "\r". |
| static constexpr [SectionBreakChar](./sectionbreakchar/) | حرف نهاية القسم: (char)12 أو "\f". |
| static constexpr [SpaceChar](./spacechar/) | حرف المسافة: (char)32. |
| static constexpr [TabChar](./tabchar/) | حرف الجدولة: (char)9 أو "\t". |

## أمثلة



يعرض كيفية استخدام الأحرف التحكمية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إدراج فقرات بنص باستخدام DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// تحويل المستند إلى صيغة نصية يكشف أن الأحرف التحكمية
// تمثل بعض العناصر الهيكلية للمستند، مثل فواصل الصفحات.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// عند تحويل مستند إلى صيغة سلسلة،
// يمكننا حذف بعض الأحرف التحكمية باستخدام طريقة Trim.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
