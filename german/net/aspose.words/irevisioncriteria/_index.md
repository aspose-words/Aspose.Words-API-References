---
title: IRevisionCriteria Interface
linktitle: IRevisionCriteria
articleTitle: IRevisionCriteria
second_title: Aspose.Words für .NET
description: Kontrollieren Sie Dokumentrevisionen mühelos mit Aspose.Words.IRevisionCriteria. Passen Sie die Annahme und Ablehnung von Änderungen für ein präzises Dokumentenmanagement an.
type: docs
weight: 3650
url: /de/net/aspose.words/irevisioncriteria/
---
## IRevisionCriteria interface

Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wann bestimmte[`Revision`](../revision/) sollte akzeptiert/abgelehnt werden oder nicht von der[`Accept`](../revisioncollection/accept/)/[`Reject`](../revisioncollection/reject/) Methoden.

```csharp
public interface IRevisionCriteria
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [IsMatch](../../aspose.words/irevisioncriteria/ismatch/)(*[Revision](../revision/)*) | Überprüft, ob angegeben*revision* entspricht den Kriterien. |

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
