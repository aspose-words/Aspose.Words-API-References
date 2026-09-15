---
title: "طريقة Aspose::Words::Paragraph::JoinRunsWithSameFormatting"
linktitle: "JoinRunsWithSameFormatting"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Paragraph::JoinRunsWithSameFormatting. يجمع المقاطع ذات التنسيق نفسه في الفقرة في C++."
type: docs
weight: 31000
url: /ar/cpp/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph::JoinRunsWithSameFormatting() method


يجمع المقاطع ذات التنسيق نفسه في الفقرة.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting()
```


### ReturnValue

عدد عمليات الجمع التي تم تنفيذها. عندما يتم جمع **N** مقاطع متجاورة تُحسب كـ **N - 1** عمليات جمع.

## أمثلة



يعرض كيفية تبسيط الفقرات عن طريق دمج المقاطع الزائدة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدخل أربع مقاطع نصية في الفقرة.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");
builder->Write(u"Run 3. ");
builder->Write(u"Run 4. ");

// إذا فتحنا هذا المستند في Microsoft Word، ستظهر الفقرة كجسم نصي سلس واحد.
// ومع ذلك، سيتكون من أربع مقاطع منفصلة ذات نفس التنسيق. الفقرات المجزأة مثل هذه
// قد تحدث عندما نقوم بتحرير أجزاء من فقرة واحدة يدوياً عدة مرات في Microsoft Word.
System::SharedPtr<Aspose::Words::Paragraph> para = builder->get_CurrentParagraph();

ASSERT_EQ(4, para->get_Runs()->get_Count());

// غيّر نمط المقاطع الأخيرة لتفصلها عن الثلاثة الأولى.
para->get_Runs()->idx_get(3)->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Emphasis);

// يمكننا تشغيل طريقة "JoinRunsWithSameFormatting" لتحسين محتويات المستند
// عن طريق دمج المقاطع المتشابهة في واحدة، مما يقلل عددها الإجمالي.
// تعيد هذه الطريقة أيضاً عدد المقاطع التي دمجتها هذه الطريقة.
// حدثت هاتان العمليتان لدمج المقاطع #1، #2، و #3،
// مع استبعاد Run #4 لأنه يحتوي على نمط غير متوافق.
ASSERT_EQ(2, para->JoinRunsWithSameFormatting());

// عدد الـ runs المتبقية سيساوي العدد الأصلي
// ناقص عدد دمج الـ runs التي نفذتها طريقة "JoinRunsWithSameFormatting".
ASSERT_EQ(2, para->get_Runs()->get_Count());
ASSERT_EQ(u"Run 1. Run 2. Run 3. ", para->get_Runs()->idx_get(0)->get_Text());
ASSERT_EQ(u"Run 4. ", para->get_Runs()->idx_get(1)->get_Text());
```

## انظر أيضًا

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) method


يجمع المقاطع ذات التنسيق نفسه في الفقرة.

```cpp
int32_t Aspose::Words::Paragraph::JoinRunsWithSameFormatting(const System::SharedPtr<Aspose::Words::JoinRunsOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| خيارات | const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\& | خيارات إضافية |

### ReturnValue

عدد عمليات الجمع التي تم تنفيذها. عندما يتم جمع **N** مقاطع متجاورة تُحسب كـ **N - 1** عمليات جمع.

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

* Class [JoinRunsOptions](../../joinrunsoptions/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
