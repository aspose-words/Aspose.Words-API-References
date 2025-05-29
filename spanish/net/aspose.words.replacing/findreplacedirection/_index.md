---
title: FindReplaceDirection Enum
linktitle: FindReplaceDirection
articleTitle: FindReplaceDirection
second_title: Aspose.Words para .NET
description: Descubra la enumeración FindReplaceDirection de Aspose.Words para un reemplazo de texto eficiente. Optimice el procesamiento de sus documentos con un control preciso de la dirección.
type: docs
weight: 5340
url: /es/net/aspose.words.replacing/findreplacedirection/
---
## FindReplaceDirection enumeration

Especifica la dirección para las operaciones de reemplazo.

```csharp
public enum FindReplaceDirection
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Forward | `0` | Los elementos coincidentes se reemplazan del primero al último. |
| Backward | `1` | Los elementos coincidentes se reemplazan desde el último hasta el primero. |

## Ejemplos

Muestra cómo determinar en qué dirección una operación de búsqueda y reemplazo recorre el documento.

```csharp
public void Direction(FindReplaceDirection findReplaceDirection)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserte tres ejecuciones que podamos buscar usando un patrón de expresiones regulares.
    //Coloca una de esas carreras dentro de un cuadro de texto.
    builder.Writeln("Match 1.");
    builder.Writeln("Match 2.");
    builder.Writeln("Match 3.");
    builder.Writeln("Match 4.");

    // Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
    FindReplaceOptions options = new FindReplaceOptions();

    // Asigna una devolución de llamada personalizada a la propiedad "ReplacingCallback".
    TextReplacementRecorder callback = new TextReplacementRecorder();
    options.ReplacingCallback = callback;

    // Establezca la propiedad "Dirección" en "FindReplaceDirection.Backward" para obtener la función de búsqueda y reemplazo
    // operación para comenzar desde el final del rango y recorrer de regreso hasta el principio.
    // Establezca la propiedad "Dirección" en "FindReplaceDirection.Forward" para obtener la función de búsqueda y reemplazo
    // operación para comenzar desde el principio del rango y recorrer hasta el final.
    options.Direction = findReplaceDirection;

    doc.Range.Replace(new Regex(@"Match \d*"), "Replacement", options);

    Assert.AreEqual("Replacement.\r" +
                    "Replacement.\r" +
                    "Replacement.\r" +
                    "Replacement.", doc.GetText().Trim());

    switch (findReplaceDirection)
    {
        case FindReplaceDirection.Forward:
            Assert.AreEqual(new[] { "Match 1", "Match 2", "Match 3", "Match 4" }, callback.Matches);
            break;
        case FindReplaceDirection.Backward:
            Assert.AreEqual(new[] { "Match 4", "Match 3", "Match 2", "Match 1" }, callback.Matches);
            break;
    }
}

/// <summary>
/// Registra todas las coincidencias que ocurren durante una operación de búsqueda y reemplazo en el orden en que tienen lugar.
/// </summary>
private class TextReplacementRecorder : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs e)
    {
        Matches.Add(e.Match.Value);
        return ReplaceAction.Replace;
    }

    public List<string> Matches { get; } = new List<string>();
}
```

### Ver también

* espacio de nombres [Aspose.Words.Replacing](../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../)
