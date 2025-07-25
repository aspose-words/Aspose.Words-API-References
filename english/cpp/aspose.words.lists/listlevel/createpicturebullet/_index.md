---
title: Aspose::Words::Lists::ListLevel::CreatePictureBullet method
linktitle: CreatePictureBullet
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::ListLevel::CreatePictureBullet method. Creates picture bullet shape for the current list level in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel::CreatePictureBullet method


Creates picture bullet shape for the current list level.

```cpp
void Aspose::Words::Lists::ListLevel::CreatePictureBullet()
```


## Examples



Shows how to set a custom image icon for list item labels. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletCircle);

// Create a picture bullet for the current list level, and set an image from a local file system
// as the icon that the bullets for this list level will display.
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

## See Also

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
