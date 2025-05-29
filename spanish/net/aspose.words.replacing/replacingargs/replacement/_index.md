---
title: ReplacingArgs.Replacement
linktitle: Replacement
articleTitle: Replacement
second_title: Aspose.Words para .NET
description: Descubra la propiedad de reemplazo ReplacingArgs para administrar y personalizar fácilmente sus cadenas de reemplazo para una mejor eficiencia de codificación.
type: docs
weight: 60
url: /es/net/aspose.words.replacing/replacingargs/replacement/
---
## ReplacingArgs.Replacement property

Obtiene o establece la cadena de reemplazo.

```csharp
public string Replacement { get; set; }
```

## Ejemplos

Muestra cómo reemplazar todas las ocurrencias de un patrón de expresión regular con otra cadena, mientras se rastrean todos dichos reemplazos.

```csharp
public void ReplaceWithCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
    FindReplaceOptions options = new FindReplaceOptions();

    // Establezca una devolución de llamada que rastree cualquier reemplazo que realizará el método "Reemplazar".
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Mantiene un registro de cada reemplazo de texto realizado mediante una operación de búsqueda y reemplazo
/// y anota el valor del texto original coincidente.
/// </summary>
private class TextFindAndReplacementLogger : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        mLog.AppendLine($"\"{args.Match.Value}\" converted to \"{args.Replacement}\" " +
                        $"{args.MatchOffset} characters into a {args.MatchNode.NodeType} node.");

        args.Replacement = $"(Old value:\"{args.Match.Value}\") {args.Replacement}";
        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

### Ver también

* class [ReplacingArgs](../)
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)
