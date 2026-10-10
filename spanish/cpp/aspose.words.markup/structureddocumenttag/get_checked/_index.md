---
title: "Método Aspose::Words::Markup::StructuredDocumentTag::get_Checked"
linktitle: "get_Checked"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Markup::StructuredDocumentTag::get_Checked. Obtiene/Establece el estado actual del SDT de casilla de verificación. El valor predeterminado para esta propiedad es false en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.markup/structureddocumenttag/get_checked/
---
## StructuredDocumentTag::get_Checked method


Obtiene/establece el estado actual del Checkbox **SDT**. El valor predeterminado de esta propiedad es **false**.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_Checked()
```

## Observaciones


Acceder a esta propiedad solo funcionará para los tipos de SDT [Checkbox](../../sdttype/).

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
