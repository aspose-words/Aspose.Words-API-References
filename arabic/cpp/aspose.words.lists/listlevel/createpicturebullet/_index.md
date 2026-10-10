---
title: "طريقة Aspose::Words::Lists::ListLevel::CreatePictureBullet"
linktitle: "CreatePictureBullet"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Lists::ListLevel::CreatePictureBullet. تُنشئ شكل نقطة صورة للمستوى الحالي من القائمة في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel::CreatePictureBullet method


ينشئ شكل تعداد صورة للمستوى الحالي من القائمة.

```cpp
void Aspose::Words::Lists::ListLevel::CreatePictureBullet()
```


## أمثلة



يعرض كيفية تعيين أيقونة صورة مخصصة لتسميات عناصر القائمة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletCircle);

// إنشاء نقطة صورة للمستوى الحالي من القائمة، وتعيين صورة من نظام ملفات محلي
// كالأيقونة التي ستعرضها النقاط لهذا المستوى من القائمة.
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

## انظر أيضًا

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
