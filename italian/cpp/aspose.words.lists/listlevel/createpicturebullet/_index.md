---
title: "Aspose::Words::Lists::ListLevel::CreatePictureBullet metodo"
linktitle: "CreatePictureBullet"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Lists::ListLevel::CreatePictureBullet metodo. Crea una forma di pallino immagine per il livello di elenco corrente in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel::CreatePictureBullet method


Crea una forma di pallino immagine per il livello di elenco corrente.

```cpp
void Aspose::Words::Lists::ListLevel::CreatePictureBullet()
```


## Esempi



Mostra come impostare un'icona immagine personalizzata per le etichette degli elementi dell'elenco.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Crea un punto elenco immagine per il livello di elenco corrente e imposta un'immagine dal file system locale
// come l'icona che i punti elenco per questo livello di elenco visualizzeranno.
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

## Vedi anche

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
