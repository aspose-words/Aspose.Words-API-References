---
title: "Aspose::Words::Lists::ListLevel::CreatePictureBullet método"
linktitle: "CreatePictureBullet"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Lists::ListLevel::CreatePictureBullet método. Crea una forma de viñeta de imagen para el nivel de lista actual en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel::CreatePictureBullet method


Crea una forma de viñeta de imagen para el nivel de lista actual.

```cpp
void Aspose::Words::Lists::ListLevel::CreatePictureBullet()
```


## Ejemplos



Muestra cómo establecer un ícono de imagen personalizado para las etiquetas de los elementos de lista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Crea una viñeta de imagen para el nivel de lista actual y establece una imagen desde el sistema de archivos local
// como el ícono que mostrarán las viñetas de este nivel de lista.
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

## Ver también

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
