---
title: Paragraph.IsDeleteRevision
linktitle: IsDeleteRevision
articleTitle: IsDeleteRevision
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IsDeleteRevision dans Microsoft Word. Découvrez comment elle indique les suppressions lors du suivi des modifications pour une gestion efficace des documents.
type: docs
weight: 40
url: /fr/net/aspose.words/paragraph/isdeleterevision/
---
## Paragraph.IsDeleteRevision property

Renvoie vrai si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé.

```csharp
public bool IsDeleteRevision { get; }
```

## Exemples

Montre comment travailler avec les paragraphes de révision.

```csharp
Document doc = new Document();
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2. ");
body.AppendParagraph("Paragraph 3. ");

// Les paragraphes ci-dessus ne sont pas des révisions.
// Les paragraphes que nous ajoutons après le démarrage du suivi des révisions seront enregistrés comme des révisions « Insérer ».
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.True(para.IsInsertRevision);

// Les paragraphes que nous supprimons après le démarrage du suivi des révisions seront enregistrés comme des révisions « Supprimer ».
ParagraphCollection paragraphs = body.Paragraphs;

Assert.AreEqual(4, paragraphs.Count);

para = paragraphs[2];
para.Remove();

// Ces paragraphes resteront en place jusqu'à ce que nous acceptions ou rejetions la révision de suppression.
// L'acceptation de la révision supprimera définitivement le paragraphe,
// et rejeter la révision la laissera dans le document comme si nous ne l'avions jamais supprimée.
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// Acceptez la révision, puis vérifiez que le paragraphe a disparu.
doc.AcceptAllRevisions();

Assert.AreEqual(3, paragraphs.Count);
Assert.AreEqual(0, para.Count);
Assert.AreEqual(
    "Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4.", doc.GetText().Trim());
```

### Voir également

* class [Paragraph](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
