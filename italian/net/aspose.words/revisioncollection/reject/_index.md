---
title: RevisionCollection.Reject
linktitle: Reject
articleTitle: Reject
second_title: Aspose.Words per .NET
description: Scopri il metodo RevisionCollection Reject per filtrare in modo efficiente le revisioni indesiderate in base ai tuoi criteri per una gestione semplificata del progetto.
type: docs
weight: 70
url: /it/net/aspose.words/revisioncollection/reject/
---
## RevisionCollection.Reject method

Rifiuta le revisioni che corrispondono ai criteri specificati.

```csharp
public int Reject(IRevisionCriteria criteria)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| criteria | IRevisionCriteria | Il[`IRevisionCriteria`](../../irevisioncriteria/) implementazione. |

### Valore di ritorno

Il numero di revisioni rifiutate.

## Esempi

Mostra come accettare o rifiutare la revisione in base ai criteri.

```csharp
public void RevisionSpecifiedCriteria()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Write("This does not count as a revision. ");

    // Per registrare le nostre modifiche come revisioni, dobbiamo dichiarare un autore e poi iniziare a monitorarle.
    doc.StartTrackRevisions("John Doe", DateTime.Now);
    builder.Write("This is insertion revision #1. ");
    doc.StopTrackRevisions();

    doc.StartTrackRevisions("Jane Doe", DateTime.Now);
    builder.Write("This is insertion revision #2. ");
    // Rimuovi una frase "Questo non conta come una revisione".
    doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();
    doc.StopTrackRevisions();

    Assert.AreEqual(3, doc.Revisions.Count);
    // Abbiamo due revisioni di autori diversi, quindi dobbiamo accettarne solo una.
    doc.Revisions.Accept(new RevisionCriteria("John Doe", RevisionType.Insertion));
    Assert.AreEqual(2, doc.Revisions.Count);
    // Rifiuta la revisione con nome autore e tipo di revisione diversi.
    doc.Revisions.Reject(new RevisionCriteria("Jane Doe", RevisionType.Deletion));
    Assert.AreEqual(1, doc.Revisions.Count);

    doc.Save(ArtifactsDir + "Revision.RevisionSpecifiedCriteria.docx");
}

/// <summary>
/// Controlla quando una determinata revisione deve essere accettata/rifiutata.
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

### Guarda anche

* interface [IRevisionCriteria](../../irevisioncriteria/)
* class [RevisionCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
