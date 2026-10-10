---
title: "Aspose::Words::Rendering::ShapeRenderer class"
linktitle: "ShapeRenderer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Rendering::ShapeRenderer class. Fournit des méthodes pour rendre une Shape ou GroupShape individuelle en image raster ou vectorielle ou dans un objet **Graphics**. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.rendering/shaperenderer/
---
## ShapeRenderer class


Fournit des méthodes pour rendre une [Shape](../../aspose.words.drawing/shape/) ou [GroupShape](../../aspose.words.drawing/groupshape/) individuelle en image raster ou vectorielle ou dans un objet **Graphics**. Pour en savoir plus, consultez l'article de documentation [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class ShapeRenderer : public Aspose::Words::Rendering::NodeRendererBase
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BoundsInPoints](../noderendererbase/get_boundsinpoints/)() const | Obtient les limites réelles de la forme en points. |
| [get_OpaqueBoundsInPoints](../noderendererbase/get_opaqueboundsinpoints/)() | Obtient les limites opaques de la forme en points. |
| [get_SizeInPoints](../noderendererbase/get_sizeinpoints/)() | Obtient la taille réelle de la forme en points. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float) | Calcule les limites de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetBoundsInPixels](../noderendererbase/getboundsinpixels/)(float, float, float) | Calcule les limites de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float) | Calcule les limites opaques de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetOpaqueBoundsInPixels](../noderendererbase/getopaqueboundsinpixels/)(float, float, float) | Calcule les limites opaques de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float) | Calcule la taille de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetSizeInPixels](../noderendererbase/getsizeinpixels/)(float, float, float) | Calcule la taille de la forme en pixels pour un facteur de zoom et une résolution spécifiés. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NodeRendererBase](../noderendererbase/noderendererbase/)() |  |
| [RenderToScale](../noderendererbase/rendertoscale/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float) | Rend la forme dans un objet **Graphics** à une échelle spécifiée. |
| [RenderToSize](../noderendererbase/rendertosize/)(const System::SharedPtr\<System::Drawing::Graphics\>\&, float, float, float, float) | Rend la forme dans un objet **Graphics** à une taille spécifiée. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Rend la forme dans une image et l'enregistre dans un fichier. |
| [Save](../noderendererbase/save/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Rend la forme dans une image SVG et l'enregistre dans un fichier. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) | Rend la forme dans une image et l'enregistre dans un flux. |
| [Save](../noderendererbase/save/)(const System::SharedPtr\<System::IO::Stream\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) | Rend la forme dans une image SVG et l'enregistre dans un flux. |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>) |  |
| [Save](../noderendererbase/save/)(std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::Saving::SvgSaveOptions\>) |  |
| [ShapeRenderer](./shaperenderer/)(const System::SharedPtr\<Aspose::Words::Drawing::ShapeBase\>\&) | Initialise une nouvelle instance de cette classe. |
| static [Type](./type/)() |  |
## Voir aussi

* Class [NodeRendererBase](../noderendererbase/)
* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
