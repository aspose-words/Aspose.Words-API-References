---
title: "Enumeración Aspose::Words::Lists::ListTrailingCharacter"
linktitle: "ListTrailingCharacter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::Lists::ListTrailingCharacter. Especifica el carácter que separa la etiqueta de la lista del texto del párrafo en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.lists/listtrailingcharacter/
---
## ListTrailingCharacter enum


Especifica el carácter que separa la etiqueta de la lista del texto del párrafo.

```cpp
enum class ListTrailingCharacter
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Tabulador | 0 | Se coloca un carácter de tabulación entre la etiqueta de la lista y el texto del párrafo. |
| Espacio | 1 | Se coloca un carácter de espacio entre la etiqueta de la lista y el texto del párrafo. |
| Nada | 2 | No hay ningún carácter separador entre la etiqueta de la lista y el texto del párrafo. |

## Observaciones


Se usa como valor para la propiedad [TrailingCharacter](../listlevel/get_trailingcharacter/).

## Ejemplos



Muestra cómo aplicar formato de lista personalizado a los párrafos al usar [DocumentBuilder](../../aspose.words/documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría.
// Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
// Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Cree una lista a partir de una plantilla de Microsoft Word y personalice los dos primeros niveles de la lista.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Este valor NumberFormat creará símbolos de viñetas en forma de estrella.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Cree párrafos y aplique ambos niveles de lista de nuestro formato de lista personalizado a ellos.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## Ver también

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
