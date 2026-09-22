---
title: "Aspose::Words::Notes::FootnoteOptions::get_NumberStyle yöntemi"
linktitle: "get_NumberStyle"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::FootnoteOptions::get_NumberStyle yöntemi. C++'ta otomatik olarak numaralandırılan dipnotlar için sayı biçimini belirtir."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.notes/footnoteoptions/get_numberstyle/
---
## FootnoteOptions::get_NumberStyle method


Otomatik numaralandırılmış dipnotlar için sayı biçimini belirtir.

```cpp
Aspose::Words::NumberStyle Aspose::Words::Notes::FootnoteOptions::get_NumberStyle() override
```

## Açıklamalar


Bu özellik için tüm sayı stilleri uygulanabilir değildir. Uygulanabilir sayı stillerinin listesi için Microsoft Word'deki Ekle [Footnote](../../footnote/) veya Endnote iletişim kutusuna bakın. Uygulanamayan bir sayı stili seçerseniz, Microsoft Word varsayılan bir değere geri dönecektir.

## Örnekler



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

## Ayrıca Bakınız

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
