---
title: RevisionCollection.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words für .NET
description: Entdecken Sie die RevisionCollection-Accept-Methode, um Revisionen einfach anhand Ihrer Kriterien für optimierte Projektaktualisierungen zu verwalten und zu filtern.
type: docs
weight: 40
url: /de/net/aspose.words/revisioncollection/accept/
---
## RevisionCollection.Accept method

Akzeptiert Revisionen, die den angegebenen Kriterien entsprechen.

```csharp
public int Accept(IRevisionCriteria criteria)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| criteria | IRevisionCriteria | Die[`IRevisionCriteria`](../../irevisioncriteria/) Implementierung. |

### Rückgabewert

Die Anzahl der akzeptierten Revisionen.

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

* interface [IRevisionCriteria](../../irevisioncriteria/)
* class [RevisionCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
