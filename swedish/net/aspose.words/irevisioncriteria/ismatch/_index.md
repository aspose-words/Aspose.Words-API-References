---
title: IRevisionCriteria.IsMatch
linktitle: IsMatch
articleTitle: IsMatch
second_title: Aspose.Words för .NET
description: Upptäck hur metoden IRevisionCriteria IsMatch effektivt verifierar om en specifik revision överensstämmer med dina kriterier för optimala resultat.
type: docs
weight: 10
url: /sv/net/aspose.words/irevisioncriteria/ismatch/
---
## IRevisionCriteria.IsMatch method

Kontrollerar om det är specificerat eller inte*revision* matchar kriterierna.

```csharp
public bool IsMatch(Revision revision)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| revision | Revision | De[`Revision`](../../revision/) exempel för att matcha kriterier. |

### Returvärde

`Sann` om den*revision* matchar kriterierna, annars`Falsk`.

## Anmärkningar

Metodimplementeringen ska inte acceptera/avvisa revisionen eller modifiera den på något sätt på grund av oväntade resultat.

## Exempel

Visar hur man accepterar eller avvisar revisioner baserat på kriterier.

```csharp
public void RevisionSpecifiedCriteria()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Write("This does not count as a revision. ");

    // För att registrera våra redigeringar som revisioner måste vi ange en författare och sedan börja spåra dem.
    doc.StartTrackRevisions("John Doe", DateTime.Now);
    builder.Write("This is insertion revision #1. ");
    doc.StopTrackRevisions();

    doc.StartTrackRevisions("Jane Doe", DateTime.Now);
    builder.Write("This is insertion revision #2. ");
    // Ta bort en körning "Detta räknas inte som en revision.".
    doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();
    doc.StopTrackRevisions();

    Assert.AreEqual(3, doc.Revisions.Count);
    // Vi har två revisioner från olika författare, så vi behöver bara acceptera en.
    doc.Revisions.Accept(new RevisionCriteria("John Doe", RevisionType.Insertion));
    Assert.AreEqual(2, doc.Revisions.Count);
    // Avvisa revision med annat författarnamn och revisionstyp.
    doc.Revisions.Reject(new RevisionCriteria("Jane Doe", RevisionType.Deletion));
    Assert.AreEqual(1, doc.Revisions.Count);

    doc.Save(ArtifactsDir + "Revision.RevisionSpecifiedCriteria.docx");
}

/// <summary>
/// Styr när en viss revision ska accepteras/avvisas.
/// </summary>
public class RevisionCriteria : IRevisionCriteria
{
    private readonly string AuthorName;
    private readonly RevisionType RevisionType;

    public RevisionCriteria(string authorName, RevisionType revisionType)
    {
        AuthorName = authorName;
        RevisionType = revisionType;
    }

    public bool IsMatch(Revision revision)
    {
        return revision.Author == AuthorName && revision.RevisionType == RevisionType;
    }
}
```

### Se även

* class [Revision](../../revision/)
* interface [IRevisionCriteria](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
