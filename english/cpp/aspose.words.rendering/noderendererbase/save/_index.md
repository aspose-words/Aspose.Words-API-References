---
title: Aspose::Words::Rendering::NodeRendererBase::Save method
linktitle: Save
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Rendering::NodeRendererBase::Save method. Renders the shape into an image and saves into a stream in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.rendering/noderendererbase/save/
---
## NodeRendererBase::Save(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method


Renders the shape into an image and saves into a stream.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::SharedPtr<System::IO::Stream> &stream, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | The stream where to save the image of the shape. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\> | Specifies the options that control how the shape is rendered and saved. Can be **null**. If this is **null**, the image will be saved in the PNG format. |

## Examples



Shows how to use a shape renderer to export shapes to files in the local file system. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Various shapes.docx");
ArrayPtr<SharedPtr<Shape>> shapes = doc->GetChildNodes(NodeType::Shape, true)->LINQ_OfType<SharedPtr<Shape>>()->LINQ_ToArray();

ASSERT_EQ(7, shapes->get_Length());

// There are 7 shapes in the document, including one group shape with 2 child shapes.
// We will render every shape to an image file in the local file system
// while ignoring the group shapes since they have no appearance.
// This will produce 6 image files.
for (const auto& shape : System::IterateOver(doc->GetChildNodes(NodeType::Shape, true)->LINQ_OfType<SharedPtr<Shape>>()))
{
    SharedPtr<ShapeRenderer> renderer = shape->GetShapeRenderer();
    auto options = MakeObject<ImageSaveOptions>(SaveFormat::Png);
    renderer->Save(ArtifactsDir + String::Format(u"Shape.RenderAllShapes.{0}.png", shape->get_Name()), options);
}
```

## See Also

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method


Renders the shape into an image and saves into a file.

```cpp
void Aspose::Words::Rendering::NodeRendererBase::Save(const System::String &fileName, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | The name for the image file. If a file with the specified name already exists, the existing file is overwritten. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\> | Specifies the options that control how the shape is rendered and saved. Can be **null**. |

## Examples



Shows how to render an Office [Math](../../../aspose.words.math/) object into an image file in the local file system. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Office math.docx");

auto math = System::DynamicCast<OfficeMath>(doc->GetChild(NodeType::OfficeMath, 0, true));

// Create an "ImageSaveOptions" object to pass to the node renderer's "Save" method to modify
// how it renders the OfficeMath node into an image.
auto saveOptions = MakeObject<ImageSaveOptions>(SaveFormat::Png);

// Set the "Scale" property to 5 to render the object to five times its original size.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(ArtifactsDir + u"Shape.RenderOfficeMath.png", saveOptions);
```

## See Also

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
## NodeRendererBase::Save(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Rendering::NodeRendererBase::Save(std::basic_ostream<CharType, Traits> &stream, System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> saveOptions)
```

## See Also

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [NodeRendererBase](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
