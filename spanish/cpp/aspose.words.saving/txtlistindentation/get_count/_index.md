---
title: "Método Aspose::Words::Saving::TxtListIndentation::get_Count"
linktitle: "get_Count"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::TxtListIndentation::get_Count. Obtiene o establece cuántos caracteres usar como sangría por cada nivel de lista. El valor predeterminado es 0, lo que significa sin sangría en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.saving/txtlistindentation/get_count/
---
## TxtListIndentation::get_Count method


Obtiene o establece cuántos [Character](../get_character/) usar como sangría por cada nivel de lista. El valor predeterminado es 0, lo que significa sin sangría.

```cpp
int32_t Aspose::Words::Saving::TxtListIndentation::get_Count() const
```


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

* Class [TxtListIndentation](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
