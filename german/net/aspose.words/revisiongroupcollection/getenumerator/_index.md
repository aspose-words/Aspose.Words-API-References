---
title: RevisionGroupCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words für .NET
description: Entdecken Sie die GetEnumerator-Methode von RevisionGroupCollection – rufen Sie Enumerator-Objekte effizient ab, um die Datenverwaltung zu optimieren und die Leistung zu verbessern.
type: docs
weight: 30
url: /de/net/aspose.words/revisiongroupcollection/getenumerator/
---
## RevisionGroupCollection.GetEnumerator method

Gibt ein Enumeratorobjekt zurück.

```csharp
public IEnumerator<RevisionGroup> GetEnumerator()
```

## Beispiele

Zeigt, wie mit der Revisionssammlung eines Dokuments gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");
RevisionCollection revisions = doc.Revisions;

// Diese Sammlung selbst enthält eine Sammlung von Revisionsgruppen.
// Jede Gruppe ist eine Folge benachbarter Revisionen.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// Durchlaufen Sie die Sammlung von Gruppen und drucken Sie den Text, der von der Revision betroffen ist.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// Jeder Lauf, der von einer Revision betroffen ist, erhält ein entsprechendes Revisionsobjekt.
// Die Sammlung der Revisionen ist erheblich umfangreicher als die oben abgedruckte Kurzfassung.
// abhängig davon, in wie viele Läufe wir das Dokument während der Bearbeitung in Microsoft Word segmentiert haben.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // Ein StyleDefinitionChange betrifft ausschließlich Stile und nicht Dokumentknoten. Dies bedeutet, dass der "ParentStyle"
        // Die Eigenschaft wird immer verwendet, während ParentNode immer null ist.
        // Da alle anderen Änderungen Knoten betreffen, wird ParentNode umgekehrt verwendet und ParentStyle ist null.
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

// Alle Revisionen über die Sammlung ablehnen und das Dokument in seine ursprüngliche Form zurückversetzen.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### Siehe auch

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
