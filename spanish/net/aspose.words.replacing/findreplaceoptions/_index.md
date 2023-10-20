---
title: FindReplaceOptions Class
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words para .NET
description: Aspose.Words.Replacing.FindReplaceOptions clase. Especifica opciones para operaciones de buscar/reemplazar en C#.
type: docs
weight: 4620
url: /es/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Especifica opciones para operaciones de buscar/reemplazar.

Para obtener más información, visite el[Encontrar y reemplazar](https://docs.aspose.com/words/net/find-and-replace/) artículo de documentación.

```csharp
public class FindReplaceOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | Constructor predeterminado |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(*[FindReplaceDirection](../findreplacedirection/)*) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(*[IReplacingCallback](../ireplacingcallback/)*) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(*[FindReplaceDirection](../findreplacedirection/), [IReplacingCallback](../ireplacingcallback/)*) |  |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | Formato de texto aplicado al contenido nuevo. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | Formato de párrafo aplicado al contenido nuevo. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | Selecciona la dirección para reemplazar. El valor predeterminado esForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | Verdadero indica que oldValue debe ser una palabra independiente. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | Obtiene o establece un valor booleano que indica que se debe ignorar el texto dentro de las revisiones de eliminación. El valor predeterminado es`FALSO` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | Obtiene o establece un valor booleano que indica que se debe ignorar el texto dentro de los códigos de campo. El valor predeterminado es`FALSO` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | Obtiene o establece un valor booleano que indica que se debe ignorar el texto dentro de los campos. El valor predeterminado es`FALSO` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | Obtiene o establece un valor booleano que indica que se deben ignorar las notas al pie. El valor predeterminado es`FALSO` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | Obtiene o establece un valor booleano que indica que se debe ignorar el texto dentro de las revisiones de inserción. El valor predeterminado es`FALSO` . |
| [IgnoreShapes](../../aspose.words.replacing/findreplaceoptions/ignoreshapes/) { get; set; } | Obtiene o establece un valor booleano que indica que se deben ignorar las formas dentro de un texto. |
| [IgnoreStructuredDocumentTags](../../aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/) { get; set; } | Obtiene o establece un valor booleano que indica que se debe ignorar el contenido de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) . El valor predeterminado es`FALSO` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Obtiene o establece un valor booleano que indica que se utiliza el antiguo algoritmo de búsqueda/reemplazo. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | Verdadero indica una comparación que distingue entre mayúsculas y minúsculas, falso indica una comparación que no distingue entre mayúsculas y minúsculas. |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | El método definido por el usuario que se llama antes de cada sustitución. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Obtiene o establece un valor booleano que indica que se permite reemplazar el párrafo break cuando no hay un siguiente párrafo hermano. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | Verdadero indica que una búsqueda de texto se realiza secuencialmente de arriba a abajo considerando los cuadros de texto. El valor predeterminado es`FALSO` . |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Obtiene o establece un valor booleano que indica si se reconocen y utilizan sustituciones dentro de los patrones de reemplazo. El valor predeterminado es`FALSO` . |

## Ejemplos

Muestra cómo alternar la distinción entre mayúsculas y minúsculas al realizar una operación de buscar y reemplazar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Podemos utilizar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
FindReplaceOptions options = new FindReplaceOptions();

// Establece el indicador "MatchCase" en "true" para aplicar distinción entre mayúsculas y minúsculas mientras buscas cadenas para reemplazar.
// Establece el indicador "MatchCase" en "false" para ignorar las mayúsculas y minúsculas mientras buscas texto para reemplazar.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Muestra cómo alternar operaciones independientes de búsqueda y reemplazo de solo palabras.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Podemos utilizar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
FindReplaceOptions options = new FindReplaceOptions();

// Establece el indicador "FindWholeWordsOnly" en "true" para reemplazar el texto encontrado si no forma parte de otra palabra.
// Establece el indicador "FindWholeWordsOnly" en "false" para reemplazar todo el texto independientemente de su entorno.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Ver también

* espacio de nombres [Aspose.Words.Replacing](../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../)
