---
title: Document.StopTrackRevisions
second_title: Référence de l'API Aspose.Words pour .NET
description: Document méthode. Arrête le marquage automatique des modifications du document en tant que révisions.
type: docs
weight: 740
url: /fr/net/aspose.words/document/stoptrackrevisions/
---
## Document.StopTrackRevisions method

Arrête le marquage automatique des modifications du document en tant que révisions.

```csharp
public void StopTrackRevisions()
```

### Exemples

Montre comment suivre les révisions lors de la modification d’un document.

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
Assert.That(doc.Revisions[0].DateTime, Is.EqualTo(DateTime.Now).Within(10).Milliseconds);

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
// en appelant des méthodes telles que Document.AcceptAllRevisions ou la méthode Accept de chaque révision.
// Dans Microsoft Word, nous pouvons les traiter manuellement via "Révision" -> "Changements".
doc.Save(ArtifactsDir + "Document.StartTrackRevisions.docx");
```

### Voir également

* method [StartTrackRevisions](../starttrackrevisions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


