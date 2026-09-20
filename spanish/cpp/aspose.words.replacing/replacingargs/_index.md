---
title: "clase Aspose::Words::Replacing::ReplacingArgs"
linktitle: "ReplacingArgs"
second_title: "Referencia de API de Aspose.Words para C++"
description: "clase Aspose::Words::Replacing::ReplacingArgs. Proporciona datos para una operación de reemplazo personalizada. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class


Proporciona datos para una operación de reemplazo personalizada. Para obtener más información, visite el artículo de documentación [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/).

```cpp
class ReplacingArgs : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_GroupIndex](./get_groupindex/)() const | Identifica, por índice, un grupo capturado en el [Match](./get_match/) que debe ser reemplazado con la cadena [Replacement](./get_replacement/). |
| [get_GroupName](./get_groupname/)() const | Identifica, por nombre, un grupo capturado en el [Match](./get_match/) que debe ser reemplazado con la cadena [Replacement](./get_replacement/). |
| [get_Match](./get_match/)() const | El **Match** resultante de una única coincidencia de expresión regular durante un **Replace**. |
| [get_MatchEndNode](./get_matchendnode/)() const | Obtiene el nodo que contiene el final de la coincidencia. |
| [get_MatchNode](./get_matchnode/)() const | Obtiene el nodo que contiene el inicio de la coincidencia. |
| [get_MatchOffset](./get_matchoffset/)() const | Obtiene la posición inicial basada en cero de la coincidencia desde el inicio del nodo que contiene el inicio de la coincidencia. |
| [get_Replacement](./get_replacement/)() const | Obtiene la cadena de reemplazo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GroupIndex](./set_groupindex/)(int32_t) | Método setter para [Aspose::Words::Replacing::ReplacingArgs::get_GroupIndex](./get_groupindex/). |
| [set_GroupName](./set_groupname/)(const System::String\&) | Método setter para [Aspose::Words::Replacing::ReplacingArgs::get_GroupName](./get_groupname/). |
| [set_Replacement](./set_replacement/)(const System::String\&) | Establece la cadena de reemplazo. |
| static [Type](./type/)() |  |

## Ver también

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
