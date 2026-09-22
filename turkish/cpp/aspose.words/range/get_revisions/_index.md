---
title: "Aspose::Words::Range::get_Revisions yöntemi"
linktitle: "get_Revisions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Range::get_Revisions yöntemi. C++'da bu aralıkta bulunan revizyonların (izlenen değişiklikler) bir koleksiyonunu alır."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/range/get_revisions/
---
## Range::get_Revisions method


Bu aralıkta mevcut olan revizyonların (izlenen değişiklikler) bir koleksiyonunu alır.

```cpp
System::SharedPtr<Aspose::Words::RevisionCollection> Aspose::Words::Range::get_Revisions()
```

## Açıklamalar


Döndürülen koleksiyon bir "canlı" koleksiyondur, bu da belge içinde revizyon içeren bölümleri kaldırırsanız, silinen revizyonların bu koleksiyondan otomatik olarak kaybolacağı anlamına gelir.

## Örnekler



Aralıktaki revizyonlarla nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
for (auto&& revision : System::IterateOver(paragraph->get_Range()->get_Revisions()))
{
    if (revision->get_RevisionType() == Aspose::Words::RevisionType::Deletion)
    {
        revision->Accept();
    }
}

// İlk bölüm revizyonlarını reddedin.
doc->get_FirstSection()->get_Range()->get_Revisions()->RejectAll();
```

## Ayrıca Bakınız

* Class [RevisionCollection](../../revisioncollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
