---
title: Range.Fields
linktitle: Fields
articleTitle: Fields
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Range Fields och få enkel tillgång till en omfattande Fields-samling för alla dina behov av dataintervall. Förbättra ditt arbetsflöde idag!
type: docs
weight: 20
url: /sv/net/aspose.words/range/fields/
---
## Range.Fields property

Returnerar en`Fields` samling som representerar alla fält i intervallet.

```csharp
public FieldCollection Fields { get; }
```

## Exempel

Visar hur man anpassar nodändringar med en återanrop.

```csharp
public void FontChangeViaCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Ställ in nodändringsmotringningen till anpassad implementering,
    // lägg sedan till/ta bort noder för att få den att generera en logg.
    HandleNodeChangingFontChanger callback = new HandleNodeChangingFontChanger();
    doc.NodeChangingCallback = callback;

    builder.Writeln("Hello world!");
    builder.Writeln("Hello again!");
    builder.InsertField(" HYPERLINK \"https://www.google.com/\" ");
    builder.InsertShape(ShapeType.Rectangle, 300, 300);

    doc.Range.Fields[0].Remove();

    Console.WriteLine(callback.GetLog());
}

/// <summary>
/// Loggar datum och tid för varje nodinsättning och borttagning.
/// Anger ett anpassat teckensnittsnamn/storlek för textinnehållet i Run-noder.
/// </summary>
public class HandleNodeChangingFontChanger : INodeChangingCallback
{
    void INodeChangingCallback.NodeInserted(NodeChangingArgs args)
    {
        mLog.AppendLine($"\tType:\t{args.Node.NodeType}");
        mLog.AppendLine($"\tHash:\t{args.Node.GetHashCode()}");

        if (args.Node.NodeType == NodeType.Run)
        {
            Aspose.Words.Font font = ((Run)args.Node).Font;
            mLog.Append($"\tFont:\tChanged from \"{font.Name}\" {font.Size}pt");

            font.Size = 24;
            font.Name = "Arial";

            mLog.AppendLine($" to \"{font.Name}\" {font.Size}pt");
            mLog.AppendLine($"\tContents:\n\t\t\"{args.Node.GetText()}\"");
        }
    }

    void INodeChangingCallback.NodeInserting(NodeChangingArgs args)
    {
        mLog.AppendLine($"\n{DateTime.Now:dd/MM/yyyy HH:mm:ss:fff}\tNode insertion:");
    }

    void INodeChangingCallback.NodeRemoved(NodeChangingArgs args)
    {
        mLog.AppendLine($"\tType:\t{args.Node.NodeType}");
        mLog.AppendLine($"\tHash code:\t{args.Node.GetHashCode()}");
    }

    void INodeChangingCallback.NodeRemoving(NodeChangingArgs args)
    {
        mLog.AppendLine($"\n{DateTime.Now:dd/MM/yyyy HH:mm:ss:fff}\tNode removal:");
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

### Se även

* class [FieldCollection](../../../aspose.words.fields/fieldcollection/)
* class [Range](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
