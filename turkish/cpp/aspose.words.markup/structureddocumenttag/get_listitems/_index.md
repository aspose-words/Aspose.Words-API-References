---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_ListItems yöntemi"
linktitle: "get_ListItems"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_ListItems yöntemi. Bu SDT ile ilişkili SdtListItemCollection'ı C++ içinde alır."
type: docs
weight: 21000
url: /tr/cpp/aspose.words.markup/structureddocumenttag/get_listitems/
---
## StructuredDocumentTag::get_ListItems method


Bu **SDT** ile ilişkili [SdtListItemCollection](../../sdtlistitemcollection/) alır.

```cpp
System::SharedPtr<Aspose::Words::Markup::SdtListItemCollection> Aspose::Words::Markup::StructuredDocumentTag::get_ListItems()
```

## Açıklamalar


Bu özelliğe erişim yalnızca [ComboBox](../../sdttype/) veya [DropDownList](../../sdttype/) SDT türleri için çalışır.

Diğer tüm SDT türleri için bir istisna oluşacaktır.

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

* Class [SdtListItemCollection](../../sdtlistitemcollection/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
