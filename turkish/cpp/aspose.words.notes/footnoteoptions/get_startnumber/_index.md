---
title: "Aspose::Words::Notes::FootnoteOptions::get_StartNumber yöntemi"
linktitle: "get_StartNumber"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::FootnoteOptions::get_StartNumber yöntemi. C++'ta ilk otomatik numaralandırılmış dipnotlar için başlangıç numarasını veya karakterini belirtir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.notes/footnoteoptions/get_startnumber/
---
## FootnoteOptions::get_StartNumber method


İlk otomatik numaralandırılmış dipnotlar için başlangıç numarasını veya karakterini belirtir.

```cpp
int32_t Aspose::Words::Notes::FootnoteOptions::get_StartNumber() override
```

## Açıklamalar


Bu özellik yalnızca [RestartRule](../get_restartrule/) [Continuous](../../footnotenumberingrule/) olarak ayarlandığında etkili olur.

## Örnekler



Belgenin dipnot/sonnot sayımına başlayacağı sayıyı nasıl ayarlayacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Dipnotlar ve sonnotlar, metne bir referans veya yan yorum eklemenin bir yoludur.
// ana metin akışına müdahale etmeyen.
// Bir dipnot/sonnot eklemek, küçük bir üst simge referans işareti ekler.
// dipnotu/sonnotu eklediğimiz ana metin içinde.
// Her dipnot/sonnot ayrıca bir giriş oluşturur; bu giriş bir sembolden oluşur
// ana metindeki referans işaretiyle eşleşen.
// Belge oluşturucunun "InsertEndnote" metoduna geçirdiğimiz referans metni.
// Dipnot girişleri, varsayılan olarak, içeren her sayfanın alt kısmında görünür
// referans işaretlerini, ve sonnotlar belgenin sonunda görünür.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");

// Varsayılan olarak, her dipnot ve sonnot için referans işareti, onun indeksidir
// belgenin tüm dipnot/sonnotları arasında. Her belge ayrı sayımlar tutar
// dipnotlar ve sonnotlar için, her ikisi de 1'den başlar.
ASSERT_EQ(1, doc->get_FootnoteOptions()->get_StartNumber());
ASSERT_EQ(1, doc->get_EndnoteOptions()->get_StartNumber());

// "StartNumber" özelliğini kullanarak belgenin
// dipnot veya sonnot sayımını farklı bir sayıdan başlatmasını sağlayabiliriz.
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::Arabic);
doc->get_EndnoteOptions()->set_StartNumber(50);

doc->Save(get_ArtifactsDir() + u"InlineStory.StartNumber.docx");
```

## Ayrıca Bakınız

* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
