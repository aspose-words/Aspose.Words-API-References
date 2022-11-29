---
title: DeletePictureBullet
second_title: Aspose.Words for C++ API Reference
description: Deletes picture bullet for the current list level.
type: docs
weight: 14
url: /cpp/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel::DeletePictureBullet method


Deletes picture bullet for the current list level.

```cpp
void Aspose::Words::Lists::ListLevel::DeletePictureBullet()
```


## Examples



Shows how to set a custom image icon for list item labels. 
```cpp
auto doc = MakeObject<Document>();

SharedPtr<List> list = doc->get_Lists()->Add(ListTemplate::BulletCircle);

// Create a picture bullet for the current list level, and set an image from a local file system
// as the icon that the bullets for this list level will display.
list->get_ListLevels()->idx_get(0)->CreatePictureBullet();
list->get_ListLevels()->idx_get(0)->get_ImageData()->SetImage(ImageDir + u"Logo icon.ico");

ASSERT_TRUE(list->get_ListLevels()->idx_get(0)->get_ImageData()->get_HasImage());

auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

doc->Save(ArtifactsDir + u"Lists.CreatePictureBullet.docx");

list->get_ListLevels()->idx_get(0)->DeletePictureBullet();

ASSERT_TRUE(list->get_ListLevels()->idx_get(0)->get_ImageData() == nullptr);
```

## See Also

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words](../../../)
