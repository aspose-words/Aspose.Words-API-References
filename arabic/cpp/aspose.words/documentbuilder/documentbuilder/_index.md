---
title: "Aspose::Words::DocumentBuilder::DocumentBuilder constructor"
linktitle: "DocumentBuilder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::DocumentBuilder constructor. يهيئ نسخة جديدة من هذه الفئة في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder::DocumentBuilder() constructor


يُنشئ مثيلًا جديدًا لهذه الفئة.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder()
```


## أمثلة



يعرض كيفية إدراج نص منسق باستخدام [DocumentBuilder](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// حدد تنسيق الخط، ثم أضف النص.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```

## انظر أيضًا

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::Document\>\&) constructor


يُنشئ مثيلًا جديدًا لهذه الفئة.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::Document> &doc)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | كائن [Document](../../document/) المراد إرفاقه. |

## أمثلة



يوضح كيفية إدراج جدول محتويات (TOC) في مستند باستخدام أنماط العناوين كمدخلات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إدراج جدول محتويات للصفحة الأولى من المستند.
// تكوين الجدول لالتقاط الفقرات التي تحتوي على عناوين من المستوى 1 إلى 3.
// أيضًا، اضبط مدخلاته لتكون روابط تشعبية ستأخذنا
// إلى موقع العنوان عند النقر بزر الفأرة الأيسر في Microsoft Word.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// قم بملء جدول المحتويات بإضافة فقرات باستخدام أنماط العناوين.
// كل عنوان من هذا النوع بمستوى بين 1 و 3 سيُنشئ مدخلاً في الجدول.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// جدول المحتويات هو حقل من نوع يحتاج إلى تحديث لإظهار نتيجة محدثة.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```

## انظر أيضًا

* Class [Document](../../document/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) constructor


يُنشئ مثيلًا جديدًا لهذه الفئة.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::Document> &doc, const System::SharedPtr<Aspose::Words::DocumentBuilderOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | كائن [Document](../../document/) المراد إرفاقه. |
| خيارات | const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\& | خيارات إضافية لعملية بناء المستند. |

## أمثلة



يعرض كيفية تجاهل تنسيق الجدول للمحتوى التالي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// يضيف محتوى قبل الجدول.
// حجم الخط الافتراضي هو 12.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// يغيّر حجم الخط داخل الجدول.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// إذا كان ContextTableFormatting صحيحًا، فإن تنسيق الجدول لا يُطبق على المحتوى التالي.
// إذا كان ContextTableFormatting خاطئًا، فإن تنسيق الجدول يُطبق على المحتوى التالي.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## انظر أيضًا

* Class [Document](../../document/)
* Class [DocumentBuilderOptions](../../documentbuilderoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) constructor


يُنشئ مثيلًا جديدًا لهذه الفئة.

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::DocumentBuilderOptions> &options)
```


## أمثلة



يعرض كيفية تجاهل تنسيق الجدول للمحتوى التالي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// يضيف محتوى قبل الجدول.
// حجم الخط الافتراضي هو 12.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// يغيّر حجم الخط داخل الجدول.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// إذا كان ContextTableFormatting صحيحًا، فإن تنسيق الجدول لا يُطبق على المحتوى التالي.
// إذا كان ContextTableFormatting خاطئًا، فإن تنسيق الجدول يُطبق على المحتوى التالي.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## انظر أيضًا

* Class [DocumentBuilderOptions](../../documentbuilderoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
