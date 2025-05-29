---
title: Document.StartTrackRevisions
linktitle: StartTrackRevisions
articleTitle: StartTrackRevisions
second_title: Aspose.Words pour .NET
description: Suivez facilement les modifications apportées à vos documents grâce à la méthode StartTrackRevisions. Marquez automatiquement toutes les modifications comme des révisions pour une collaboration fluide et une clarté accrue.
type: docs
weight: 760
url: /fr/net/aspose.words/document/starttrackrevisions/
---
## StartTrackRevisions(*string, DateTime*) {#starttrackrevisions_1}

Commence à marquer automatiquement toutes les modifications ultérieures que vous apportez au document par programmation comme des modifications de révision.

```csharp
public void StartTrackRevisions(string author, DateTime dateTime)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| author | String | Initiales de l'auteur à utiliser pour les révisions. |
| dateTime | DateTime | La date et l'heure à utiliser pour les révisions. |

## Remarques

Si vous appelez cette méthode et apportez ensuite des modifications au document par programmation, enregistrez le document et ouvrez-le ultérieurement dans MS Word, vous verrez ces modifications comme des révisions.

Actuellement, Aspose.Words ne prend en charge que le suivi des insertions et des suppressions de nœuds. Les modifications de formatage ne sont pas enregistrées comme des révisions.

Le suivi automatique des modifications est pris en charge à la fois lors de la modification de ce document via des manipulations de nœuds ainsi que lors de l'utilisation[`DocumentBuilder`](../../documentbuilder/)

Cette méthode ne change pas la[`TrackRevisions`](../trackrevisions/) option et n'utilise pas sa valeur à des fins de suivi des révisions.

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## StartTrackRevisions(*string*) {#starttrackrevisions}

Commence à marquer automatiquement toutes les modifications ultérieures que vous apportez au document par programmation comme des modifications de révision.

```csharp
public void StartTrackRevisions(string author)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| author | String | Initiales de l'auteur à utiliser pour les révisions. |

## Remarques

Si vous appelez cette méthode et apportez ensuite des modifications au document par programmation, enregistrez le document et ouvrez-le ultérieurement dans MS Word, vous verrez ces modifications comme des révisions.

Actuellement, Aspose.Words ne prend en charge que le suivi des insertions et des suppressions de nœuds. Les modifications de formatage ne sont pas enregistrées comme des révisions.

Le suivi automatique des modifications est pris en charge à la fois lors de la modification de ce document via des manipulations de nœuds ainsi que lors de l'utilisation[`DocumentBuilder`](../../documentbuilder/)

Cette méthode ne change pas la[`TrackRevisions`](../trackrevisions/) option et n'utilise pas sa valeur à des fins de suivi des révisions.

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

* method [StopTrackRevisions](../stoptrackrevisions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
