---
title: "Aspose::Words::Notes::FootnoteNumberingRule enum"
linktitle: "FootnoteNumberingRule"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::FootnoteNumberingRule enum. C++ içinde otomatik dipnot veya sonnot numaralandırmasının ne zaman yeniden başlayacağını belirler."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.notes/footnotenumberingrule/
---
## FootnoteNumberingRule enum


Otomatik dipnot veya sonnot numaralandırmasının ne zaman yeniden başlayacağını belirler.

```cpp
enum class FootnoteNumberingRule
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Continuous | 0 | Belge boyunca numaralandırma sürekli olur. |
| RestartSection | 1 | Numaralandırma her bölümde yeniden başlar. |
| RestartPage | 2 | Numaralandırma her sayfada yeniden başlar. Yalnızca dipnotlar için geçerlidir. |
| Default | n/a | Eşittir [Continuous](./). |


## Örnekler



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

## Ayrıca Bakınız

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
