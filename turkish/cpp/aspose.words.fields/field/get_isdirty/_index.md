---
title: "Aspose::Words::Fields::Field::get_IsDirty yöntemi"
linktitle: "get_IsDirty"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::Field::get_IsDirty yöntemi. Alanın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar C++'ta."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.fields/field/get_isdirty/
---
## Field::get_IsDirty method


Alan'ın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar.

```cpp
bool Aspose::Words::Fields::Field::get_IsDirty()
```


## Örnekler



Alan sonucunu güncellemek için özel özelliğin nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgenin yerleşik "Author" (Yazar) özelliği değerini verin ve ardından bir alanla görüntüleyin.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));

ASSERT_FALSE(field->get_IsDirty());
ASSERT_EQ(u"John Doe", field->get_Result());

// Özelliği güncelleyin. Alan hâlâ eski değeri gösteriyor.
doc->get_BuiltInDocumentProperties()->set_Author(u"John & Jane Doe");

ASSERT_EQ(u"John Doe", field->get_Result());

// Alan değerinin güncel olmaması nedeniyle, onu "dirty" (kirli) olarak işaretleyebiliriz.
// Bu değer, Field.Update() yöntemiyle alanı manuel olarak güncelleyinceye kadar güncel kalmayacak.
field->set_IsDirty(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    // Bir güncelleme yöntemi çağırmadan kaydederseniz,
    // alan, çıktı belgesinde güncel olmayan değeri göstermeye devam edecektir.
    doc->Save(docStream, Aspose::Words::SaveFormat::Docx);

    // LoadOptions nesnesinin tüm alanları güncelleme seçeneği vardır
    // belge yüklendiğinde "dirty" (kirli) olarak işaretlenir.
    auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    options->set_UpdateDirtyFields(updateDirtyFields);
    doc = System::MakeObject<Aspose::Words::Document>(docStream, options);

    ASSERT_EQ(u"John & Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());

    field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(doc->get_Range()->get_Fields()->idx_get(0));

    // Kirli alanları bu şekilde güncellemek, otomatik olarak "IsDirty" bayrağını false olarak ayarlar.
    if (updateDirtyFields)
    {
        ASSERT_EQ(u"John & Jane Doe", field->get_Result());
        ASSERT_FALSE(field->get_IsDirty());
    }
    else
    {
        ASSERT_EQ(u"John Doe", field->get_Result());
        ASSERT_TRUE(field->get_IsDirty());
    }
}
```

## Ayrıca Bakınız

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
