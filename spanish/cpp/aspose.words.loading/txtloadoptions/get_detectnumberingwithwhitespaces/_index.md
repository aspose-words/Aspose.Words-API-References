---
title: "Método Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces"
linktitle: "get_DetectNumberingWithWhitespaces"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces. Permite especificar cómo se reconocen los elementos de listas numeradas cuando el documento se importa desde formato de texto plano. El valor predeterminado es true en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.loading/txtloadoptions/get_detectnumberingwithwhitespaces/
---
## TxtLoadOptions::get_DetectNumberingWithWhitespaces method


Permite especificar cómo se reconocen los elementos de listas numeradas cuando el documento se importa desde formato de texto plano. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Loading::TxtLoadOptions::get_DetectNumberingWithWhitespaces() const
```

## Observaciones


Si esta opción se establece en **false**, el algoritmo de reconocimiento de listas detecta los párrafos de lista cuando los números de lista terminan con un punto, un corchete derecho o símbolos de viñeta (como "•", "*", "-" o "o").

Si esta opción se establece en **true**, los espacios en blanco también se utilizan como delimitadores de números de lista: el algoritmo de reconocimiento de listas para numeración al estilo árabe (1., 1.1.2.) usa tanto los espacios en blanco como el punto (".") como símbolos.

## Ejemplos



Muestra cómo detectar listas al cargar documentos de texto plano.
```cpp
// Cree un documento de texto plano en una cadena con cuatro partes separadas que podemos interpretar como listas,
// con diferentes delimitadores. Al cargar el documento de texto plano en un objeto "Document",
// Aspose.Words siempre detectará las tres primeras listas y añadirá un objeto "List"
// para cada una en la propiedad "Lists" del documento.
const System::String textDoc = System::String(u"Full stop delimiters:\n") + u"1. First list item 1\n" + u"2. First list item 2\n" + u"3. First list item 3\n\n" + u"Right bracket delimiters:\n" + u"1) Second list item 1\n" + u"2) Second list item 2\n" + u"3) Second list item 3\n\n" + u"Bullet delimiters:\n" + u"• Third list item 1\n" + u"• Third list item 2\n" + u"• Third list item 3\n\n" + u"Whitespace delimiters:\n" + u"1 Fourth list item 1\n" + u"2 Fourth list item 2\n" + u"3 Fourth list item 3";

// Cree un objeto "TxtLoadOptions", que podemos pasar al constructor de un documento
// para modificar cómo cargamos un documento de texto plano.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::TxtLoadOptions>();

// Establezca la propiedad "DetectNumberingWithWhitespaces" en "true" para detectar elementos numerados
// con delimitadores de espacio en blanco, como la cuarta lista en nuestro documento, como listas.
// Esto también puede detectar falsamente párrafos que comienzan con números como listas.
// Establezca la propiedad "DetectNumberingWithWhitespaces" en "false"
// para no crear listas a partir de elementos numerados con delimitadores de espacio en blanco.
loadOptions->set_DetectNumberingWithWhitespaces(detectNumberingWithWhitespaces);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(textDoc)), loadOptions);

if (detectNumberingWithWhitespaces)
{
    ASSERT_EQ(4, doc->get_Lists()->get_Count());
    ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
    {
        return p->GetText().Contains(u"Fourth list") && (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_IsListItem();
    }))));
}
else
{
    ASSERT_EQ(3, doc->get_Lists()->get_Count());
    ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> p)>>([](System::SharedPtr<Aspose::Words::Node> p) -> bool
    {
        return p->GetText().Contains(u"Fourth list") && (System::ExplicitCast<Aspose::Words::Paragraph>(p))->get_IsListItem();
    }))));
}
```

## Ver también

* Class [TxtLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
