---
title: Document.AcceptAllRevisions
second_title: Référence de l'API Aspose.Words pour .NET
description: Document méthode. Accepte toutes les modifications suivies dans le document.
type: docs
weight: 520
url: /fr/net/aspose.words/document/acceptallrevisions/
---
## Document.AcceptAllRevisions method

Accepte toutes les modifications suivies dans le document.

```csharp
public void AcceptAllRevisions()
```

### Remarques

Cette méthode est un raccourci pour[`AcceptAll`](../../revisioncollection/acceptall/).

### Exemples

Montre comment accepter toutes les modifications de suivi dans le document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifiez le document tout en suivant les modifications pour créer quelques révisions.
doc.StartTrackRevisions("John Doe");
builder.Write("Hello world! ");
builder.Write("Hello again! "); 
builder.Write("This is another revision.");
doc.StopTrackRevisions();

Assert.AreEqual(3, doc.Revisions.Count);

// Nous pouvons parcourir chaque révision et l'accepter/rejeter dans le cadre de notre document.
// Si nous savons que nous souhaitons accepter chaque révision, nous pouvons le faire plus simplement en appelant cette méthode.
doc.AcceptAllRevisions();

Assert.AreEqual(0, doc.Revisions.Count);
Assert.AreEqual("Hello world! Hello again! This is another revision.", doc.GetText().Trim());
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


