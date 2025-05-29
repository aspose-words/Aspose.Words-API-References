---
title: IRevisionCriteria.IsMatch
linktitle: IsMatch
articleTitle: IsMatch
second_title: Aspose.Words per .NET
description: Scopri come il metodo IRevisionCriteria IsMatch verifica in modo efficace se una specifica revisione è in linea con i tuoi criteri per risultati ottimali.
type: docs
weight: 10
url: /it/net/aspose.words/irevisioncriteria/ismatch/
---
## IRevisionCriteria.IsMatch method

Controlla se specificato o meno*revision* corrisponde ai criteri.

```csharp
public bool IsMatch(Revision revision)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| revision | Revision | IL[`Revision`](../../revision/) istanza per soddisfare i criteri. |

### Valore di ritorno

`VERO` se il*revision* corrisponde ai criteri, altrimenti`Falso`.

## Osservazioni

L'implementazione del metodo non dovrebbe accettare/rifiutare la revisione o modificarla in alcun modo a causa di risultati inaspettati.

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

* class [Revision](../../revision/)
* interface [IRevisionCriteria](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
