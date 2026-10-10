---
title: "Aspose::Words::WatermarkLayout enum"
linktitle: "WatermarkLayout"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::WatermarkLayout enum. Define la disposición de la marca de agua relativa al centro de la marca de agua en C++."
type: docs
weight: 130000
url: /es/cpp/aspose.words/watermarklayout/
---
## WatermarkLayout enum


Define el diseño de la marca de agua relativo al centro de la marca de agua.

```cpp
enum class WatermarkLayout
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Horizontal | 0 | Disposición horizontal de la marca de agua. Corresponde a 0 grados de rotación. |
| Diagonal | 315 | Disposición diagonal de la marca de agua. Corresponde a 315 grados de rotación. |


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
