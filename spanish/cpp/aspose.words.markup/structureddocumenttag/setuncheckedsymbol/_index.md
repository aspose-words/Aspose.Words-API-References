---
title: "Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol método"
linktitle: "SetUncheckedSymbol"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol método. Establece el símbolo utilizado para representar el estado sin marcar de un control de contenido de casilla de verificación en C++."
type: docs
weight: 59000
url: /es/cpp/aspose.words.markup/structureddocumenttag/setuncheckedsymbol/
---
## StructuredDocumentTag::SetUncheckedSymbol method


Establece el símbolo usado para representar el estado desmarcado de un control de contenido de casilla de verificación.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::SetUncheckedSymbol(int32_t characterCode, const System::String &fontName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| characterCode | int32_t | El código de carácter para el símbolo especificado. |
| fontName | const System::String\& | El nombre de la fuente que contiene el símbolo. |
## Observaciones


Acceder a este método solo funcionará para los tipos SDT [Checkbox](../../sdttype/).

Para todos los demás tipos de SDT se producirá una excepción.

## Ejemplos



Muestra cómo crear una etiqueta de documento estructurado en forma de casilla de verificación.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto sdtCheckBox = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
sdtCheckBox->set_Checked(true);

// Podemos establecer los símbolos utilizados para representar el estado marcado/desmarcado de un control de contenido de casilla de verificación.
sdtCheckBox->SetCheckedSymbol(0x00A9, u"Times New Roman");
sdtCheckBox->SetUncheckedSymbol(0x00AE, u"Times New Roman");

builder->InsertNode(sdtCheckBox);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CheckBox.docx");
```

## Ver también

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
