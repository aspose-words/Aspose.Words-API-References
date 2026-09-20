---
title: "Aspose::Words::TextWatermarkOptions clase"
linktitle: "TextWatermarkOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::TextWatermarkOptions. Contiene opciones que pueden especificarse al añadir una marca de agua con texto. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 72000
url: /es/cpp/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class


Contiene opciones que pueden especificarse al agregar una marca de agua con texto. Para obtener más información, visite el artículo de documentación [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class TextWatermarkOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Color](./get_color/)() const | Obtiene o establece el color de fuente. El valor predeterminado es **Silver**. |
| [get_FontFamily](./get_fontfamily/)() const | Obtiene o establece el nombre de la familia de fuentes. El valor predeterminado es "Calibri". |
| [get_FontSize](./get_fontsize/)() const | Obtiene o establece un tamaño de fuente. El valor predeterminado es 0 - automático. |
| [get_IsSemitrasparent](./get_issemitrasparent/)() const | Obtiene o establece un valor booleano que controla la opacidad de la marca de agua. El valor predeterminado es **true**. |
| [get_Layout](./get_layout/)() const | Obtiene o establece el diseño de la marca de agua. El valor predeterminado es [Diagonal](../watermarklayout/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Establecedor de [Aspose::Words::TextWatermarkOptions::get_Color](./get_color/). |
| [set_FontFamily](./set_fontfamily/)(const System::String\&) | Establecedor de [Aspose::Words::TextWatermarkOptions::get_FontFamily](./get_fontfamily/). |
| [set_FontSize](./set_fontsize/)(float) | Establecedor de [Aspose::Words::TextWatermarkOptions::get_FontSize](./get_fontsize/). |
| [set_IsSemitrasparent](./set_issemitrasparent/)(bool) | Establecedor de [Aspose::Words::TextWatermarkOptions::get_IsSemitrasparent](./get_issemitrasparent/). |
| [set_Layout](./set_layout/)(Aspose::Words::WatermarkLayout) | Establecedor de [Aspose::Words::TextWatermarkOptions::get_Layout](./get_layout/). |
| [TextWatermarkOptions](./textwatermarkoptions/)() |  |
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
