---
title: "Aspose::Words::Layout::LayoutOptions::get_RevisionOptions metodu"
linktitle: "get_RevisionOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::LayoutOptions::get_RevisionOptions metodu. C++'ta revizyon seçeneklerini alır."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.layout/layoutoptions/get_revisionoptions/
---
## LayoutOptions::get_RevisionOptions method


Revizyon seçeneklerini alır.

```cpp
System::SharedPtr<Aspose::Words::Layout::RevisionOptions> Aspose::Words::Layout::LayoutOptions::get_RevisionOptions() const
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

* Class [RevisionOptions](../../revisionoptions/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
