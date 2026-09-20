---
title: "Aspose::Words::Lists::ListLevel::get_NumberFormat método"
linktitle: "get_NumberFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Lists::ListLevel::get_NumberFormat método. Devuelve o establece el formato numérico para el nivel de lista en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.lists/listlevel/get_numberformat/
---
## ListLevel::get_NumberFormat method


Devuelve o establece el formato de número para el nivel de lista.

```cpp
System::String Aspose::Words::Lists::ListLevel::get_NumberFormat() const
```

## Observaciones


Entre los caracteres de texto normales, la cadena puede contener caracteres de marcador de posición \x0000 a \x0008 que representan los números de los niveles de lista correspondientes.

Por ejemplo, la cadena "\x0000.\x0001)" generará una etiqueta de lista que se ve algo así como "1.5)". El número "1" es el número actual del primer nivel de lista, el número "5" es el número actual del segundo nivel de lista.

Null no está permitido, pero una cadena vacía que signifique sin número es válida.

## Ejemplos



Muestra cómo aplicar formato de lista personalizado a los párrafos al usar [DocumentBuilder](../../../aspose.words/documentbuilder/).
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


Muestra formas avanzadas de personalizar las etiquetas de lista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría.
// Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
// Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

// Las etiquetas de nivel 1 se formatearán según el estilo de párrafo "Heading 1" y tendrán un prefijo.
// Estas se verán como "Appendix A", "Appendix B"...
list->get_ListLevels()->idx_get(0)->set_NumberFormat(u"Appendix \x0000");
list->get_ListLevels()->idx_get(0)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);
list->get_ListLevels()->idx_get(0)->set_LinkedStyle(doc->get_Styles()->idx_get(u"Heading 1"));

// Las etiquetas de nivel 2 mostrarán los números actuales del primer y segundo nivel de lista y tendrán ceros iniciales.
// Si el primer nivel de lista está en 1, entonces las etiquetas de lista de estos se verán como "Section (1.01)", "Section (1.02)"...
list->get_ListLevels()->idx_get(1)->set_NumberFormat(u"Section (\x0000" u".\x0001" u")");
list->get_ListLevels()->idx_get(1)->set_NumberStyle(Aspose::Words::NumberStyle::LeadingZero);

// Observe que el nivel superior usa la numeración UppercaseLetter.
// Podemos establecer la propiedad "IsLegal" para usar números arábigos en los niveles de lista superiores.
list->get_ListLevels()->idx_get(1)->set_IsLegal(true);
list->get_ListLevels()->idx_get(1)->set_RestartAfterLevel(0);

// Las etiquetas de nivel 3 serán numerales romanos en mayúsculas con un prefijo y un sufijo y se reiniciarán en cada elemento de nivel 1 de la lista.
// Estas etiquetas de lista se verán como "-I-", "-II-"...
list->get_ListLevels()->idx_get(2)->set_NumberFormat(u"-\x0002" u"-");
list->get_ListLevels()->idx_get(2)->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
list->get_ListLevels()->idx_get(2)->set_RestartAfterLevel(1);

// Haga que las etiquetas de todos los niveles de lista estén en negrita.
for (auto&& level : list->get_ListLevels())
{
    level->get_Font()->set_Bold(true);
}

// Aplique formato de lista al párrafo actual.
builder->get_ListFormat()->set_List(list);

// Cree elementos de lista que muestren los tres niveles de lista.
for (int32_t n = 0; n < 2; n++)
{
    for (int32_t i = 0; i < 3; i++)
    {
        builder->get_ListFormat()->set_ListLevelNumber(i);
        builder->Writeln(System::String(u"Level ") + i);
    }
}

builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.CreateListRestartAfterHigher.docx");
```

## Ver también

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
