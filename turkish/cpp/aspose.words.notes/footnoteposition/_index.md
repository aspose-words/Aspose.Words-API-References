---
title: "Aspose::Words::Notes::FootnotePosition enum"
linktitle: "FootnotePosition"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::FootnotePosition enum. C++'da dipnot konumunu tanımlar."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.notes/footnoteposition/
---
## FootnotePosition enum


Dipnot konumunu tanımlar.

```cpp
enum class FootnotePosition
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| BottomOfPage | 1 | Dipnotlar her sayfanın alt kısmında görüntülenir. |
| BeneathText | 2 | Dipnotlar her sayfada metnin altında görüntülenir. |


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

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
