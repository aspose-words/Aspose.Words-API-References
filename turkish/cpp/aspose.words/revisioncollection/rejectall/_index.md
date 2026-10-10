---
title: "Aspose::Words::RevisionCollection::RejectAll yöntemi"
linktitle: "RejectAll"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::RevisionCollection::RejectAll yöntemi. C++'ta bu koleksiyondaki tüm revizyonları reddeder."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/revisioncollection/rejectall/
---
## RevisionCollection::RejectAll method


Bu koleksiyondaki tüm revizyonları reddeder.

```cpp
void Aspose::Words::RevisionCollection::RejectAll()
```


## Örnekler



Bir belgenin revizyon koleksiyonu ile nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");
System::SharedPtr<Aspose::Words::RevisionCollection> revisions = doc->get_Revisions();

// Bu koleksiyonun kendisi bir revizyon grubu koleksiyonuna sahiptir.
// Her grup, yan yana gelen revizyonların bir dizisidir.
std::cout << System::String::Format(u"{0} revision groups:", revisions->get_Groups()->get_Count()) << std::endl;

// Grupların koleksiyonunu yineleyin ve revizyonun ilgili olduğu metni yazdırın.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::RevisionGroup>>> e = revisions->get_Groups()->GetEnumerator();
    while (e->MoveNext())
    {
        std::cout << (System::String::Format(u"\tGroup type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_Text().Trim())) << std::endl;
    }
}

// Bir revizyonun etkilediği her Run, karşılık gelen bir Revision nesnesi alır.
// Revizyonların koleksiyonu, yukarıda yazdırdığımız sıkıştırılmış formdan oldukça daha büyüktür,
// Microsoft Word düzenlemesi sırasında belgeyi kaç Run'a bölüştüğümüze bağlı olarak.
std::cout << System::String::Format(u"\n{0} revisions:", revisions->get_Count()) << std::endl;

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Revision>>> e = revisions->GetEnumerator();
    while (e->MoveNext())
    {
        // Bir StyleDefinitionChange yalnızca stilleri etkiler ve belge düğümlerini etkilemez. Bu, "ParentStyle"
        // özelliğinin her zaman kullanılacağı, ParentNode'un ise her zaman null olacağı anlamına gelir.
        // Diğer tüm değişiklikler düğümleri etkilediğinden, ParentNode tersine kullanılacak ve ParentStyle null olacaktır.
        if (e->get_Current()->get_RevisionType() == Aspose::Words::RevisionType::StyleDefinitionChange)
        {
            std::cout << (System::String::Format(u"\tRevision type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, style: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_ParentStyle()->get_Name())) << std::endl;
        }
        else
        {
            std::cout << (System::String::Format(u"\tRevision type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_ParentNode()->GetText().Trim())) << std::endl;
        }
    }
}

// Koleksiyon aracılığıyla tüm revizyonları reddedin, belgeyi orijinal haline geri döndürün.
revisions->RejectAll();

ASSERT_EQ(0, revisions->get_Count());
```

## Ayrıca Bakınız

* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
