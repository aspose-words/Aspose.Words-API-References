---
title: "Aspose::Words::Lists::ListLevel::CreatePictureBullet 方法"
linktitle: "CreatePictureBullet"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListLevel::CreatePictureBullet 方法。为当前列表级别在 C++ 中创建图片项目符号形状。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel::CreatePictureBullet method


为当前列表级别创建图片项目符号形状。

```cpp
void Aspose::Words::Lists::ListLevel::CreatePictureBullet()
```


## 示例



展示如何为列表项标签设置自定义图像图标。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletCircle);

// 为当前列表级别创建图片项目符号，并从本地文件系统设置图像
// 作为此列表级别的项目符号将显示的图标。
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

## 另见

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
