---
title: "Aspose::Words::HeaderFooterCollection::LinkToPrevious yöntemi"
linktitle: "LinkToPrevious"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::HeaderFooterCollection::LinkToPrevious yöntemi. Belirtilen üstbilgi veya altbilgiyi önceki bölümdeki karşılık gelen üstbilgi veya altbilgiye bağlar veya bağını kaldırır C++ içinde."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/headerfootercollection/linktoprevious/
---
## HeaderFooterCollection::LinkToPrevious(Aspose::Words::HeaderFooterType, bool) method


Belirtilen başlık veya altbilgiyi önceki bölümdeki karşılık gelen başlık veya altbilgiye bağlar veya bağını kaldırır.

```cpp
void Aspose::Words::HeaderFooterCollection::LinkToPrevious(Aspose::Words::HeaderFooterType headerFooterType, bool isLinkToPrevious)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | Bağlanacak/bağlantısı kaldırılacak üstbilgi veya altbilgiyi belirten bir [HeaderFooterType](../../headerfootertype/) değeri. |
| isLinkToPrevious | bool | **true** üstbilgi veya altbilgiyi önceki bölüme bağlamak için; **false** bağını kaldırmak için. |
## Açıklamalar


Belirtilen türdeki üstbilgi veya altbilgi mevcut değilse, otomatik olarak oluşturur.

## Örnekler



Bölümler arasında üstbilgi ve altbilgileri nasıl bağlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// İlk bölüme geçin ve bir üstbilgi ile bir altbilgi oluşturun. Varsayılan olarak,
// üstbilgi ve altbilgi yalnızca onları içeren bölümdeki sayfalarda görünecektir.
builder->MoveToSection(0);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// Bir bölümün üstbilgi/altbilgilerini önceki bölümün üstbilgi/altbilgilerine bağlayabiliriz
// bağlayan bölümün, bağlanan bölümün üstbilgi/altbilgilerini görüntülemesine izin vermek için.
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// Her bölüm hâlâ kendi üstbilgi/altbilgi nesnelerine sahip olacaktır. Bölümleri bağladığımızda,
// bağlayan bölüm, kendi üstbilgi/altbilgilerini korurken bağlanan bölümün üstbilgi/altbilgilerini gösterecektir.
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// Üçüncü bölümün üstbilgi/altbilgilerini ikinci bölümün üstbilgi/altbilgilerine bağlayın.
// İkinci bölüm zaten birinci bölümün üstbilgi/altbilgilerine bağlanmıştır,
// bu yüzden ikinci bölüme bağlamak bir bağ zinciri oluşturur.
// Birinci, ikinci ve artık üçüncü bölümler, birinci bölümün üstbilgilerini gösterecek.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// LinkToPrevious yöntemini çağırırken "false" geçirerek önceki bir bölümün üstbilgi/altbilgilerini bağlamayı kaldırabiliriz.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// Bu yöntemi kullanarak yalnızca belirli bir üstbilgi/altbilgi türünü bağlamayı seçebiliriz.
// Üçüncü bölüm artık ikinci ve birinci bölümlerle aynı altbilgiye sahip olacak, ancak üstbilgiye sahip olmayacak.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(Aspose::Words::HeaderFooterType::FooterPrimary, true);

// Birinci bölümün üstbilgi/altbilgileri, önceki bir bölüm olmadığı için kendilerini hiçbir şeye bağlayamaz.
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// İkinci bölümün tüm üstbilgi/altbilgileri birinci bölümün üstbilgi/altbilgilerine bağlanmıştır.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return (System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Üçüncü bölümde, yalnızca alt bilgi, ikinci bölüm aracılığıyla birinci bölümün alt bilgisine bağlanır.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Link.docx");
```

## Ayrıca Bakınız

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## HeaderFooterCollection::LinkToPrevious(bool) method


Tüm başlıkları ve altbilgileri önceki bölümdeki karşılık gelen başlık ve altbilgilere bağlar veya bağlarını kaldırır.

```cpp
void Aspose::Words::HeaderFooterCollection::LinkToPrevious(bool isLinkToPrevious)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| isLinkToPrevious | bool | **true** başlıkları ve alt bilgileri önceki bölüme bağlamak için; **false** bağlarını kaldırmak için. |
## Açıklamalar


Başlıkların veya alt bilgilerin herhangi biri mevcut değilse, otomatik olarak oluşturulur.

## Örnekler



Bölümler arasında üstbilgi ve altbilgileri nasıl bağlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// İlk bölüme geçin ve bir üstbilgi ile bir altbilgi oluşturun. Varsayılan olarak,
// üstbilgi ve altbilgi yalnızca onları içeren bölümdeki sayfalarda görünecektir.
builder->MoveToSection(0);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// Bir bölümün üstbilgi/altbilgilerini önceki bölümün üstbilgi/altbilgilerine bağlayabiliriz
// bağlayan bölümün, bağlanan bölümün üstbilgi/altbilgilerini görüntülemesine izin vermek için.
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// Her bölüm hâlâ kendi üstbilgi/altbilgi nesnelerine sahip olacaktır. Bölümleri bağladığımızda,
// bağlayan bölüm, kendi üstbilgi/altbilgilerini korurken bağlanan bölümün üstbilgi/altbilgilerini gösterecektir.
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// Üçüncü bölümün üstbilgi/altbilgilerini ikinci bölümün üstbilgi/altbilgilerine bağlayın.
// İkinci bölüm zaten birinci bölümün üstbilgi/altbilgilerine bağlanmıştır,
// bu yüzden ikinci bölüme bağlamak bir bağ zinciri oluşturur.
// Birinci, ikinci ve artık üçüncü bölümler, birinci bölümün üstbilgilerini gösterecek.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// LinkToPrevious yöntemini çağırırken "false" geçirerek önceki bir bölümün üstbilgi/altbilgilerini bağlamayı kaldırabiliriz.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// Bu yöntemi kullanarak yalnızca belirli bir üstbilgi/altbilgi türünü bağlamayı seçebiliriz.
// Üçüncü bölüm artık ikinci ve birinci bölümlerle aynı altbilgiye sahip olacak, ancak üstbilgiye sahip olmayacak.
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(Aspose::Words::HeaderFooterType::FooterPrimary, true);

// Birinci bölümün üstbilgi/altbilgileri, önceki bir bölüm olmadığı için kendilerini hiçbir şeye bağlayamaz.
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// İkinci bölümün tüm üstbilgi/altbilgileri birinci bölümün üstbilgi/altbilgilerine bağlanmıştır.
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return (System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// Üçüncü bölümde, yalnızca alt bilgi, ikinci bölüm aracılığıyla birinci bölümün alt bilgisine bağlanır.
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Link.docx");
```

## Ayrıca Bakınız

* Class [HeaderFooterCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
