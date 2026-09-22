---
title: "Aspose::Words::Loading::TxtTrailingSpacesOptions enum"
linktitle: "TxtTrailingSpacesOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::TxtTrailingSpacesOptions enum. C++'da Metin dosyasından içe aktarım sırasında satır sonu boşluklarının işlenmesi için mevcut seçenekleri belirtir."
type: docs
weight: 19000
url: /tr/cpp/aspose.words.loading/txttrailingspacesoptions/
---
## TxtTrailingSpacesOptions enum


Satır sonu boşluklarının işlenmesi için mevcut seçenekleri, [Text](../../aspose.words/loadformat/) dosyasından içe aktarım sırasında belirtir.

```cpp
enum class TxtTrailingSpacesOptions
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Trim | 0 | Satır sonu boşlukları kırpılır. |
| Preserve | 1 | Satır sonu boşlukları korunur. |


## Örnekler



Düz metin belgeleri yüklenirken boşlukların nasıl kırpılacağını gösterir.
```cpp
System::String textDoc = System::String(u"      Line 1 \n") + u"    Line 2   \n" + u" Line 3       ";

// "TxtLoadOptions" nesnesi oluşturun, bunu bir belgenin yapıcısına geçirebiliriz
// düz metin belgesini nasıl yüklediğimizi değiştirmek için.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// "LeadingSpacesOptions" özelliğini "TxtLeadingSpacesOptions.Preserve" olarak ayarlayın.
// her satırın başındaki tüm boşluk karakterlerini korumak için.
// "LeadingSpacesOptions" özelliğini "TxtLeadingSpacesOptions.ConvertToIndent" olarak ayarlayın
// her satırın başındaki tüm boşluk karakterlerini kaldırmak için,
// ve ardından paragrafın ilk satırına sol girinti uygulayarak boşlukların etkisini taklit edin.
// "LeadingSpacesOptions" özelliğini "TxtLeadingSpacesOptions.Trim" olarak ayarlayın
// her satırın başındaki tüm boşluk karakterlerini kaldırmak için.
loadOptions->set_LeadingSpacesOptions(txtLeadingSpacesOptions);

// "TrailingSpacesOptions" özelliğini "TxtTrailingSpacesOptions.Preserve" olarak ayarlayın
// her satırın sonundaki tüm boşluk karakterlerini korumak için.
// "TrailingSpacesOptions" özelliğini "TxtTrailingSpacesOptions.Trim" olarak ayarlayın
// her satırın sonundaki tüm boşluk karakterlerini kaldırın.
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

## Ayrıca Bakınız

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
