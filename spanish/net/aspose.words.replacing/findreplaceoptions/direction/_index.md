---
title: FindReplaceOptions.Direction
linktitle: Direction
articleTitle: Direction
second_title: Aspose.Words para .NET
description: Descubra la propiedad Dirección de FindReplaceOptions para personalizar su función de reemplazo. Elija entre Adelante y Atrás para obtener resultados óptimos.
type: docs
weight: 40
url: /es/net/aspose.words.replacing/findreplaceoptions/direction/
---
## FindReplaceOptions.Direction property

Selecciona la dirección de reemplazo. El valor predeterminado esForward .

```csharp
public FindReplaceDirection Direction { get; set; }
```

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

* enum [FindReplaceDirection](../../findreplacedirection/)
* class [FindReplaceOptions](../)
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)
