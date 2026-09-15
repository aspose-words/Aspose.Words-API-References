---
title: "طريقة Aspose::Words::Range::Replace"
linktitle: "Replace"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Range::Replace. تستبدل جميع حدوث نمط حرف محدد بتعبير عادي بسلسلة أخرى في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words/range/replace/
---
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


يستبدل جميع تكرارات نمط الحرف المحدد بتعبير عادي بسلسلة أخرى.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| نمط | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


يستبدل التطابق الكامل الذي تم التقاطه بواسطة التعبير العادي.

الطريقة قادرة على معالجة الفواصل في كل من سلاسل النمط والاستبدال.

يجب عليك استخدام أحرف ميتا خاصة إذا كنت بحاجة إلى العمل مع الفواصل:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## أمثلة



يعرض كيفية استبدال جميع تكرارات نمط تعبير عادي بنص آخر.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"I decided to get the curtains in gray, ideal for the grey-accented room.");

doc->get_Range()->Replace(System::MakeObject<System::Text::RegularExpressions::Regex>(u"gr(a|e)y"), u"lavender");

ASSERT_EQ(u"I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc->GetText().Trim());
```

## انظر أيضًا

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


يستبدل جميع تكرارات نمط الحرف المحدد بتعبير عادي بسلسلة أخرى.

```cpp
int32_t Aspose::Words::Range::Replace(const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| نمط | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | نمط تعبير عادي يُستخدم للعثور على التطابقات. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | كائن [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) لتحديد خيارات إضافية. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


يستبدل التطابق الكامل الذي تم التقاطه بواسطة التعبير العادي.

الطريقة قادرة على معالجة الفواصل في كل من سلاسل النمط والاستبدال.

يجب عليك استخدام أحرف ميتا خاصة إذا كنت بحاجة إلى العمل مع الفواصل:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## انظر أيضًا

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&) method


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| نمط | const System::String\& | سلسلة لاستبدالها. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


لن يُستخدم النمط كتعابير عادية. يرجى استخدام [Replace()](../) إذا كنت بحاجة إلى تعابير عادية.

تم استخدام مقارنة غير حساسة لحالة الأحرف.

الطريقة قادرة على معالجة الفواصل في كل من سلاسل النمط والاستبدال.

يجب عليك استخدام أحرف ميتا خاصة إذا كنت بحاجة إلى العمل مع الفواصل:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break



## أمثلة



يعرض كيفية إجراء عملية بحث واستبدال نص على محتويات المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Greetings, _FullName_!");

// قم بإجراء عملية بحث واستبدال على محتويات مستندنا وتحقق من عدد الاستبدالات التي حدثت.
int32_t replacementCount = doc->get_Range()->Replace(u"_FullName_", u"John Doe");

ASSERT_EQ(1, replacementCount);
ASSERT_EQ(u"Greetings, John Doe!", doc->GetText().Trim());
```


يوضح كيفية إضافة تنسيق إلى الفقرات التي وجدت فيها عملية البحث والاستبدال تطابقات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Every paragraph that ends with a full stop like this one will be right aligned.");
builder->Writeln(u"This one will not!");
builder->Write(u"This one also will.");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// عيّن الخاصية "Alignment" إلى "ParagraphAlignment.Right" لمحاذاة كل فقرة إلى اليمين.
// التي تحتوي على تطابق تجده عملية البحث والاستبدال.
options->get_ApplyParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// استبدل كل نقطة (.) التي تسبق مباشرة فاصل الفقرة بعلامة تعجب (!).
int32_t count = doc->get_Range()->Replace(u".&p", u"!&p", options);

ASSERT_EQ(2, count);
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(System::String(u"Every paragraph that ends with a full stop like this one will be right aligned!\r") + u"This one will not!\r" + u"This one also will!", doc->GetText().Trim());
```

## انظر أيضًا

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Range::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


يستبدل جميع تكرارات نمط سلسلة الأحرف المحدد بسلسلة استبدال.

```cpp
int32_t Aspose::Words::Range::Replace(const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| نمط | const System::String\& | سلسلة لاستبدالها. |
| استبدال | const System::String\& | سلسلة لاستبدال جميع حدوث النمط. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | كائن [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) لتحديد خيارات إضافية. |

### ReturnValue

عدد عمليات الاستبدال التي تم إجراؤها.
## ملاحظات


لن يُستخدم النمط كتعابير عادية. يرجى استخدام [Replace()](../) إذا كنت بحاجة إلى تعابير عادية.

الطريقة قادرة على معالجة الفواصل في كل من سلاسل النمط والاستبدال.

يجب عليك استخدام أحرف ميتا خاصة إذا كنت بحاجة إلى العمل مع الفواصل:

* **%&p** - paragraph break
* **%&b** - section break
* **%&m** - page break
* **%&l** - manual line break
* **%&&** - & character



## أمثلة



يوضح كيفية استبدال النص في تذييل المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```


يوضح كيفية تبديل حساسية حالة الأحرف عند تنفيذ عملية البحث والاستبدال.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// عيّن علم "MatchCase" إلى "true" لتطبيق حساسية حالة الأحرف أثناء البحث عن السلاسل لاستبدالها.
// عيّن علم "MatchCase" إلى "false" لتجاهل حالة الأحرف أثناء البحث عن النص لاستبداله.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


يوضح كيفية تبديل عمليات البحث والاستبدال التي تقتصر على الكلمات المستقلة فقط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// عيّن علم "FindWholeWordsOnly" إلى "true" لاستبدال النص الموجود إذا لم يكن جزءًا من كلمة أخرى.
// عيّن علم "FindWholeWordsOnly" إلى "false" لاستبدال كل النص بغض النظر عن محيطه.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```


يعرض كيفية استبدال جميع حالات سلسلة النص في جدول وخلية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Carrots");
builder->InsertCell();
builder->Write(u"50");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Potatoes");
builder->InsertCell();
builder->Write(u"50");
builder->EndTable();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(true);
options->set_FindWholeWordsOnly(true);

// قم بإجراء عملية بحث واستبدال على جدول كامل.
table->get_Range()->Replace(u"Carrots", u"Eggs", options);

// قم بإجراء عملية بحث واستبدال على الخلية الأخيرة من الصف الأخير في الجدول.
table->get_LastRow()->get_LastCell()->get_Range()->Replace(u"50", u"20", options);

ASSERT_EQ(System::String(u"Eggs\a50\a\a") + u"Potatoes\a20\a\a", table->GetText().Trim());
```

## انظر أيضًا

* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
