---
title: Document.StopTrackRevisions
linktitle: StopTrackRevisions
articleTitle: StopTrackRevisions
second_title: Aspose.Words pour .NET
description: Apprenez à utiliser la méthode StopTrackRevisions pour empêcher les marquages automatiques de modification de document, améliorant ainsi l'efficacité de votre édition et la clarté de votre document.
type: docs
weight: 770
url: /fr/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

Arrête le marquage automatique des modifications du document comme des révisions.

```csharp
public void StopTrackRevisions()
```

## Exemples

Montre comment suivre les révisions lors de l'édition d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// La modification d'un document ne compte généralement pas comme une révision jusqu'à ce que nous commencions à le suivre.
builder.Write("Hello world! ");

Assert.AreEqual(0, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[0].IsInsertRevision);

doc.StartTrackRevisions("John Doe");

builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.True(doc.FirstSection.Body.Paragraphs[0].Runs[1].IsInsertRevision);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
Assert.IsTrue((DateTime.Now - doc.Revisions[0].DateTime).Milliseconds <= 10);

// Arrêtez de suivre les révisions pour ne pas compter les modifications futures comme des révisions.
doc.StopTrackRevisions();
builder.Write("Hello again! ");

Assert.AreEqual(1, doc.Revisions.Count);
Assert.False(doc.FirstSection.Body.Paragraphs[0].Runs[2].IsInsertRevision);

// La création de révisions leur donne une date et une heure de l'opération.
// Nous pouvons désactiver cela en passant DateTime.MinValue lorsque nous commençons à suivre les révisions.
doc.StartTrackRevisions("John Doe", DateTime.MinValue);
builder.Write("Hello again! ");

Assert.AreEqual(2, doc.Revisions.Count);
Assert.AreEqual("John Doe", doc.Revisions[1].Author);
Assert.AreEqual(DateTime.MinValue, doc.Revisions[1].DateTime);

// Nous pouvons accepter/rejeter ces révisions par programmation
// en appelant des méthodes telles que Document.AcceptAllRevisions, ou la méthode Accept de chaque révision.
// Dans Microsoft Word, nous pouvons les traiter manuellement via « Révision » -> « Modifications ».
doc.Save(ArtifactsDir + "Revision.StartTrackRevisions.docx");
```

### Voir également

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
