---
title: RevisionGroupCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words für .NET
description: RevisionGroupCollection GetEnumerator methode. Gibt ein Enumeratorobjekt zurück in C#.
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

// Diese Sammlung selbst verfügt über eine Sammlung von Revisionsgruppen.
// Jede Gruppe ist eine Folge benachbarter Revisionen.
Console.WriteLine($"{revisions.Groups.Count} revision groups:");

// Durchlaufen Sie die Sammlung von Gruppen und geben Sie den Text aus, den die Überarbeitung betrifft.
using (IEnumerator<RevisionGroup> e = revisions.Groups.GetEnumerator())
{
    while (e.MoveNext())
    {
        Console.WriteLine($"\tGroup type \"{e.Current.RevisionType}\", " +
                          $"author: {e.Current.Author}, contents: [{e.Current.Text.Trim()}]");
    }
}

// Jeder Lauf, auf den sich eine Revision auswirkt, erhält ein entsprechendes Revisionsobjekt.
// Die Sammlung der Revisionen ist erheblich größer als die oben gedruckte komprimierte Form.
// abhängig davon, in wie viele Durchläufe wir das Dokument während der Microsoft Word-Bearbeitung segmentiert haben.
Console.WriteLine($"\n{revisions.Count} revisions:");

using (IEnumerator<Revision> e = revisions.GetEnumerator())
{
    while (e.MoveNext())
    {
        // Ein StyleDefinitionChange wirkt sich ausschließlich auf Stile und nicht auf Dokumentknoten aus. Dies bedeutet den „ParentStyle“
        //-Eigenschaft wird immer verwendet, während der ParentNode immer null ist.
        // Da sich alle anderen Änderungen auf Knoten auswirken, wird umgekehrt ParentNode verwendet und ParentStyle ist null.
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

// Alle Überarbeitungen über die Sammlung ablehnen und das Dokument in seine ursprüngliche Form zurückversetzen.
revisions.RejectAll();

Assert.AreEqual(0, revisions.Count);
```

### Siehe auch

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
