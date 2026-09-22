---
title: "Aspose::Words::Layout::RevisionOptions::get_CommentColor metodu"
linktitle: "get_CommentColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::RevisionOptions::get_CommentColor metodu. Yorumlar için kullanılacak rengi belirtmenizi sağlar. Varsayılan değer C++'da Kırmızıdır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.layout/revisionoptions/get_commentcolor/
---
## RevisionOptions::get_CommentColor method


Yorumlar için kullanılacak rengi belirtmenizi sağlar. Varsayılan değer [Kırmızı](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_CommentColor() const
```


## Örnekler



Revizyonların görünümünü nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Revizyonların görünümünü kontrol eden RevisionOptions nesnesini alın.
System::SharedPtr<Aspose::Words::Layout::RevisionOptions> revisionOptions = doc->get_LayoutOptions()->get_RevisionOptions();

// Ekleme revizyonlarını yeşil ve italik olarak render edin.
revisionOptions->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::Green);
revisionOptions->set_InsertedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Italic);

// Silme revizyonlarını kırmızı ve kalın olarak render edin.
revisionOptions->set_DeletedTextColor(Aspose::Words::Layout::RevisionColor::Red);
revisionOptions->set_DeletedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// Aynı metin bir hareket revizyonunda iki kez görünecek:
// bir kez çıkış noktasında ve bir kez varış noktasında.
// Taşınan-önce revizyonundaki metni çift üstü çizgiyle sarı olarak render edin
// ve taşınan-sonra revizyonunda çift altı çizili mavi olarak.
revisionOptions->set_MovedFromTextColor(Aspose::Words::Layout::RevisionColor::Yellow);
revisionOptions->set_MovedFromTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleStrikeThrough);
revisionOptions->set_MovedToTextColor(Aspose::Words::Layout::RevisionColor::ClassicBlue);
revisionOptions->set_MovedToTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleUnderline);

// Biçim revizyonlarını koyu kırmızı ve kalın olarak render edin.
revisionOptions->set_RevisedPropertiesColor(Aspose::Words::Layout::RevisionColor::DarkRed);
revisionOptions->set_RevisedPropertiesEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// Sayfanın sol tarafına, revizyonlardan etkilenen satırların yanına kalın koyu mavi bir çubuk yerleştirin.
revisionOptions->set_RevisionBarsColor(Aspose::Words::Layout::RevisionColor::DarkBlue);
revisionOptions->set_RevisionBarsWidth(15.0f);

// Revizyon işaretlerini ve orijinal metni göster.
revisionOptions->set_ShowOriginalRevision(true);
revisionOptions->set_ShowRevisionMarks(true);

// Hareket, silme, biçimlendirme revizyonlarını ve yorumları yeşil balonlarda gösterilecek şekilde alın
// sayfanın sağ tarafında.
revisionOptions->set_ShowInBalloons(Aspose::Words::Layout::ShowInBalloons::Format);
revisionOptions->set_CommentColor(Aspose::Words::Layout::RevisionColor::BrightGreen);

// Bu özellikler yalnızca .pdf veya .jpg gibi formatlar için geçerlidir.
doc->Save(get_ArtifactsDir() + u"Revision.RevisionOptions.pdf");
```

## Ayrıca Bakınız

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
