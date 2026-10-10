---
title: "Aspose::Words::ParagraphFormat::get_SnapToGrid yöntemi"
linktitle: "get_SnapToGrid"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_SnapToGrid yöntemi. Mevcut paragrafın, paragraftaki içeriği düzenlerken sayfa başına belge ızgara satırlarını kullanıp kullanmayacağını C++'ta belirtir."
type: docs
weight: 30000
url: /tr/cpp/aspose.words/paragraphformat/get_snaptogrid/
---
## ParagraphFormat::get_SnapToGrid method


Geçerli paragrafın, paragraftaki içeriği düzenlerken sayfa başına belge ızgara çizgileri ayarlarını kullanıp kullanmayacağını belirtir.

```cpp
bool Aspose::Words::ParagraphFormat::get_SnapToGrid()
```


## Örnekler



Her sayfada bulunabilecek satır sayısı için bir sınır nasıl belirlenir gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Kaydırmayı etkinleştirin ve ardından bu bölümde sayfa başına satır sayısını ayarlamak için kullanın.
// Yeterince büyük bir yazı tipi boyutu, karakterlerin üst üste gelmesini önlemek için bazı satırları bir sonraki sayfaya itecektir.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::LineGrid);
builder->get_PageSetup()->set_LinesPerPage(15);

builder->get_ParagraphFormat()->set_SnapToGrid(true);

for (int32_t i = 0; i < 30; i++)
{
    builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
}

doc->Save(get_ArtifactsDir() + u"PageSetup.LinesPerPage.docx");
```

## Ayrıca Bakınız

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
