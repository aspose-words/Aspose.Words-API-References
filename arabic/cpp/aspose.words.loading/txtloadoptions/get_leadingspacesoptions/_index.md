---
title: "طريقة Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions"
linktitle: "get_LeadingSpacesOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions. يحصل أو يضبط الخيار المفضل لمعالجة المسافات الرائدة. القيمة الافتراضية هي ConvertToIndent في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.loading/txtloadoptions/get_leadingspacesoptions/
---
## TxtLoadOptions::get_LeadingSpacesOptions method


يحصل أو يضبط الخيار المفضل لمعالجة المسافات الرائدة. القيمة الافتراضية هي [ConvertToIndent](../../txtleadingspacesoptions/).

```cpp
Aspose::Words::Loading::TxtLeadingSpacesOptions Aspose::Words::Loading::TxtLoadOptions::get_LeadingSpacesOptions() const
```


## أمثلة



يعرض كيفية قص المسافات البيضاء عند تحميل مستندات نصية عادية.
```cpp
System::String textDoc = System::String(u"      Line 1 \n") + u"    Line 2   \n" + u" Line 3       ";

// إنشاء كائن "TxtLoadOptions"، والذي يمكننا تمريره إلى مُنشئ المستند
// لتعديل طريقة تحميل المستند النصي.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// اضبط الخاصية "LeadingSpacesOptions" إلى "TxtLeadingSpacesOptions.Preserve"
// للحفاظ على جميع أحرف المسافات البيضاء في بداية كل سطر.
// اضبط خاصية \"LeadingSpacesOptions\" إلى \"TxtLeadingSpacesOptions.ConvertToIndent\"
// لإزالة جميع أحرف المسافات البيضاء من بداية كل سطر،
// ثم طبق مسافة بادئة للسطر الأول إلى اليسار على الفقرة لمحاكاة تأثير المسافات البيضاء.
// اضبط خاصية \"LeadingSpacesOptions\" إلى \"TxtLeadingSpacesOptions.Trim\"
// لإزالة جميع أحرف المسافات البيضاء من بداية كل سطر.
loadOptions->set_LeadingSpacesOptions(txtLeadingSpacesOptions);

// اضبط خاصية \"TrailingSpacesOptions\" إلى \"TxtTrailingSpacesOptions.Preserve\"
// للحفاظ على جميع أحرف المسافات البيضاء في نهاية كل سطر.
// اضبط خاصية \"TrailingSpacesOptions\" إلى \"TxtTrailingSpacesOptions.Trim\" لت
// إزالة جميع أحرف المسافات البيضاء من نهاية كل سطر.
loadOptions->set_TrailingSpacesOptions(txtTrailingSpacesOptions);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(textDoc)), loadOptions);
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

switch (txtLeadingSpacesOptions)
{
    case Aspose::Words::Loading::TxtLeadingSpacesOptions::ConvertToIndent:
        ASPOSE_ASSERT_EQ(37.8, paragraphs->idx_get(0)->get_ParagraphFormat()->get_FirstLineIndent());
        ASPOSE_ASSERT_EQ(25.2, paragraphs->idx_get(1)->get_ParagraphFormat()->get_FirstLineIndent());
        ASPOSE_ASSERT_EQ(6.3, paragraphs->idx_get(2)->get_ParagraphFormat()->get_FirstLineIndent());
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"Line 1"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"Line 2"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u"Line 3"));
        break;

    case Aspose::Words::Loading::TxtLeadingSpacesOptions::Preserve:
        ASSERT_TRUE(paragraphs->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
        {
            return (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_ParagraphFormat()->get_FirstLineIndent() == 0.0;
        }))));
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"      Line 1"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"    Line 2"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u" Line 3"));
        break;

    case Aspose::Words::Loading::TxtLeadingSpacesOptions::Trim:
        ASSERT_TRUE(paragraphs->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
        {
            return (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_ParagraphFormat()->get_FirstLineIndent() == 0.0;
        }))));
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().StartsWith(u"Line 1"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().StartsWith(u"Line 2"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().StartsWith(u"Line 3"));
        break;

}

switch (txtTrailingSpacesOptions)
{
    case Aspose::Words::Loading::TxtTrailingSpacesOptions::Preserve:
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().EndsWith(u"Line 1 \r"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().EndsWith(u"Line 2   \r"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().EndsWith(u"Line 3       \f"));
        break;

    case Aspose::Words::Loading::TxtTrailingSpacesOptions::Trim:
        ASSERT_TRUE(paragraphs->idx_get(0)->GetText().EndsWith(u"Line 1\r"));
        ASSERT_TRUE(paragraphs->idx_get(1)->GetText().EndsWith(u"Line 2\r"));
        ASSERT_TRUE(paragraphs->idx_get(2)->GetText().EndsWith(u"Line 3\f"));
        break;

}
```

## انظر أيضًا

* Enum [TxtLeadingSpacesOptions](../../txtleadingspacesoptions/)
* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
