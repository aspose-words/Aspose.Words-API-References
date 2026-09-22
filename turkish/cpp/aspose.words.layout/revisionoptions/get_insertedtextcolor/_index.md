---
title: "Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor yöntemi"
linktitle: "get_InsertedTextColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor yöntemi. Eklenen içerik için kullanılacak rengi belirtmeye izin verir Insertion. Varsayılan değer C++'da ByAuthor'dir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.layout/revisionoptions/get_insertedtextcolor/
---
## RevisionOptions::get_InsertedTextColor method


Eklenen içerik için kullanılacak rengi belirtmeye izin verir [Insertion](../../../aspose.words/revisiontype/). Varsayılan değer [ByAuthor](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor()
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

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
