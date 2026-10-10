---
title: "Aspose::Words::BorderCollection::GetEnumerator metodu"
linktitle: "GetEnumerator"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BorderCollection::GetEnumerator yöntemi. Koleksiyondaki tüm kenarlarda yineleme yapmak için kullanılabilecek bir yineleyici nesnesi döndürür C++'da."
type: docs
weight: 16000
url: /tr/cpp/aspose.words/bordercollection/getenumerator/
---
## BorderCollection::GetEnumerator method


Koleksiyondaki tüm kenarları yinelemek için kullanılabilecek bir enumerator nesnesi döndürür.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Border>>> Aspose::Words::BorderCollection::GetEnumerator() override
```


## Örnekler



Bir paragraf biçim nesnesindeki tüm kenarları nasıl yineleyeceğinizi ve düzenleyeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Yapıcının paragraf biçim ayarlarını, tüm kenarlarda yeşil dalga kenarı oluşturacak şekilde yapılandırın.
System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Border>>> enumerator = borders->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::Border> border = enumerator->get_Current();
        border->set_Color(System::Drawing::Color::get_Green());
        border->set_LineStyle(Aspose::Words::LineStyle::Wave);
        border->set_LineWidth(3);
    }
}

// Bir paragraf ekleyin. Kenar ayarlarımız, kenarının görünümünü belirleyecek.
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"BorderCollection.GetBordersEnumerator.docx");
```

## Ayrıca Bakınız

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
