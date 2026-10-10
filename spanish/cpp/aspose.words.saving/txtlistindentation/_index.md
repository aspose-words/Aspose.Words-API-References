---
title: "Clase Aspose::Words::Saving::TxtListIndentation"
linktitle: "TxtListIndentation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Saving::TxtListIndentation. Especifica cómo se sangran los niveles de lista cuando el documento se exporta al formato Texto. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 32000
url: /es/cpp/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class


Especifica cómo se sangran los niveles de lista cuando el documento se exporta al formato [Texto](../../aspose.words/saveformat/). Para obtener más información, visite el artículo de documentación [Guardar un documento](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class TxtListIndentation : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Character](./get_character/)() const | Obtiene o establece qué carácter usar para sangrar los niveles de lista. El valor predeterminado es '\\0', lo que significa que no hay sangría. |
| [get_Count](./get_count/)() const | Obtiene o establece cuántos [Character](./get_character/) usar como sangría por cada nivel de lista. El valor predeterminado es 0, lo que significa que no hay sangría. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Character](./set_character/)(char16_t) | Método set para [Aspose::Words::Saving::TxtListIndentation::get_Character](./get_character/). |
| [set_Count](./set_count/)(int32_t) | Método set para [Aspose::Words::Saving::TxtListIndentation::get_Count](./get_count/). |
| [TxtListIndentation](./txtlistindentation/)() |  |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo configurar la sangría de listas al guardar un documento en texto plano.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Cree una lista con tres niveles de sangría.
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 3");

// Cree un objeto "TxtSaveOptions", que podemos pasar al método "Save" del documento
// para modificar cómo guardamos el documento en texto plano.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Establezca la propiedad "Character" para asignar un carácter a usar
// para el relleno que simula la sangría de listas en texto plano.
txtSaveOptions->get_ListIndentation()->set_Character(u' ');

// Establezca la propiedad "Count" para especificar el número de veces
// para colocar el carácter de relleno en cada nivel de sangría de lista.
txtSaveOptions->get_ListIndentation()->set_Count(3);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt");
System::String newLine = System::Environment::get_NewLine();

ASSERT_EQ(System::String::Format(u"1. Item 1{0}", newLine) + System::String::Format(u"   a. Item 2{0}", newLine) + System::String::Format(u"      i. Item 3{0}", newLine), docText);
```

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
