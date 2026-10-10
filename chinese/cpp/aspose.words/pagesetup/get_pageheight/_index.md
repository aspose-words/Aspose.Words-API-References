---
title: "Aspose::Words::PageSetup::get_PageHeight 方法"
linktitle: "get_PageHeight"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_PageHeight 方法。返回或设置页面的高度（单位为点）（C++）。"
type: docs
weight: 33000
url: /zh/cpp/aspose.words/pagesetup/get_pageheight/
---
## PageSetup::get_PageHeight method


返回或设置页面的高度（单位为点）。

```cpp
double Aspose::Words::PageSetup::get_PageHeight()
```


## 示例



展示如何插入图像并将其用作水印。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 将图像插入页眉，以便在每页上可见。
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// 将图像放置在页面中心。
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```

## 另见

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
