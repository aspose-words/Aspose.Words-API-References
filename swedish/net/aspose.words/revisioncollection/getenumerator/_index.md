---
title: RevisionCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words för .NET
description: Upptäck RevisionCollection GetEnumerator-metoden! Hämta effektivt uppräknarobjekt för sömlös datahantering och förbättrad prestanda.
type: docs
weight: 60
url: /sv/net/aspose.words/revisioncollection/getenumerator/
---
## RevisionCollection.GetEnumerator method

Returnerar ett uppräknarobjekt.

```csharp
public IEnumerator<Revision> GetEnumerator()
```

## Exempel

Visar hur man arbetar med en dokumentsamling av revisioner.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// Den här samlingen har i sig en samling revisionsgrupper.
// Varje grupp är en sekvens av intilliggande revisioner.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// Iterera över samlingen av grupper och skriv ut texten som revisionen avser.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// Varje körning som en revision påverkar får ett motsvarande revisionsobjekt.
// Samlingen av revisionerna är betydligt större än den kondenserade versionen vi tryckte ovan,
// beroende på hur många körningar vi har segmenterat dokumentet i under redigeringen i Microsoft Word.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // En StyleDefinitionChange påverkar strikt stilar och inte dokumentnoder. Detta innebär "ParentStyle"
        // egenskapen kommer alltid att användas, medan ParentNode alltid kommer att vara null.
        // Eftersom alla andra ändringar påverkar noder, kommer ParentNode å andra sidan att användas, och ParentStyle kommer att vara null.
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

* class [Revision](../../revision/)
* class [RevisionCollection](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
