---
title: Revision.ParentStyle
linktitle: ParentStyle
articleTitle: ParentStyle
second_title: Aspose.Words för .NET
description: Revision ParentStyle fast egendom. Hämtar den omedelbara överordnade stilen ägaren för denna version. Den här egenskapen fungerar endast förStyleDefinitionChange revisionstyp i C#.
type: docs
weight: 50
url: /sv/net/aspose.words/revision/parentstyle/
---
## Revision.ParentStyle property

Hämtar den omedelbara överordnade stilen (ägaren) för denna version. Den här egenskapen fungerar endast förStyleDefinitionChange revisionstyp.

```csharp
public Style ParentStyle { get; }
```

## Anmärkningar

Om denna version avser ändringar på dokumentnoder, använd[`ParentNode`](../parentnode/) istället.

## Exempel

Visar hur man arbetar med ett dokuments samling av revisioner.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// Denna samling i sig har en samling revisionsgrupper.
// Varje grupp är en sekvens av intilliggande revisioner.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// Iterera över samlingen av grupper och skriv ut texten som revideringen gäller.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// Varje körning som en revision påverkar får ett motsvarande revisionsobjekt.
// Revisionernas samling är avsevärt större än den sammanfattade formen vi tryckte ovan,
// beroende på hur många körningar vi har segmenterat dokumentet i under Microsoft Word-redigering.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // En StyleDefinitionChange påverkar strikt stilar och inte dokumentnoder. Detta betyder "föräldrastilen"
        //-egenskapen kommer alltid att användas, medan ParentNode alltid kommer att vara null.
        // Eftersom alla andra ändringar påverkar noder, kommer ParentNode omvänt att användas, och ParentStyle kommer att vara null.
        if (e.Current.RevisionType == RevisionType.StyleDefinitionChange)
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, style: [{e.Current.ParentStyle.Name}]");
        }
        else
        {
            Console.WriteLine($"\tRevision type \"{e.Current.RevisionType}\", " +
                              $"author: {e.Current.Author}, contents: [{e.Current.ParentNode.GetText().Trim()}]");
        }
    }
}

// Avvisa alla revisioner via samlingen, återställ dokumentet till dess ursprungliga form.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### Se även

* class [Style](../../style/)
* class [Revision](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
