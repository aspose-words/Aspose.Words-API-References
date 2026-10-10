---
title: "Aspose::Words::Markup::SdtListItemCollection class"
linktitle: "SdtListItemCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::SdtListItemCollection sınıfı. Bir yapılandırılmış belge etiketinin SdtListItem öğelerine erişim sağlar. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class


Bir yapılandırılmış belge etiketinin [SdtListItem](../sdtlistitem/) öğelerine erişim sağlar. Daha fazla bilgi için [Yapılandırılmış Belge Etiketleri veya İçerik Kontrolü](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) belge makalesini ziyaret edin.

```cpp
class SdtListItemCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::SdtListItem\>\&) | Bu koleksiyona bir öğe ekler. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Bu koleksiyondaki tüm öğeleri temizler. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Koleksiyondaki öğe sayısını alır. |
| [get_SelectedValue](./get_selectedvalue/)() | Bu listede şu anda seçili değeri belirtir. Boş değer izin verilir, bu da şu anda seçili bir girişin bu liste öğesi koleksiyonuyla ilişkili olmadığı anlamına gelir. |
| [GetEnumerator](./getenumerator/)() override | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Koleksiyondaki sıfır tabanlı indeksine göre bir [SdtListItem](../sdtlistitem/) nesnesi döndürür. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Belirtilen indeksdeki bir liste öğesini kaldırır. |
| [set_SelectedValue](./set_selectedvalue/)(const System::SharedPtr\<Aspose::Words::Markup::SdtListItem\>\&) | Ayarlayıcı: [Aspose::Words::Markup::SdtListItemCollection::get_SelectedValue](./get_selectedvalue/). |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Açıklama |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

## Örnekler



Açılır liste yapılandırılmış belge etiketleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::DropDownList, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// Açılır liste yapılandırılmış belge etiketi, kullanıcının
// Microsoft Word'de formu sol tıklayarak açıp bir listeden seçenek seçmesini sağlar.
//  \"ListItems\" özelliği tüm liste öğelerini içerir ve her liste öğesi bir \"SdtListItem\"dır.
System::SharedPtr<Aspose::Words::Markup::SdtListItemCollection> listItems = tag->get_ListItems();
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Value 1"));

ASSERT_EQ(listItems->idx_get(0)->get_DisplayText(), listItems->idx_get(0)->get_Value());

// 3 tane daha liste öğesi ekleyin. Bu öğeleri ilk öğeden farklı bir yapıcı kullanarak başlatın
// değerlerinden farklı dizeler görüntülemek için.
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 2", u"Value 2"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 3", u"Value 3"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 4", u"Value 4"));

ASSERT_EQ(4, listItems->get_Count());

// Açılır liste ilk öğeyi gösteriyor. Görüntülemek için "SelectedValue" özelliğine farklı bir liste öğesi atayın.
listItems->set_SelectedValue(listItems->idx_get(3));

ASSERT_EQ(u"Value 4", listItems->get_SelectedValue()->get_Value());

// Koleksiyon üzerinde yineleme yapın ve her öğeyi yazdırın.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>> enumerator = listItems->GetEnumerator();
    while (enumerator->MoveNext())
    {
        if (enumerator->get_Current() != nullptr)
        {
            std::cout << System::String::Format(u"List item: {0}, value: {1}", enumerator->get_Current()->get_DisplayText(), enumerator->get_Current()->get_Value()) << std::endl;
        }
    }
}

// Son liste öğesini kaldırın.
listItems->RemoveAt(3);

ASSERT_EQ(3, listItems->get_Count());

// Açılır denetimimiz varsayılan olarak kaldırılan öğeyi göstermeye ayarlandığından, mevcut bir öğe vererek göstermesini sağlayın.
listItems->set_SelectedValue(listItems->idx_get(1));

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.ListItemCollection.docx");

// "Clear" yöntemini kullanarak tüm açılır öğe koleksiyonunu bir kerede boşaltın.
listItems->Clear();

ASSERT_EQ(0, listItems->get_Count());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
