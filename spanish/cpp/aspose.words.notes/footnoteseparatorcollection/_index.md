---
title: "Aspose::Words::Notes::FootnoteSeparatorCollection class"
linktitle: "FootnoteSeparatorCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Notes::FootnoteSeparatorCollection class. Proporciona acceso tipado a los nodos FootnoteSeparator de un documento en C++."
type: docs
weight: 3667
url: /es/cpp/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class


Proporciona acceso tipado a los nodos [FootnoteSeparator](../footnoteseparator/) de un documento.

```cpp
class FootnoteSeparatorCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [FootnoteSeparatorCollection](./footnoteseparatorcollection/)() |  |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::Notes::FootnoteSeparatorType) | Recupera un [FootnoteSeparator](../footnoteseparator/) del tipo especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo administrar el formato del separador de notas al pie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Alinear el separador de notas al pie.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## Ver también

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
