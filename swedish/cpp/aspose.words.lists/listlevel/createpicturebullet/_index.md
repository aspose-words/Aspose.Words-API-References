---
title: "Aspose::Words::Lists::ListLevel::CreatePictureBullet metod"
linktitle: "CreatePictureBullet"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::ListLevel::CreatePictureBullet metod. Skapar en bildpunktsform för den aktuella listnivån i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel::CreatePictureBullet method


Skapar bildpunktsform för den aktuella listnivån.

```cpp
void Aspose::Words::Lists::ListLevel::CreatePictureBullet()
```


## Exempel



Visar hur man anger en anpassad bildikon för listobjektets etiketter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Skapa en bildpunkt för den aktuella listnivån och ange en bild från ett lokalt filsystem
// som ikonen som punkterna för den här listnivån kommer att visa.
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

## Se även

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
