---
title: "Aspose::Words::Lists::ListLevel::DeletePictureBullet Methode"
linktitle: "DeletePictureBullet"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListLevel::DeletePictureBullet Methode. Löscht das Bildaufzählungszeichen für die aktuelle Listenebene in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel::DeletePictureBullet method


Löscht das Bildaufzählungszeichen für die aktuelle Listenebene.

```cpp
void Aspose::Words::Lists::ListLevel::DeletePictureBullet()
```


## Beispiele



Zeigt, wie man ein benutzerdefiniertes Bildsymbol für Listenelement‑Beschriftungen festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Erstelle ein Bildaufzählungszeichen für die aktuelle Listenebene und setze ein Bild aus einem lokalen Dateisystem.
// als das Symbol, das die Aufzählungszeichen für diese Listenebene anzeigen.
list->get_ListLevels()->idx_get(0)->CreatePictureBullet();
list->get_ListLevels()->idx_get(0)->get_ImageData()->SetImage(get_ImageDir() + u"Logo icon.ico");

ASSERT_TRUE(list->get_ListLevels()->idx_get(0)->get_ImageData()->get_HasImage());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

doc->Save(get_ArtifactsDir() + u"Lists.CreatePictureBullet.docx");

list->get_ListLevels()->idx_get(0)->DeletePictureBullet();

ASSERT_TRUE(System::TestTools::IsNull(list->get_ListLevels()->idx_get(0)->get_ImageData()));
```

## Siehe auch

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
