---
title: "Aspose::Words::Notes::FootnoteOptions::get_Position yöntemi"
linktitle: "get_Position"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::FootnoteOptions::get_Position yöntemi. C++'ta dipnotların konumunu belirtir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.notes/footnoteoptions/get_position/
---
## FootnoteOptions::get_Position method


Dipnotların konumunu belirtir.

```cpp
Aspose::Words::Notes::FootnotePosition Aspose::Words::Notes::FootnoteOptions::get_Position()
```


## Örnekler



Belgenin dipnotları topladığı ve görüntülediği farklı bir yeri nasıl seçeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Dipnot, metne bir referans veya yan yorum eklemenin bir yoludur.
// ana metin akışına müdahale etmeyen.
// Bir dipnot eklemek, küçük bir üst simge referans işareti ekler.
// dipnotu eklediğimiz ana metin içinde.
// Her dipnot ayrıca sayfanın alt kısmında bir giriş oluşturur; bu giriş bir simgeden oluşur.
// ana metindeki referans işaretiyle eşleşen.
// Belge oluşturucunun "InsertFootnote" metoduna geçtiğimiz referans metni.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote contents.");

// "Position" özelliğini kullanarak belgenin tüm dipnotları nereye yerleştireceğini belirleyebiliriz.
// "Position" özelliğinin değerini "FootnotePosition.BottomOfPage" olarak ayarlarsak,
// her dipnot, referans işaretini içeren sayfanın alt kısmında görünecektir. Bu varsayılan değerdir.
// "Position" özelliğinin değerini "FootnotePosition.BeneathText" olarak ayarlarsak,
// her dipnot, referans işaretini içeren sayfanın metninin sonunda görünecektir.
doc->get_FootnoteOptions()->set_Position(footnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionFootnote.docx");
```

## Ayrıca Bakınız

* Enum [FootnotePosition](../../footnoteposition/)
* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
