---
title: "Aspose::Words::WarningInfoCollection sınıfı"
linktitle: "WarningInfoCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::WarningInfoCollection sınıfı. WarningInfo nesnelerinin tiplenmiş bir koleksiyonunu temsil eder. Daha fazla bilgi için C++ belgelerindeki makaleyi ziyaret edin."
type: docs
weight: 75000
url: /tr/cpp/aspose.words/warninginfocollection/
---
## WarningInfoCollection class


WarningInfo nesnelerinin tiplenmiş bir koleksiyonunu temsil eder. Daha fazla bilgi için [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) belgelerindeki makaleyi ziyaret edin.

```cpp
class WarningInfoCollection : public Aspose::Words::IWarningCallback,
                              public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::WarningInfo>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Koleksiyonda bulunan eleman sayısını alır. |
| [GetEnumerator](./getenumerator/)() override | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki öğeyi alır. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
| [Warning](./warning/)(System::SharedPtr\<Aspose::Words::WarningInfo\>) override | [IWarningCallback](../iwarningcallback/) arayüzünü uygular. Bu koleksiyona bir uyarı ekler. |
| [WarningInfoCollection](./warninginfocollection/)() |  |
## Typedefs

| Typedef | Açıklama |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Açıklamalar


Bu koleksiyon nesnesini, Aspose.Words'ün yükleme veya kaydetme işlemi sırasında ürettiği tüm uyarıları toplamak için en basit [IWarningCallback](../iwarningcallback/) uygulaması biçimi olarak kullanabilirsiniz. Bu sınıfın bir örneğini oluşturun ve onu [WarningCallback](../../aspose.words.loading/loadoptions/get_warningcallback/) veya [WarningCallback](../documentbase/get_warningcallback/) özelliğine atayın.

## Örnekler



Mevcut yazı tipi kaynaklarından eksik bir yazı tipi için en yakın eşleşmeyi bulmak üzere özelliği nasıl ayarlayacağınızı gösterir.
```cpp
// Yazı tipi kaynaklarımızın hiçbirinde bulunmayan bir yazı tipiyle biçimlendirilmiş metin içeren bir belge açın.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Yazı tipi ikame uyarılarını işlemek için bir geri çağırma atayın.
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// Varsayılan bir yazı tipi adı ayarlayın ve yazı tipi ikamesini etkinleştirin.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// Yazı tipi ikamesinden sonra orijinal yazı tipi ölçümleri kullanılmalıdır.
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// Eksik bir yazı tipiyle bir belgeyi kaydedersek yazı tipi ikamesi uyarısı alacağız.
doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.EnableFontSubstitution.pdf");

for (auto&& info : warningCollector)
{
    if (info->get_WarningType() == Aspose::Words::WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```

## Ayrıca Bakınız

* Interface [IWarningCallback](../iwarningcallback/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
