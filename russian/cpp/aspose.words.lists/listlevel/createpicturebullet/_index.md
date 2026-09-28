---
title: "Aspose::Words::Lists::ListLevel::CreatePictureBullet метод"
linktitle: "CreatePictureBullet"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Lists::ListLevel::CreatePictureBullet метод. Создаёт форму графического маркера для текущего уровня списка в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel::CreatePictureBullet method


Создаёт форму графического маркера для текущего уровня списка.

```cpp
void Aspose::Words::Lists::ListLevel::CreatePictureBullet()
```


## Примеры



Показывает, как установить пользовательский значок изображения для меток элементов списка.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Создайте графический маркер для текущего уровня списка и задайте изображение из локальной файловой системы.
// в качестве значка, который будут отображать маркеры для этого уровня списка.
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

## См. также

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
