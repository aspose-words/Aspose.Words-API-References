---
title: "Aspose::Words::Drawing::ImageType enum"
linktitle: "ImageType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ImageType enum。指定在 C++ 中 Microsoft Word 文档中图像的类型（格式）。"
type: docs
weight: 28000
url: /zh/cpp/aspose.words.drawing/imagetype/
---
## ImageType enum


指定 Microsoft Word 文档中图像的类型（格式）。

```cpp
enum class ImageType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| NoImage | 0 | 没有图像数据。 |
| 未知 | 1 | 未知的图像类型或无法直接存储在 Microsoft Word 文档中的图像类型。 |
| Emf | 2 | Windows 增强型图元文件。 |
| Wmf | 3 | Windows 图元文件。 |
| Pict | 4 | Macintosh PICT。文档中将保留已有图像，但不支持向文档中插入新的 PICT 图像。 |
| Jpeg | 5 | JPEG JFIF。 |
| Png | 6 | 可移植网络图形。 |
| Bmp | 7 | Windows 位图。 |
| Eps | 8 | 封装的 PostScript。 |
| WebP | 9 | WebP。 |
| Gif | 10 | GIF。 |


## 示例



展示如何向形状添加图像并检查其类型。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> imgShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, imgShape->get_ImageData()->get_ImageType());
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
