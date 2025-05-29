---
title: FindReplaceOptions Class
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.FindReplaceOptions para obtener funciones avanzadas de búsqueda y reemplazo, mejorando la edición de documentos con precisión y flexibilidad.
type: docs
weight: 5350
url: /es/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Especifica opciones para operaciones de búsqueda y reemplazo.

Para obtener más información, visite el[Buscar y reemplazar](https://docs.aspose.com/words/net/find-and-replace/) Artículo de documentación.

```csharp
public class FindReplaceOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | Inicializa una nueva instancia de la clase FindReplaceOptions con la configuración predeterminada. |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(*[FindReplaceDirection](../findreplacedirection/)*) | Inicializa una nueva instancia de la clase FindReplaceOptions con la dirección especificada. |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(*[IReplacingCallback](../ireplacingcallback/)*) | Inicializa una nueva instancia de la clase FindReplaceOptions con la devolución de llamada de reemplazo especificada. |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(*[FindReplaceDirection](../findreplacedirection/), [IReplacingCallback](../ireplacingcallback/)*) | Inicializa una nueva instancia de la clase FindReplaceOptions con la dirección especificada y la devolución de llamada de reemplazo. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | Formato de texto aplicado al nuevo contenido. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | Formato de párrafo aplicado al nuevo contenido. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | Selecciona la dirección de reemplazo. El valor predeterminado esForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | True indica que el valor anterior debe ser una palabra independiente. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de las revisiones eliminadas. El valor predeterminado es`FALSO` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de los códigos de campo. El valor predeterminado es`FALSO` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de los campos. El valor predeterminado es`FALSO` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | Obtiene o establece un valor booleano que indica si se deben ignorar las notas al pie. El valor predeterminado es`FALSO` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de las revisiones de inserción. El valor predeterminado es`FALSO` . |
| [IgnoreShapes](../../aspose.words.replacing/findreplaceoptions/ignoreshapes/) { get; set; } | Obtiene o establece un valor booleano que indica si se deben ignorar las formas dentro de un texto. |
| [IgnoreStructuredDocumentTags](../../aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/) { get; set; } | Obtiene o establece un valor booleano que indica si se debe ignorar el contenido de[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) . El valor predeterminado es`FALSO` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Obtiene o establece un valor booleano que indica que se utiliza el antiguo algoritmo de búsqueda/reemplazo. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | Verdadero indica una comparación que distingue entre mayúsculas y minúsculas, falso indica una comparación que no distingue entre mayúsculas y minúsculas. |
| [ReplacementFormat](../../aspose.words.replacing/findreplaceoptions/replacementformat/) { get; set; } | Especifica el formato del reemplazo. El valor predeterminado esText . |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | El método definido por el usuario que se llama antes de cada ocurrencia de reemplazo. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Obtiene o establece un valor booleano que indica que está permitido reemplazar el párrafo break cuando no hay un siguiente párrafo hermano. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True indica que se realiza una búsqueda de texto secuencialmente de arriba a abajo considerando los cuadros de texto. El valor predeterminado es`FALSO` . |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Obtiene o establece un valor booleano que indica si se deben reconocer y utilizar sustituciones dentro de los patrones de reemplazo. El valor predeterminado es`FALSO` . |

## Ejemplos

Muestra cómo alternar la distinción entre mayúsculas y minúsculas al realizar una operación de búsqueda y reemplazo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "MatchCase" en "verdadero" para aplicar distinción entre mayúsculas y minúsculas al buscar cadenas para reemplazar.
// Establezca el indicador "MatchCase" en "falso" para ignorar las mayúsculas y minúsculas mientras busca texto para reemplazar.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Muestra cómo alternar operaciones de búsqueda y reemplazo independientes de solo palabras.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "FindWholeWordsOnly" en "verdadero" para reemplazar el texto encontrado si no es parte de otra palabra.
// Establezca el indicador "FindWholeWordsOnly" en "falso" para reemplazar todo el texto independientemente de su entorno.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Ver también

* espacio de nombres [Aspose.Words.Replacing](../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../)
