---
title: "طريقة Aspose::Words::DocumentBuilder::InsertHtml"
linktitle: "InsertHtml"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::InsertHtml. تُدرج سلسلة HTML في المستند بلغة C++."
type: docs
weight: 37000
url: /ar/cpp/aspose.words/documentbuilder/inserthtml/
---
## DocumentBuilder::InsertHtml(const System::String\&) method


يدرج سلسلة HTML في المستند.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| html | const System::String\& | سلسلة HTML لإدراجها في المستند. |

## أمثلة



يوضح كيفية استخدام مُنشئ المستند لإدراج محتوى HTML في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const System::String html = System::String(u"<p align='right'>Paragraph right</p>") + u"<b>Implicit paragraph left</b>" + u"<div align='center'>Div center</div>" + u"<h1 align='left'>Heading 1 left.</h1>";

builder->InsertHtml(html);

// يقوم إدراج شفرة HTML بتحليل تنسيق كل عنصر وتحويله إلى تنسيق نصي مكافئ في المستند.
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(u"Paragraph right", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Implicit paragraph left", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_TRUE(paragraphs->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_Bold());

ASSERT_EQ(u"Div center", paragraphs->idx_get(2)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Heading 1 left.", paragraphs->idx_get(3)->GetText().Trim());
ASSERT_EQ(u"Heading 1", paragraphs->idx_get(3)->get_ParagraphFormat()->get_Style()->get_Name());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtml.docx");
```

## انظر أيضًا

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, Aspose::Words::HtmlInsertOptions) method


يقوم بإدراج سلسلة HTML في المستند. يسمح بتحديد خيارات إضافية.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, Aspose::Words::HtmlInsertOptions options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| html | const System::String\& | سلسلة HTML لإدراجها في المستند. |
| خيارات | Aspose::Words::HtmlInsertOptions | الخيارات المستخدمة عند إدراج سلسلة HTML. |

## انظر أيضًا

* Enum [HtmlInsertOptions](../../htmlinsertoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, bool) method


يدرج سلسلة HTML في المستند.

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, bool useBuilderFormatting)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| html | const System::String\& | سلسلة HTML لإدراجها في المستند. |
| useBuilderFormatting | bool | قيمة تشير إلى ما إذا كان التنسيق المحدد في [DocumentBuilder](../) يُستخدم كتنسيق أساسي للنص المستورد من HTML. |
## ملاحظات


يمكنك استخدام هذه الطريقة لإدراج جزء HTML أو مستند HTML كامل.

عندما يكون *useBuilderFormatting* **false**, يتم تجاهل تنسيق [DocumentBuilder](../) ويستند تنسيق النص المُدرج إلى تنسيق HTML الافتراضي. نتيجة لذلك، يظهر النص كما يُعرض في المتصفحات.

عندما يكون *useBuilderFormatting* **true**, يستند تنسيق النص المُدرج إلى تنسيق [DocumentBuilder](../)، ويظهر النص كما لو أنه تم إدراجه باستخدام [Write()](../).

## أمثلة



يوضح كيفية تطبيق تنسيق مُنشئ المستند أثناء إدراج محتوى HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// حدد محاذاة النص للمُنشئ، وأدرج فقرة HTML بمحاذاة محددة، وواحدة بدون محاذاة.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Distributed);
builder->InsertHtml(System::String(u"<p align='right'>Paragraph 1.</p>") + u"<p>Paragraph 2.</p>", useBuilderFormatting);

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// الفقرة الأولى لها محاذاة محددة. عندما يقوم InsertHtml بتحليل شفرة HTML،
// دائمًا ما تتجاوز قيمة محاذاة الفقرة الموجودة في شفرة HTML قيمة محاذاة مُنشئ المستند.
ASSERT_EQ(u"Paragraph 1.", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

// الفقرة الثانية لا تحتوي على محاذاة محددة. يمكن ملء قيمة محاذتها
// بقيمة المُنشئ اعتمادًا على العلامة التي مررناها إلى طريقة InsertHtml.
ASSERT_EQ(u"Paragraph 2.", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(useBuilderFormatting ? Aspose::Words::ParagraphAlignment::Distributed : Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtmlWithFormatting.docx");
```

## انظر أيضًا

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
