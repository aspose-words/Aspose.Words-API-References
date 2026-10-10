---
title: "Aspose::Words::Rendering::ShapeRenderer class"
linktitle: "ShapeRenderer"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Rendering::ShapeRenderer class. Tek bir Shape veya GroupShape'i raster veya vektör görüntüsüne ya da bir Graphics nesnesine render etmek için yöntemler sağlar. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class


Tek bir [Shape](../../aspose.words.drawing/shape/) veya [GroupShape](../../aspose.words.drawing/groupshape/) nesnesini raster veya vektör görüntüsüne ya da bir Graphics nesnesine render etmek için yöntemler sağlar. Daha fazla bilgi için [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) belge makalesini ziyaret edin.

```cpp
class ShapeRenderer : public Aspose::Words::Rendering::NodeRendererBase
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_BoundsInPoints](../noderendererbase/get_boundsinpoints/)() const | Şeklin gerçek sınırlarını puan cinsinden alır. |
| [get_OpaqueBoundsInPoints](../noderendererbase/get_opaqueboundsinpoints/)() | Şeklin opak sınırlarını puan cinsinden alır. |
| [get_SizeInPoints](../noderendererbase/get_sizeinpoints/)() | Şeklin gerçek boyutunu puan cinsinden alır. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin sınırlarını pikseller cinsinden hesaplar. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float, float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin sınırlarını pikseller cinsinden hesaplar. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin opak sınırlarını pikseller cinsinden hesaplar. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float, float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin opak sınırlarını pikseller cinsinden hesaplar. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin boyutunu pikseller cinsinden hesaplar. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float, float) | Belirtilen yakınlaştırma faktörü ve çözünürlük için şeklin boyutunu pikseller cinsinden hesaplar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](../noderendererbase/noderendererbase/)() |  |
| [RenderToScale](../noderendererbase/rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Şekli belirtilen ölçeğe **Graphics** nesnesine çizer. |
| [RenderToSize](../noderendererbase/rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Şekli belirtilen boyuta **Graphics** nesnesine çizer. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Şekli bir görüntüye render eder ve bir dosyaya kaydeder. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Şekli bir SVG görüntüsüne render eder ve bir dosyaya kaydeder. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Şekli bir görüntüye render eder ve bir akışa kaydeder. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Şekli bir SVG görüntüsüne render eder ve bir akışa kaydeder. |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| [ShapeRenderer](./shaperenderer/)(const System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\&) | Bu sınıfın yeni bir örneğini başlatır. |
| static [Type](./type/)() |  |
## Ayrıca Bakınız

* Class [NodeRendererBase](../noderendererbase/)
* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
