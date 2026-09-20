---
title: "Aspose::Words::TextWatermarkOptions::get_Layout método"
linktitle: "get_Layout"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TextWatermarkOptions::get_Layout método. Obtiene o establece el diseño de la marca de agua. El valor predeterminado es Diagonal en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/textwatermarkoptions/get_layout/
---
## TextWatermarkOptions::get_Layout method


Obtiene o establece el diseño de la marca de agua. El valor predeterminado es [Diagonal](../../watermarklayout/).

```cpp
Aspose::Words::WatermarkLayout Aspose::Words::TextWatermarkOptions::get_Layout() const
```


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

* Enum [WatermarkLayout](../../watermarklayout/)
* Class [TextWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
