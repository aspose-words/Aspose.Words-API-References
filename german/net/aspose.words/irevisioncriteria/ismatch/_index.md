---
title: IRevisionCriteria.IsMatch
linktitle: IsMatch
articleTitle: IsMatch
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die IsMatch-Methode von IRevisionCriteria effektiv überprüft, ob eine bestimmte Revision Ihren Kriterien für optimale Ergebnisse entspricht.
type: docs
weight: 10
url: /de/net/aspose.words/irevisioncriteria/ismatch/
---
## IRevisionCriteria.IsMatch method

Überprüft, ob angegeben*revision* entspricht den Kriterien.

```csharp
public bool IsMatch(Revision revision)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| revision | Revision | Der[`Revision`](../../revision/) Instanz, um den Kriterien zu entsprechen. |

### Rückgabewert

`WAHR` wenn die*revision* entspricht den Kriterien, andernfalls`FALSCH`.

## Bemerkungen

Die Methodenimplementierung sollte die Revision aufgrund unerwarteter Ergebnisse weder akzeptieren/ablehnen noch in irgendeiner Weise ändern.

## Beispiele

Zeigt, wie eine Revision auf Grundlage von Kriterien angenommen oder abgelehnt wird.

```csharp
public void RevisionSpecifiedCriteria()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Write("This does not count as a revision. ");

    // Um unsere Änderungen als Revisionen zu registrieren, müssen wir einen Autor angeben und dann mit der Verfolgung beginnen.
    doc.StartTrackRevisions("John Doe", DateTime.Now);
    builder.Write("This is insertion revision #1. ");
    doc.StopTrackRevisions();

    doc.StartTrackRevisions("Jane Doe", DateTime.Now);
    builder.Write("This is insertion revision #2. ");
    // Einen Lauf entfernen „Dies zählt nicht als Revision.“.
    doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();
    doc.StopTrackRevisions();

    Assert.AreEqual(3, doc.Revisions.Count);
    // Wir haben zwei Revisionen von verschiedenen Autoren, also müssen wir nur eine akzeptieren.
    doc.Revisions.Accept(new RevisionCriteria("John Doe", RevisionType.Insertion));
    Assert.AreEqual(2, doc.Revisions.Count);
    // Revision mit anderem Autorennamen und Revisionstyp ablehnen.
    doc.Revisions.Reject(new RevisionCriteria("Jane Doe", RevisionType.Deletion));
    Assert.AreEqual(1, doc.Revisions.Count);

    doc.Save(ArtifactsDir + "Revision.RevisionSpecifiedCriteria.docx");
}

/// <summary>
/// Steuern Sie, wann bestimmte Revisionen akzeptiert/abgelehnt werden sollen.
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

### Siehe auch

* class [Revision](../../revision/)
* interface [IRevisionCriteria](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
