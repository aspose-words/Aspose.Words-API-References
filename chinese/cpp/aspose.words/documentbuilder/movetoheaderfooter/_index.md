---
title: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter method"
linktitle: "MoveToHeaderFooter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::MoveToHeaderFooter 方法。将光标移动到 C++ 中当前节的页眉或页脚的开头。"
type: docs
weight: 57000
url: /zh/cpp/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder::MoveToHeaderFooter method


将光标移动到当前节的页眉或页脚的开头。

```cpp
void Aspose::Words::DocumentBuilder::MoveToHeaderFooter(Aspose::Words::HeaderFooterType headerFooterType)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| headerFooterType | Aspose::Words::HeaderFooterType | 指定要移动到的页眉或页脚。 |
## 备注


将光标移动到页眉或页脚后，您可以使用其余的 [DocumentBuilder](../) 方法来修改页眉或页脚的内容。

如果您想为首页创建不同的页眉和页脚，需要设置 [DifferentFirstPageHeaderFooter](../../pagesetup/get_differentfirstpageheaderfooter/)。

如果您想为奇数页和偶数页创建不同的页眉和页脚，需要设置 [OddAndEvenPagesHeaderFooter](../../pagesetup/get_oddandevenpagesheaderfooter/)。

使用 [MoveToSection()](../movetosection/) 可将光标从页眉移出到正文。

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

* Enum [HeaderFooterType](../../headerfootertype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
