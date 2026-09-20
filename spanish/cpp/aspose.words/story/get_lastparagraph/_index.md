---
title: "Método Aspose::Words::Story::get_LastParagraph"
linktitle: "get_LastParagraph"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Story::get_LastParagraph. Obtiene el último párrafo de la historia en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/story/get_lastparagraph/
---
## Story::get_LastParagraph method


Obtiene el último párrafo de la historia.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::get_LastParagraph() override
```


## Ejemplos



Muestra cómo mover la posición del cursor de un [DocumentBuilder](../../documentbuilder/) a un nodo especificado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Run 1. ");

// El constructor de documentos tiene un cursor, que actúa como la parte del documento
// donde el constructor agrega nuevos nodos cuando usamos sus métodos de construcción de documentos.
// Este cursor funciona de la misma manera que el cursor intermitente de Microsoft Word,
// y también siempre termina inmediatamente después de cualquier nodo que el constructor acaba de insertar.
// Para agregar contenido a una parte diferente del documento,
// podemos mover el cursor a un nodo diferente con el método "MoveTo".
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

// El cursor ahora está delante del nodo al que lo movimos.
// Agregar una segunda ejecución lo insertará delante de la primera ejecución.
builder->Writeln(u"Run 2. ");

ASSERT_EQ(u"Run 2. \rRun 1.", doc->GetText().Trim());

// Mueva el cursor al final del documento para continuar agregando texto al final como antes.
builder->MoveTo(doc->get_LastSection()->get_Body()->get_LastParagraph());
builder->Writeln(u"Run 3. ");

ASSERT_EQ(u"Run 2. \rRun 1. \rRun 3.", doc->GetText().Trim());
```

## Ver también

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
