---
title: "طريقة Aspose::Words::HeaderFooterCollection::LinkToPrevious"
linktitle: "LinkToPrevious"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::HeaderFooterCollection::LinkToPrevious. تربط أو تفك ربط الرأس أو التذييل المحدد إلى الرأس أو التذييل المقابل في القسم السابق في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/headerfootercollection/linktoprevious/
---
## HeaderFooterCollection::LinkToPrevious(Aspose::Words::HeaderFooterType, bool) method


يربط أو يفك ربط الرأس أو التذييل المحدد بالرأس أو التذييل المقابل في القسم السابق.

```cpp
void Aspose::Words::HeaderFooterCollection::LinkToPrevious(Aspose::Words::HeaderFooterType headerFooterType, bool isLinkToPrevious)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | قيمة [HeaderFooterType](../../headerfootertype/) التي تحدد الرأس أو التذييل للربط/فك الربط. |
| isLinkToPrevious | bool | **true** لربط الرأس أو التذييل بالقسم السابق؛ **false** لفك الربط. |
## ملاحظات


إذا لم يكن الرأس أو التذييل من النوع المحدد موجودًا، يتم إنشاؤه تلقائيًا.

## أمثلة



يظهر كيفية ربط الرؤوس والتذييلات بين الأقسام.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// انتقل إلى القسم الأول وأنشئ رأسًا وتذييلًا. بشكل افتراضي،
// سيظهر الرأس والتذييل فقط على الصفحات في القسم الذي يحتويهما.
builder->MoveToSection(0);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// يمكننا ربط رؤوس/تذييلات القسم بالرؤوس/التذييلات الخاصة بالقسم السابق
// للسماح للقسم الرابط بعرض رؤوس/تذييلات القسم المرتبط.
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// سيظل لكل قسم كائناته الخاصة من الرأس/التذييل. عندما نربط الأقسام،
// سيعرض القسم الرابط رؤوس/تذييلات القسم المرتبط مع الاحتفاظ بملكيته الخاصة.
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// ربط رؤوس/تذييلات القسم الثالث إلى رؤوس/تذييلات القسم الثاني.
// القسم الثاني يربط بالفعل إلى رؤوس/تذييلات القسم الأول،
// لذا ربط القسم الثاني سيخلق سلسلة ربط.
// القسم الأول، الثاني، والآن القسم الثالث سيعرضون جميعًا رؤوس القسم الأول.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// يمكننا فك ربط رؤوس/تذييلات قسم سابق بتمرير "false" عند استدعاء طريقة LinkToPrevious.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// يمكننا أيضًا اختيار نوع محدد فقط من الرأس/التذييل للربط باستخدام هذه الطريقة.
// القسم الثالث الآن سيحصل على نفس التذييل كما في القسمين الثاني والأول، لكن ليس الرأس.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(Aspose::Words::HeaderFooterType::FooterPrimary, true);

// رؤوس/تذييلات القسم الأول لا يمكنها ربط نفسها بأي شيء لأنه لا يوجد قسم سابق.
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// جميع رؤوس/تذييلات القسم الثاني مرتبطة برؤوس/تذييلات القسم الأول.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return (System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// In the third section, only the footer is linked to the first section's footer via the second section.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Link.docx");
```

## انظر أيضًا

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## HeaderFooterCollection::LinkToPrevious(bool) method


يربط أو يفك ربط جميع الرؤوس والتذييلات بالرؤوس والتذييلات المقابلة في القسم السابق.

```cpp
void Aspose::Words::HeaderFooterCollection::LinkToPrevious(bool isLinkToPrevious)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| isLinkToPrevious | bool | **true** لربط الرؤوس والتذييلات بالقسم السابق; **false** لفصلها. |
## ملاحظات


إذا لم يكن أي من الرؤوس أو التذييلات موجودًا، يتم إنشاؤها تلقائيًا.

## أمثلة



يظهر كيفية ربط الرؤوس والتذييلات بين الأقسام.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// انتقل إلى القسم الأول وأنشئ رأسًا وتذييلًا. بشكل افتراضي،
// سيظهر الرأس والتذييل فقط على الصفحات في القسم الذي يحتويهما.
builder->MoveToSection(0);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// يمكننا ربط رؤوس/تذييلات القسم بالرؤوس/التذييلات الخاصة بالقسم السابق
// للسماح للقسم الرابط بعرض رؤوس/تذييلات القسم المرتبط.
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// سيظل لكل قسم كائناته الخاصة من الرأس/التذييل. عندما نربط الأقسام،
// سيعرض القسم الرابط رؤوس/تذييلات القسم المرتبط مع الاحتفاظ بملكيته الخاصة.
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// ربط رؤوس/تذييلات القسم الثالث إلى رؤوس/تذييلات القسم الثاني.
// القسم الثاني يربط بالفعل إلى رؤوس/تذييلات القسم الأول،
// لذا ربط القسم الثاني سيخلق سلسلة ربط.
// القسم الأول، الثاني، والآن القسم الثالث سيعرضون جميعًا رؤوس القسم الأول.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// يمكننا فك ربط رؤوس/تذييلات قسم سابق بتمرير "false" عند استدعاء طريقة LinkToPrevious.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// يمكننا أيضًا اختيار نوع محدد فقط من الرأس/التذييل للربط باستخدام هذه الطريقة.
// القسم الثالث الآن سيحصل على نفس التذييل كما في القسمين الثاني والأول، لكن ليس الرأس.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(Aspose::Words::HeaderFooterType::FooterPrimary, true);

// رؤوس/تذييلات القسم الأول لا يمكنها ربط نفسها بأي شيء لأنه لا يوجد قسم سابق.
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// جميع رؤوس/تذييلات القسم الثاني مرتبطة برؤوس/تذييلات القسم الأول.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return (System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// In the third section, only the footer is linked to the first section's footer via the second section.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Link.docx");
```

## انظر أيضًا

* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
