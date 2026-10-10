---
title: "Aspose::Words::Notes::EndnotePosition enum"
linktitle: "EndnotePosition"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::EndnotePosition enum. C++'da dipnot konumunu tanımlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.notes/endnoteposition/
---
## EndnotePosition enum


Dipnot konumunu tanımlar.

```cpp
enum class EndnotePosition
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| EndOfSection | 0 | Dipnotlar bölümün sonunda çıkarılır. |
| EndOfDocument | 3 | Dipnotlar belgenin sonunda çıkarılır. |


## Örnekler



Belgenin dipnotları topladığı ve gösterdiği farklı bir yeri nasıl seçeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir dipnot, metne bir referans veya yan yorum eklemenin bir yoludur.
// ana metin akışına müdahale etmeyen.
// Bir dipnot eklemek, küçük bir üst simge referans işareti ekler
// dipnot eklediğimiz ana metin içinde
// Her dipnot ayrıca belge sonunda bir giriş oluşturur, bir işaretten oluşur
// ana metindeki referans işaretiyle eşleşen.
// Belge oluşturucunun "InsertEndnote" metoduna geçirdiğimiz referans metni.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote contents.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"This is the second section.");

// Belgenin tüm dipnotlarını nereye yerleştireceğini belirlemek için "Position" özelliğini kullanabiliriz.
// Eğer "Position" özelliğinin değerini "EndnotePosition.EndOfDocument" olarak ayarlarsak,
// her dipnot belge sonunda bir koleksiyonda görünecektir. Bu varsayılan değerdir.
// Eğer "Position" özelliğinin değerini "EndnotePosition.EndOfSection" olarak ayarlarsak,
// her dipnot, dipnotun referans işaretini içeren metnin bulunduğu bölümün sonunda bir koleksiyonda görünecektir.
doc->get_EndnoteOptions()->set_Position(endnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionEndnote.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
