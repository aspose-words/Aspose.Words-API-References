---
title: "Aspose::Words::Lists::ListFormat::RemoveNumbers método"
linktitle: "RemoveNumbers"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Lists::ListFormat::RemoveNumbers método. Elimina números o viñetas del párrafo actual y establece el nivel de lista a cero en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.lists/listformat/removenumbers/
---
## ListFormat::RemoveNumbers method


Elimina los números o viñetas del párrafo actual y establece el nivel de lista a cero.

```cpp
void Aspose::Words::Lists::ListFormat::RemoveNumbers()
```

## Observaciones


Llamar a este método es equivalente a establecer la propiedad [List](../get_list/) a **null**.

## Ejemplos



Muestra cómo crear listas con viñetas y numeradas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Aspose.Words main advantages are:");

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría.
// Podemos iniciar y terminar una lista usando la propiedad "ListFormat" de un document builder.
// Cada párrafo que añadamos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// A continuación se presentan dos tipos de listas que podemos crear con un Document Builder.
// 1 -  Una lista con viñetas:
// Esta lista aplicará una sangría y un símbolo de viñeta ("•") antes de cada párrafo.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Great performance");
builder->Writeln(u"High reliability");
builder->Writeln(u"Quality code and working");
builder->Writeln(u"Wide variety of features");
builder->Writeln(u"Easy to understand API");

// Finaliza la lista con viñetas.
builder->get_ListFormat()->RemoveNumbers();

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->Writeln(u"Aspose.Words allows:");

// 2 -  Una lista numerada:
// Las listas numeradas crean un orden lógico para sus párrafos numerando cada elemento.
builder->get_ListFormat()->ApplyNumberDefault();

// Este párrafo es el primer elemento. El primer elemento de una lista numerada tendrá un \"1.\" como símbolo del elemento de la lista.
builder->Writeln(u"Opening documents from different formats:");

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Llame al método "ListIndent" para aumentar el nivel de lista actual,
// lo que iniciará una nueva lista independiente, con una sangría más profunda, en el elemento actual del primer nivel de lista.
builder->get_ListFormat()->ListIndent();

ASSERT_EQ(1, builder->get_ListFormat()->get_ListLevelNumber());

// Estos son los primeros tres elementos de lista del segundo nivel de lista, que mantendrán un recuento
// independiente del recuento del primer nivel de lista. Según el formato de lista actual,
// tendrán símbolos de "a.", "b.", y "c.".
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");

// Llame al método "ListOutdent" para volver al nivel de lista anterior.
builder->get_ListFormat()->ListOutdent();

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Estos dos párrafos continuarán el recuento del primer nivel de lista.
// Estos elementos tendrán símbolos de "2.", y "3."
builder->Writeln(u"Processing documents");
builder->Writeln(u"Saving documents in different formats:");

// Si aumentamos el nivel de lista a un nivel al que ya habíamos añadido elementos previamente,
// la lista anidada será independiente de la anterior, y su numeración comenzará desde el principio.
// Estos elementos de lista tendrán símbolos de "a.", "b.", "c.", "d.", y "e".
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");
builder->Writeln(u"MHTML");
builder->Writeln(u"Plain text");

// Desplace la sangría del nivel de lista nuevamente.
builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"Doing many other things!");

// Finalice la lista numerada.
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.ApplyDefaultBulletsAndNumbers.docx");
```


Muestra cómo eliminar el formato de lista de todos los párrafos en el texto principal de una sección.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");
builder->Writeln(u"Numbered list item 3");
builder->get_ListFormat()->RemoveNumbers();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);
ASSERT_EQ(3, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));

for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(paras))
{
    paragraph->get_ListFormat()->RemoveNumbers();
}

ASSERT_EQ(0, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));
```

## Ver también

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
