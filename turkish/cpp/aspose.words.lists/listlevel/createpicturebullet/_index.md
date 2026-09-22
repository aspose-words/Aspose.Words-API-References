---
title: "Aspose::Words::Lists::ListLevel::CreatePictureBullet yöntemi"
linktitle: "CreatePictureBullet"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Lists::ListLevel::CreatePictureBullet yöntemi. C++ içinde mevcut liste seviyesi için resim madde işareti şekli oluşturur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel::CreatePictureBullet method


Geçerli liste seviyesi için resim madde işareti şekli oluşturur.

```cpp
void Aspose::Words::Lists::ListLevel::CreatePictureBullet()
```


## Örnekler



Liste öğesi etiketleri için özel bir resim simgesi ayarlamanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Mevcut liste seviyesi için bir resim madde işareti oluşturun ve yerel dosya sisteminden bir resim ayarlayın
// bu liste seviyesi için madde işaretlerinin göstereceği simge olarak.
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

## Ayrıca Bakınız

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
