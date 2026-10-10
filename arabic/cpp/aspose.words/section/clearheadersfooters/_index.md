---
title: "Aspose::Words::Section::ClearHeadersFooters method"
linktitle: "ClearHeadersFooters"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Section::ClearHeadersFooters method. يمسح رؤوس وتذييلات هذا القسم في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words/section/clearheadersfooters/
---
## Section::ClearHeadersFooters() method


يمسح رؤوس وتذييلات هذا القسم.

```cpp
void Aspose::Words::Section::ClearHeadersFooters()
```

## ملاحظات


يتم مسح نص جميع الرؤوس والتذييلات، لكن كائنات [HeaderFooter](../../headerfooter/) نفسها لا تُزال.

هذا يجعل رؤوس وتذييلات هذا القسم مرتبطة برؤوس وتذييلات القسم السابق.

## أمثلة



يظهر كيفية مسح محتويات جميع الرؤوس والتذييلات في قسم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(0, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Writeln(u"This is the primary header.");
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Writeln(u"This is the primary footer.");

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(u"This is the primary header.", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"This is the primary footer.", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());

// إفراغ جميع الرؤوس والتذييلات في هذا القسم من جميع محتوياتها.
// ستظل الرؤوس والتذييلات نفسها موجودة ولكن لن يكون لديها ما تعرضه.
doc->get_FirstSection()->ClearHeadersFooters();

ASSERT_EQ(2, doc->get_FirstSection()->get_HeadersFooters()->get_Count());

ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(System::String::Empty, doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
```

## انظر أيضًا

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Section::ClearHeadersFooters(bool) method


يمسح رؤوس وتذييلات هذا القسم.

```cpp
void Aspose::Words::Section::ClearHeadersFooters(bool preserveWatermarks)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| preserveWatermarks | bool | صحيح إذا كان يجب عدم إزالة العلامات المائية. |
## ملاحظات


يتم مسح نص جميع الرؤوس والتذييلات، لكن كائنات [HeaderFooter](../../headerfooter/) نفسها لا تُزال.

هذا يجعل رؤوس وتذييلات هذا القسم مرتبطة برؤوس وتذييلات القسم السابق.

## أمثلة



يظهر كيفية مسح محتويات الرأس والتذييل مع أو بدون علامة مائية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// أضف علامة مائية نصية عادية.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// تأكد من أن الرؤوس والتذييلات تحتوي على محتوى.
System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"First header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"Second header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"Third header", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"First footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"Second footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"Third footer", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());

// يزيل جميع محتويات الرأس والتذييل باستثناء العلامات المائية.
doc->get_FirstSection()->ClearHeadersFooters(true);

headersFooters = doc->get_FirstSection()->get_HeadersFooters();
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::HeaderPrimary)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterFirst)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterEven)->GetText().Trim());
ASSERT_EQ(u"", headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary)->GetText().Trim());
ASSERT_EQ(Aspose::Words::WatermarkType::Text, doc->get_Watermark()->get_Type());

// يزيل جميع محتويات الرأس والتذييل بما في ذلك العلامات المائية.
doc->get_FirstSection()->ClearHeadersFooters(false);
ASSERT_EQ(Aspose::Words::WatermarkType::None, doc->get_Watermark()->get_Type());
```

## انظر أيضًا

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
