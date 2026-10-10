---
title: "Aspose::Words::Drawing::TextureAlignment 枚举"
linktitle: "TextureAlignment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::TextureAlignment 枚举。指定纹理填充平铺的对齐方式（C++）。"
type: docs
weight: 42000
url: /zh/cpp/aspose.words.drawing/texturealignment/
---
## TextureAlignment enum


指定纹理填充平铺的对齐方式。

```cpp
enum class TextureAlignment
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| TopLeft | 0 | 左上纹理对齐。 |
| 顶部 | 1 | 顶部纹理对齐。 |
| TopRight | 2 | 右上纹理对齐。 |
| 左 | 3 | 左侧纹理对齐。 |
| 居中 | 4 | 居中纹理对齐。 |
| 右 | 5 | 右侧纹理对齐。 |
| BottomLeft | 6 | 左下纹理对齐。 |
| 底部 | 7 | 底部纹理对齐。 |
| BottomRight | 8 | 右下角纹理对齐。 |
| None | 9 | 无纹理对齐。 |


## 示例



展示如何在形状内部填充和平铺纹理。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);

// 将纹理对齐应用于形状填充。
shape->get_Fill()->PresetTextured(Aspose::Words::Drawing::PresetTexture::Canvas);
shape->get_Fill()->set_TextureAlignment(Aspose::Words::Drawing::TextureAlignment::TopRight);

// 如果想获取 "TextureAlignment"，请使用合规选项通过 DML 定义形状。
// 文档保存后属性。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.TextureFill.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.TextureFill.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(Aspose::Words::Drawing::TextureAlignment::TopRight, shape->get_Fill()->get_TextureAlignment());
ASSERT_EQ(Aspose::Words::Drawing::PresetTexture::Canvas, shape->get_Fill()->get_PresetTexture());
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
