---
title: RevisionCollection.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words para .NET
description: Descubra el método Accept de RevisionCollection para administrar y filtrar fácilmente las revisiones según sus criterios para optimizar las actualizaciones del proyecto.
type: docs
weight: 40
url: /es/net/aspose.words/revisioncollection/accept/
---
## RevisionCollection.Accept method

Acepta revisiones que coinciden con los criterios especificados.

```csharp
public int Accept(IRevisionCriteria criteria)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| criteria | IRevisionCriteria | El[`IRevisionCriteria`](../../irevisioncriteria/) implementación. |

### Valor_devuelto

El recuento de revisiones aceptadas.

## Ejemplos

Muestra cómo aceptar o rechazar una revisión según criterios.

```csharp
public void RevisionSpecifiedCriteria()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Write("This does not count as a revision. ");

    // Para registrar nuestras ediciones como revisiones, necesitamos declarar un autor y luego comenzar a rastrearlas.
    doc.StartTrackRevisions("John Doe", DateTime.Now);
    builder.Write("This is insertion revision #1. ");
    doc.StopTrackRevisions();

    doc.StartTrackRevisions("Jane Doe", DateTime.Now);
    builder.Write("This is insertion revision #2. ");
    // Eliminar una ejecución "Esto no cuenta como una revisión".
    doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();
    doc.StopTrackRevisions();

    Assert.AreEqual(3, doc.Revisions.Count);
    Tenemos dos revisiones de diferentes autores, por lo que debemos aceptar solo una.
    doc.Revisions.Accept(new RevisionCriteria("John Doe", RevisionType.Insertion));
    Assert.AreEqual(2, doc.Revisions.Count);
    // Rechazar revisión con diferente nombre de autor y tipo de revisión.
    doc.Revisions.Reject(new RevisionCriteria("Jane Doe", RevisionType.Deletion));
    Assert.AreEqual(1, doc.Revisions.Count);

    doc.Save(ArtifactsDir + "Revision.RevisionSpecifiedCriteria.docx");
}

/// <summary>
/// Controlar cuándo se debe aceptar/rechazar determinada revisión.
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

### Ver también

* interface [IRevisionCriteria](../../irevisioncriteria/)
* class [RevisionCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
