---
title: TxtLoadOptions.DetectNumberingWithWhitespaces
second_title: Referencia de API de Aspose.Words para .NET
description: TxtLoadOptions propiedad. Permite especificar cómo se reconocen los elementos de la lista numerada cuando el documento se importa desde formato de texto sin formato. El valor predeterminado es verdadero.
type: docs
weight: 20
url: /es/net/aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/
---
## TxtLoadOptions.DetectNumberingWithWhitespaces property

Permite especificar cómo se reconocen los elementos de la lista numerada cuando el documento se importa desde formato de texto sin formato. El valor predeterminado es verdadero.

```csharp
public bool DetectNumberingWithWhitespaces { get; set; }
```

### Observaciones

Si esta opción se establece en falso, el algoritmo de reconocimiento de listas detecta los párrafos de la lista, cuando los números de la lista terminan con , ya sea un punto, un corchete derecho o símbolos de viñetas (como "•", "*", "-" u "o").

Si esta opción se establece en verdadero, los espacios en blanco también se utilizan como delimitadores de números de lista: algoritmo de reconocimiento de listas para numeración de estilo árabe (1., 1.1.2.) utiliza espacios en blanco y símbolos de punto (".").

### Ejemplos

Muestra cómo detectar listas al cargar documentos de texto sin formato.

```csharp
// Crea un documento de texto sin formato en una cadena con cuatro partes separadas que podemos interpretar como listas,
// con diferentes delimitadores. Al cargar el documento de texto sin formato en un objeto "Documento",
// Aspose.Words siempre detectará las primeras tres listas y agregará un objeto "Lista"
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

// Crear un objeto "TxtLoadOptions", que podemos pasar al constructor de un documento
// para modificar cómo cargamos un documento de texto sin formato.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Establecer la propiedad "DetectNumberingWithWhitespaces" en "true" para detectar elementos numerados
// con delimitadores de espacios en blanco, como la cuarta lista de nuestro documento, como listas.
// Esto también puede detectar falsamente párrafos que comienzan con números como listas.
// Establecer la propiedad "DetectNumberingWithWhitespaces" en "false"
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
* espacio de nombres [Aspose.Words.Loading](../../txtloadoptions/)
* asamblea [Aspose.Words](../../../)


