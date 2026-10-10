---
title: "Aspose::Words::Lists::ListLevel::get_LinkedStyle método"
linktitle: "get_LinkedStyle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Lists::ListLevel::get_LinkedStyle método. Obtiene o establece el estilo de párrafo que está vinculado a este nivel de lista en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.lists/listlevel/get_linkedstyle/
---
## ListLevel::get_LinkedStyle method


Obtiene o establece el estilo de párrafo que está vinculado a este nivel de lista.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Lists::ListLevel::get_LinkedStyle()
```

## Observaciones


Esta propiedad es **null** cuando el nivel de lista no está vinculado a un estilo de párrafo. Esta propiedad puede establecerse en **null**.

## Ejemplos



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

* Class [Style](../../../aspose.words/style/)
* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
