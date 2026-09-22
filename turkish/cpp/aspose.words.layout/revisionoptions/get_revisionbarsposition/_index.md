---
title: "Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition metodu"
linktitle: "get_RevisionBarsPosition"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition metodu. Revizyon çubuklarının renderleme konumunu alır veya ayarlar. Varsayılan değer C++'da Dışarıdır."
type: docs
weight: 15000
url: /tr/cpp/aspose.words.layout/revisionoptions/get_revisionbarsposition/
---
## RevisionOptions::get_RevisionBarsPosition method


Revizyon çubuklarının renderleme konumunu alır veya ayarlar. Varsayılan değer [Dışarı](../../../aspose.words.drawing/horizontalalignment/).

```cpp
Aspose::Words::Drawing::HorizontalAlignment Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition() const
```


## Örnekler



Bir oluşturulmuş çıktı belgesinde revizyonların görünümünün nasıl değiştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir revizyon ekleyin, ardından tüm revizyonların rengini yeşile değiştirin.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Her revize edilmiş satırın solunda görünen çubuğu kaldırın.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Ayrıca Bakınız

* Enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
