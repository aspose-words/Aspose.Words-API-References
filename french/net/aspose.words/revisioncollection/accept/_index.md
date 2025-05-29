---
title: RevisionCollection.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words pour .NET
description: Découvrez la méthode RevisionCollection Accept pour gérer et filtrer facilement les révisions en fonction de vos critères pour des mises à jour de projet simplifiées.
type: docs
weight: 40
url: /fr/net/aspose.words/revisioncollection/accept/
---
## RevisionCollection.Accept method

Accepte les révisions qui correspondent aux critères spécifiés.

```csharp
public int Accept(IRevisionCriteria criteria)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| criteria | IRevisionCriteria | Le[`IRevisionCriteria`](../../irevisioncriteria/) implémentation. |

### Return_Value

Le nombre de révisions acceptées.

## Exemples

Montre comment accepter ou rejeter une révision en fonction de critères.

```csharp
public void RevisionSpecifiedCriteria()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Write("This does not count as a revision. ");

    // Pour enregistrer nos modifications en tant que révisions, nous devons déclarer un auteur, puis commencer à les suivre.
    doc.StartTrackRevisions("John Doe", DateTime.Now);
    builder.Write("This is insertion revision #1. ");
    doc.StopTrackRevisions();

    doc.StartTrackRevisions("Jane Doe", DateTime.Now);
    builder.Write("This is insertion revision #2. ");
    // Supprimer une exécution « Ceci ne compte pas comme une révision. ».
    doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();
    doc.StopTrackRevisions();

    Assert.AreEqual(3, doc.Revisions.Count);
    // Nous avons deux révisions d'auteurs différents, nous devons donc n'en accepter qu'une seule.
    doc.Revisions.Accept(new RevisionCriteria("John Doe", RevisionType.Insertion));
    Assert.AreEqual(2, doc.Revisions.Count);
    // Rejeter la révision avec un nom d'auteur et un type de révision différents.
    doc.Revisions.Reject(new RevisionCriteria("Jane Doe", RevisionType.Deletion));
    Assert.AreEqual(1, doc.Revisions.Count);

    doc.Save(ArtifactsDir + "Revision.RevisionSpecifiedCriteria.docx");
}

/// <summary>
/// Contrôlez quand certaines révisions doivent être acceptées/rejetées.
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

### Voir également

* interface [IRevisionCriteria](../../irevisioncriteria/)
* class [RevisionCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
