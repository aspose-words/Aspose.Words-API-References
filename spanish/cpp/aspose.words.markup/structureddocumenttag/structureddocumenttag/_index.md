---
title: "Constructor Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag"
linktitle: "StructuredDocumentTag"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag. Inicializa una nueva instancia de la clase de etiqueta de documento estructurado en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag::StructuredDocumentTag constructor


Inicializa una nueva instancia de la clase **Structured document tag**.

```cpp
Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Markup::SdtType type, Aspose::Words::Markup::MarkupLevel level)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | El documento propietario. |
| tipo | Aspose::Words::Markup::SdtType | Tipo de nodo SDT. |
| nivel | Aspose::Words::Markup::MarkupLevel | Nivel del nodo SDT dentro del documento. |
## Observaciones


Los siguientes tipos de SDT pueden crearse:

* [Checkbox](../../sdttype/)
* [DropDownList](../../sdttype/)
* [ComboBox](../../sdttype/)
* [Date](../../sdttype/)
* [BuildingBlockGallery](../../sdttype/)
* [Group](../../sdttype/)
* [Picture](../../sdttype/)
* [RichText](../../sdttype/)
* [PlainText](../../sdttype/)



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

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [SdtType](../../sdttype/)
* Enum [MarkupLevel](../../markuplevel/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
