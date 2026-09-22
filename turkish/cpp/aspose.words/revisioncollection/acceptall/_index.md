---
title: "Aspose::Words::RevisionCollection::AcceptAll yöntemi"
linktitle: "AcceptAll"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::RevisionCollection::AcceptAll yöntemi. C++'ta bu koleksiyondaki tüm revizyonları kabul eder."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection::AcceptAll method


Bu koleksiyondaki tüm revizyonları kabul eder.

```cpp
void Aspose::Words::RevisionCollection::AcceptAll()
```


## Örnekler



Belgelerin nasıl karşılaştırılacağını gösterir.
```cpp
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);
builder->Writeln(u"This is the original document.");

auto docEdited = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docEdited);
builder->Writeln(u"This is the edited document.");

// Revizyonlu belgeleri karşılaştırmak bir istisna fırlatır.
if (docOriginal->get_Revisions()->get_Count() == 0 && docEdited->get_Revisions()->get_Count() == 0)
{
    docOriginal->Compare(docEdited, u"authorName", System::DateTime::get_Now());
}

// Karşılaştırmadan sonra, orijinal belge yeni bir revizyon kazanacaktır
// düzenlenmiş belgede farklı olan her öğe için.
for (auto&& r : System::IterateOver(docOriginal->get_Revisions()))
{
    std::cout << System::String::Format(u"Revision type: {0}, on a node of type \"{1}\"", r->get_RevisionType(), r->get_ParentNode()->get_NodeType()) << std::endl;
    std::cout << System::String::Format(u"\tChanged text: \"{0}\"", r->get_ParentNode()->GetText()) << std::endl;
}

// Bu revizyonları kabul etmek, orijinal belgeyi düzenlenmiş belgeye dönüştürecektir.
docOriginal->get_Revisions()->AcceptAll();

ASSERT_EQ(docOriginal->GetText(), docEdited->GetText());
```

## Ayrıca Bakınız

* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
