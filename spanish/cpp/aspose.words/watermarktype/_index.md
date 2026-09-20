---
title: "Aspose::Words::WatermarkType enumeración"
linktitle: "WatermarkType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::WatermarkType enumeración. Especifica el tipo de marca de agua en C++."
type: docs
weight: 131000
url: /es/cpp/aspose.words/watermarktype/
---
## WatermarkType enum


Especifica el tipo de marca de agua.

```cpp
enum class WatermarkType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Text | 0 | Indica que el texto se usará como marca de agua. Esa marca de agua corresponde a un objeto WordArt. |
| Image | 1 | Indica que la imagen se usará como marca de agua. Esa marca de agua corresponde a una forma con imagen. |
| None | 2 | Indica que la marca de agua no está establecida. |


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
