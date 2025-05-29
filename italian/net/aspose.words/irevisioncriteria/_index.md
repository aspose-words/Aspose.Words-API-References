---
title: IRevisionCriteria Interface
linktitle: IRevisionCriteria
articleTitle: IRevisionCriteria
second_title: Aspose.Words per .NET
description: Gestisci le revisioni dei documenti senza sforzo con Aspose.Words.IRevisionCriteria. Personalizza l'accettazione e il rifiuto delle modifiche per una gestione precisa dei documenti.
type: docs
weight: 3650
url: /it/net/aspose.words/irevisioncriteria/
---
## IRevisionCriteria interface

Implementa questa interfaccia se vuoi controllare quando determinati[`Revision`](../revision/) dovrebbe essere accettato/rifiutato o no dal[`Accept`](../revisioncollection/accept/)/[`Reject`](../revisioncollection/reject/) metodi.

```csharp
public interface IRevisionCriteria
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [IsMatch](../../aspose.words/irevisioncriteria/ismatch/)(*[Revision](../revision/)*) | Controlla se specificato o meno*revision* corrisponde ai criteri. |

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
