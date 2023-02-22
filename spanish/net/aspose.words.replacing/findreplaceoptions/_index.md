---
title: Class FindReplaceOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Replacing.FindReplaceOptions clase. Especifica opciones para operaciones de búsqueda/reemplazo.
type: docs
weight: 4360
url: /es/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Especifica opciones para operaciones de búsqueda/reemplazo.

```csharp
public class FindReplaceOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | Constructor predeterminado |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(FindReplaceDirection) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(IReplacingCallback) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(FindReplaceDirection, IReplacingCallback) |  |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | Formato de texto aplicado al nuevo contenido. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | Formato de párrafo aplicado al nuevo contenido. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | Selecciona la dirección para reemplazar. El valor predeterminado esForward . |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | True indica que oldValue debe ser una palabra independiente. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | Obtiene o establece un valor booleano que indica ignorar el texto dentro de eliminar revisiones. El valor predeterminado es`falso` . |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | Obtiene o establece un valor booleano que indica ignorar el texto dentro de los códigos de campo. El valor predeterminado es`falso` . |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | Obtiene o establece un valor booleano que indica ignorar el texto dentro de los campos. El valor predeterminado es`falso` . |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | Obtiene o establece un valor booleano que indica ignorar las notas al pie. El valor predeterminado es`falso` . |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | Obtiene o establece un valor booleano que indica ignorar el texto dentro de las revisiones de inserción. El valor predeterminado es`falso` . |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Obtiene o establece un valor booleano que indica que se utiliza el antiguo algoritmo de búsqueda/reemplazo. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | Verdadero indica una comparación que distingue entre mayúsculas y minúsculas, falso indica una comparación que no distingue entre mayúsculas y minúsculas. |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | El método definido por el usuario que se llama antes de cada reemplazo. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Obtiene o establece un valor booleano que indica que se permite reemplazar el párrafo break cuando no hay un siguiente párrafo relacionado. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True indica que una búsqueda de texto se realiza secuencialmente de arriba a abajo considerando los cuadros de texto. El valor por defecto es false. |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Obtiene o establece un valor booleano que indica si reconocer y usar sustituciones dentro de patrones de reemplazo. El valor predeterminado es`falso` . |

### Ejemplos

Muestra cómo alternar entre mayúsculas y minúsculas al realizar una operación de buscar y reemplazar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "MatchCase" en "verdadero" para aplicar la distinción entre mayúsculas y minúsculas mientras busca cadenas para reemplazar.
// Establezca el indicador "MatchCase" en "falso" para ignorar las mayúsculas y minúsculas mientras busca texto para reemplazar.
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

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
FindReplaceOptions options = new FindReplaceOptions();

// Establezca el indicador "FindWholeWordsOnly" en "true" para reemplazar el texto encontrado si no forma parte de otra palabra.
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


