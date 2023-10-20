---
title: TxtLoadOptions.DetectNumberingWithWhitespaces
linktitle: DetectNumberingWithWhitespaces
articleTitle: DetectNumberingWithWhitespaces
second_title: Aspose.Words para .NET
description: TxtLoadOptions DetectNumberingWithWhitespaces propiedad. Permite especificar cómo se reconocen los elementos de la lista numerados cuando el documento se importa desde formato de texto sin formato. El valor predeterminado esverdadero en C#.
type: docs
weight: 30
url: /es/net/aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/
---
## TxtLoadOptions.DetectNumberingWithWhitespaces property

Permite especificar cómo se reconocen los elementos de la lista numerados cuando el documento se importa desde formato de texto sin formato. El valor predeterminado es`verdadero`.

```csharp
public bool DetectNumberingWithWhitespaces { get; set; }
```

## Observaciones

Si esta opción está configurada en`FALSO`, el algoritmo de reconocimiento de listas detecta párrafos de listas, cuando los números de la lista terminan con ya sea un punto, un corchete derecho o un símbolo de viñeta (como "•", "*", "-" u "o").

Si esta opción está configurada en`verdadero`los espacios en blanco también se utilizan como delimitadores de números de lista: el algoritmo de reconocimiento de listas para numeración de estilo árabe (1., 1.1.2.) utiliza espacios en blanco y símbolos de punto (".").

## Ejemplos

Muestra cómo detectar listas al cargar documentos de texto sin formato.

```csharp
// Crea un documento de texto plano en una cadena con cuatro partes separadas que podemos interpretar como listas,
// con diferentes delimitadores. Al cargar el documento de texto sin formato en un objeto "Documento",
// Aspose.Words siempre detectará las tres primeras listas y agregará un objeto "Lista"
// para cada uno a la propiedad "Listas" del documento.
const string textDoc = "Full stop delimiters:\n" +
                       "1. First list item 1\n" +
                       "2. First list item 2\n" +
                       "3. First list item 3\n\n" +
                       "Right bracket delimiters:\n" +
                       "1) Second list item 1\n" +
                       "2) Second list item 2\n" +
                       "3) Second list item 3\n\n" +
                       "Bullet delimiters:\n" +
                       "• Third list item 1\n" +
                       "• Third list item 2\n" +
                       "• Third list item 3\n\n" +
                       "Whitespace delimiters:\n" +
                       "1 Fourth list item 1\n" +
                       "2 Fourth list item 2\n" +
                       "3 Fourth list item 3";

// Crea un objeto "TxtLoadOptions", que podemos pasar al constructor de un documento.
// para modificar cómo cargamos un documento de texto plano.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Establece la propiedad "DetectNumberingWithWhitespaces" en "true" para detectar elementos numerados
// con delimitadores de espacios en blanco, como la cuarta lista de nuestro documento, como listas.
// Esto también puede detectar erróneamente párrafos que comienzan con números como listas.
// Establece la propiedad "DetectNumberingWithWhitespaces" en "falso"
// para no crear listas a partir de elementos numerados con delimitadores de espacios en blanco.
loadOptions.DetectNumberingWithWhitespaces = detectNumberingWithWhitespaces;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);

if (detectNumberingWithWhitespaces)
{
    Assert.AreEqual(4, doc.Lists.Count);
    Assert.True(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
else
{
    Assert.AreEqual(3, doc.Lists.Count);
    Assert.False(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
```

### Ver también

* class [TxtLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
