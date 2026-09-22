---
title: "Aspose::Words::Document::get_FootnoteOptions yöntemi"
linktitle: "get_FootnoteOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_FootnoteOptions yöntemi. Bu belgede dipnotların numaralandırmasını ve konumlandırmasını kontrol eden seçenekler sağlar (C++)."
type: docs
weight: 26000
url: /tr/cpp/aspose.words/document/get_footnoteoptions/
---
## Document::get_FootnoteOptions method


Bu belgede dipnotların numaralandırmasını ve konumlandırmasını kontrol eden seçenekler sağlar.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> Aspose::Words::Document::get_FootnoteOptions()
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


Dipnot/sonnot referans işaretlerinin sayı stilini nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Dipnotlar ve sonnotlar, metne bir referans veya yan yorum eklemenin bir yoludur.
// ana metin akışına müdahale etmeyen.
// Bir dipnot/sonnot eklemek, küçük bir üst simge referans işareti ekler.
// dipnotu/sonnotu eklediğimiz ana metin içinde.
// Her dipnot/sonnot ayrıca bir giriş oluşturur; bu giriş referansla eşleşen bir simgeden oluşur.
// ana metindeki simge. Belge oluşturucunun "InsertEndnote" metoduna geçtiğimiz referans metni.
// Dipnot girişleri, varsayılan olarak, içeren her sayfanın alt kısmında görünür
// referans işaretlerini, ve sonnotlar belgenin sonunda görünür.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.", u"Custom footnote reference mark");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.", u"Custom endnote reference mark");

// Varsayılan olarak, her dipnot ve sonnot için referans işareti, onun indeksidir
// belgenin tüm dipnot/sonnotları arasında. Her belge ayrı sayımlar tutar
// dipnotlar ve sonnotlar için. Varsayılan olarak, dipnotlar sayılarını Arap rakamlarıyla gösterir,
// ve sonnotlar sayılarını küçük harfli Roma rakamlarıyla gösterir.
ASSERT_EQ(Aspose::Words::NumberStyle::Arabic, doc->get_FootnoteOptions()->get_NumberStyle());
ASSERT_EQ(Aspose::Words::NumberStyle::LowercaseRoman, doc->get_EndnoteOptions()->get_NumberStyle());

// "NumberStyle" özelliğini kullanarak dipnot ve sonnotlara özel numaralandırma stilleri uygulayabiliriz.
// Bu, özel referans işaretlerine sahip dipnot/sonnotları etkilemez.
doc->get_FootnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);

doc->Save(get_ArtifactsDir() + u"InlineStory.RefMarkNumberStyle.docx");
```


Belirli yerlerde dipnot/sonnot numaralandırmasının nasıl yeniden başlatılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Dipnotlar ve sonnotlar, metne bir referans veya yan yorum eklemenin bir yoludur.
// ana metin akışına müdahale etmeyen.
// Bir dipnot/sonnot eklemek, küçük bir üst simge referans işareti ekler.
// dipnotu/sonnotu eklediğimiz ana metin içinde.
// Her dipnot/sonnot ayrıca bir giriş oluşturur; bu giriş referansla eşleşen bir simgeden oluşur.
// ana metindeki simge. Belge oluşturucunun "InsertEndnote" metoduna geçtiğimiz referans metni.
// Dipnot girişleri, varsayılan olarak, içeren her sayfanın alt kısmında görünür
// referans işaretlerini, ve sonnotlar belgenin sonunda görünür.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 4.");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 4.");

// Varsayılan olarak, her dipnot ve sonnot için referans işareti, onun indeksidir
// belgenin tüm dipnot/sonnotları arasında. Her belge ayrı sayımlar tutar
// dipnotlar ve sonnotlar için ve bu sayımları hiçbir noktada yeniden başlatmaz.
ASSERT_EQ(doc->get_FootnoteOptions()->get_RestartRule(), Aspose::Words::Notes::FootnoteNumberingRule::Default);
ASSERT_EQ(Aspose::Words::Notes::FootnoteNumberingRule::Default, Aspose::Words::Notes::FootnoteNumberingRule::Continuous);

// "RestartRule" özelliğini kullanarak belgenin yeniden başlatmasını sağlayabiliriz.
// dipnot/sonnot sayımlarını yeni bir sayfada veya bölümde.
doc->get_FootnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
doc->get_EndnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartSection);

doc->Save(get_ArtifactsDir() + u"InlineStory.NumberingRule.docx");
```


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

* Class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
