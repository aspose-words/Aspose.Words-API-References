---
title: "Aspose::Words::Drawing::ShapeBase::get_IsImage 方法"
linktitle: "get_IsImage"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_IsImage 方法。返回 true，如果此形状是图像形状（C++）。"
type: docs
weight: 29000
url: /zh/cpp/aspose.words.drawing/shapebase/get_isimage/
---
## ShapeBase::get_IsImage method


如果此形状是图像形状，则返回 **true**。

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsImage()
```


## 示例



展示如何使用基础 URI 从流中打开带有图像的 HTML 文档。
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // 在加载时传递基础文件夹的 URI
    // 以便能够找到 HTML 文档中任何带有相对 URI 的图像。
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // 验证文档的第一个形状包含有效的图像。
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
