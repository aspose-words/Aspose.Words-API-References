---
title: "Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars yöntemi"
linktitle: "get_ShowRevisionBars"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars yöntemi. Revize edilmiş içeriği içeren satırların yakınında revizyon çubuklarının render edilip edilmeyeceğini belirtmenizi sağlar. Varsayılan değer C++'da true'dur."
type: docs
weight: 19000
url: /tr/cpp/aspose.words.layout/revisionoptions/get_showrevisionbars/
---
## RevisionOptions::get_ShowRevisionBars method


Revizyon çubuklarının revize içerik içeren satırların yakınında renderlenip renderlenmeyeceğini belirtmenizi sağlar. Varsayılan değer **true**.

```cpp
bool Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars() const
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

* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
