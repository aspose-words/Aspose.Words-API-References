---
title: "فئة Aspose::Words::JoinRunsOptions"
linktitle: "JoinRunsOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::JoinRunsOptions. توفر أعلام تكوين لعملية دمج المقاطع في C++."
type: docs
weight: 38500
url: /ar/cpp/aspose.words/joinrunsoptions/
---
## JoinRunsOptions class


يوفر أعلام تكوين لعملية دمج المقاطع.

```cpp
class JoinRunsOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_IgnoreInsignificant](./get_ignoreinsignificant/)() const | صحيح يشير إلى أن السمات غير المهمة لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه. |
| [get_IgnoreRedundant](./get_ignoreredundant/)() const | صحيح يشير إلى أن السمات الزائدة لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه. |
| [get_IgnoreSpacing](./get_ignorespacing/)() const | صحيح يشير إلى أن سمات التباعد لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [JoinRunsOptions](./joinrunsoptions/)() |  |
| [set_IgnoreInsignificant](./set_ignoreinsignificant/)(bool) | صحيح يشير إلى أن السمات غير المهمة لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه. |
| [set_IgnoreRedundant](./set_ignoreredundant/)(bool) | صحيح يشير إلى أن السمات الزائدة لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه. |
| [set_IgnoreSpacing](./set_ignorespacing/)(bool) | صحيح يشير إلى أن سمات التباعد لجميع المقاطع سيتم تجاهلها عند دمج المقاطع ذات التنسيق نفسه. |
| static [Type](./type/)() |  |

## أمثلة



يعرض كيفية دمج المقاطع ذات التنسيق نفسه مع تجاهل السمات الزائدة وغير المهمة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء مقاطع بتنسيق مرئي متطابق لكن مع بعض الاختلافات الداخلية.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(12);
builder->Write(u"Hello ");
builder->Write(u"world");

// تحقق من المقاطع قبل الدمج.
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello ", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1)->get_Text());

// تكوين الخيارات لتجاهل السمات الزائدة وغير المهمة أثناء الدمج.
auto options = System::MakeObject<Aspose::Words::JoinRunsOptions>();
options->set_IgnoreRedundant(true);
// تجاهل خصائص المقاطع الزائدة التي لا تؤثر على المظهر.
options->set_IgnoreInsignificant(true);
// تجاهل الاختلافات غير المهمة مثل المقاطع التي تحتوي فقط على مسافات بيضاء.

// اجمع القطاعات التي لها نفس التنسيق المرئي باستخدام الخيارات الموسعة.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->JoinRunsWithSameFormatting(options);

// تحقق من أن القطاعات تم دمجها بنجاح.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->get_Count());
ASSERT_EQ(u"Hello world", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());

doc->Save(get_ArtifactsDir() + u"Paragraph.JoinRunsWithSameFormattingWithOptions.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
