---
title: "Aspose::Words::Watermark clase"
linktitle: "Marca de agua"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Watermark clase. Representa una clase para trabajar con la marca de agua del documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 76000
url: /es/cpp/aspose.words/watermark/
---
## Watermark class


Representa una clase para trabajar con la marca de agua del documento. Para obtener más información, visite el artículo de documentación [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class Watermark : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Type](./get_type/)() | Obtiene el tipo de marca de agua. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Elimina la marca de agua. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Agrega una marca de agua de imagen al documento. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Agrega una marca de agua de imagen al documento. |
| [SetImage](./setimage/)(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Agrega una marca de agua de imagen al documento. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Agrega una marca de agua de imagen al documento. |
| [SetText](./settext/)(const System::String\&) | Agrega una marca de agua de texto al documento. |
| [SetText](./settext/)(const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Agrega una marca de agua de texto al documento. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo crear una marca de agua de texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Añade una marca de agua de texto simple.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// Si deseamos editar el formato del texto usándolo como marca de agua,
// podemos hacerlo pasando un objeto TextWatermarkOptions al crear la marca de agua.
auto textWatermarkOptions = System::MakeObject<Aspose::Words::TextWatermarkOptions>();
textWatermarkOptions->set_FontFamily(u"Arial");
textWatermarkOptions->set_FontSize(36.0f);
textWatermarkOptions->set_Color(System::Drawing::Color::get_Black());
textWatermarkOptions->set_Layout(Aspose::Words::WatermarkLayout::Diagonal);
textWatermarkOptions->set_IsSemitrasparent(false);

doc->get_Watermark()->SetText(u"Aspose Watermark", textWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.TextWatermark.docx");

// Podemos eliminar una marca de agua de un documento como este.
if (doc->get_Watermark()->get_Type() == Aspose::Words::WatermarkType::Text)
{
    doc->get_Watermark()->Remove();
}
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
