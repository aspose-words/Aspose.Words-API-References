---
title: ReplacingArgs.GroupName
linktitle: GroupName
articleTitle: GroupName
second_title: Aspose.Words para .NET
description: Descubre cómo usar eficazmente la propiedad GroupName para reemplazar grupos capturados en tus coincidencias con cadenas personalizadas. ¡Mejora tus habilidades de manipulación de cadenas!
type: docs
weight: 20
url: /es/net/aspose.words.replacing/replacingargs/groupname/
---
## ReplacingArgs.GroupName property

Identifica, por nombre, un grupo capturado en el[`Match`](../match/) que se va a reemplazar con el[`Replacement`](../replacement/) cadena.

```csharp
public string GroupName { get; set; }
```

## Observaciones

Cuando el nombre del grupo es`nulo` ,[`GroupIndex`](../groupindex/) Se utiliza para identificar al grupo.

El valor predeterminado es`nulo`.

## Ejemplos

Muestra cómo aplicar una fuente diferente al contenido nuevo a través de FindReplaceOptions.

```csharp
public void ConvertNumbersToHexadecimal()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Arial";
    builder.Writeln("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\n" +
                    "123, 456, 789 and 17379.");

    // Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de búsqueda y reemplazo.
    FindReplaceOptions options = new FindReplaceOptions();

    // Establezca la propiedad "HighlightColor" en un color de fondo que queremos aplicar al texto resultante de la operación.
    options.ApplyFont.HighlightColor = Color.LightGray;

    NumberHexer numberHexer = new NumberHexer();
    options.ReplacingCallback = numberHexer;

    int replacementCount = doc.Range.Replace(new Regex("[0-9]+"), "", options);

    Console.WriteLine(numberHexer.GetLog());

    Assert.AreEqual(4, replacementCount);
    Assert.AreEqual("Numbers that the find-and-replace operation will convert to hexadecimal and highlight:\r" +
                    "0x7B, 0x1C8, 0x315 and 0x43E3.", doc.GetText().Trim());
    Assert.AreEqual(4, doc.GetChildNodes(NodeType.Run, true).OfType<Run>()
            .Count(r => r.Font.HighlightColor.ToArgb() == Color.LightGray.ToArgb()));
}

/// <summary>
/// Reemplaza las coincidencias numéricas de búsqueda y reemplazo con sus equivalentes hexadecimales.
/// Mantiene un registro de cada reemplazo.
/// </summary>
private class NumberHexer : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mCurrentReplacementNumber++;

        int number = Convert.ToInt32(args.Match.Value);

        args.Replacement = $"0x{number:X}";

        mLog.AppendLine($"Match #{mCurrentReplacementNumber}");
        mLog.AppendLine($"\tOriginal value:\t{args.Match.Value}");
        mLog.AppendLine($"\tReplacement:\t{args.Replacement}");
        mLog.AppendLine($"\tOffset in parent {args.MatchNode.NodeType} node:\t{args.MatchOffset}");

        mLog.AppendLine(string.IsNullOrEmpty(args.GroupName)
            ? $"\tGroup index:\t{args.GroupIndex}"
            : $"\tGroup name:\t{args.GroupName}");

        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private int mCurrentReplacementNumber;
    private readonly StringBuilder mLog = new StringBuilder();
}
```

### Ver también

* class [ReplacingArgs](../)
* espacio de nombres [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* asamblea [Aspose.Words](../../../)
