---
title: TabStopCollection.Equals
linktitle: Equals
articleTitle: Equals
second_title: Aspose.Words pour .NET
description: Découvrez la méthode TabStopCollection Equals pour comparer facilement les TabStopCollections pour l'égalité, améliorant ainsi l'efficacité et la précision de votre codage.
type: docs
weight: 70
url: /fr/net/aspose.words/tabstopcollection/equals/
---
## Equals(*[TabStopCollection](../)*) {#equals}

Détermine si le spécifié[`TabStopCollection`](../) est égal en valeur au courant[`TabStopCollection`](../) .

```csharp
public bool Equals(TabStopCollection rhs)
```

## Exemples

Montre comment travailler avec la collection de taquets de tabulation d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 points correspondent à un « pouce » sur la règle de tabulation de Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Chaque caractère « tabulation » amène le curseur du constructeur à l'emplacement du prochain taquet de tabulation.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Chaque paragraphe obtient sa collection d'arrêts de tabulation, qui clone ses valeurs à partir de la collection d'arrêts de tabulation du générateur de documents.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Une collection d'arrêts de tabulation peut nous indiquer des arrêts de tabulation avant et après certaines positions.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Nous pouvons effacer la collection de tabulations d'un paragraphe pour revenir au comportement de tabulation par défaut.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Voir également

* class [TabStopCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Equals(*object*) {#equals_1}

Détermine si l'objet spécifié est égal en valeur à l'objet actuel.

```csharp
public override bool Equals(object obj)
```

## Exemples

Montre comment travailler avec la collection de taquets de tabulation d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TabStopCollection tabStops = builder.ParagraphFormat.TabStops;

// 72 points correspondent à un « pouce » sur la règle de tabulation de Microsoft Word.
tabStops.Add(new TabStop(72.0));
tabStops.Add(new TabStop(432.0, TabAlignment.Right, TabLeader.Dashes));

Assert.AreEqual(2, tabStops.Count);
Assert.IsFalse(tabStops[0].IsClear);
Assert.IsFalse(tabStops[0].Equals(tabStops[1]));

// Chaque caractère « tabulation » amène le curseur du constructeur à l'emplacement du prochain taquet de tabulation.
builder.Writeln("Start\tTab 1\tTab 2");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(2, paragraphs.Count);

// Chaque paragraphe obtient sa collection d'arrêts de tabulation, qui clone ses valeurs à partir de la collection d'arrêts de tabulation du générateur de documents.
Assert.AreEqual(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);
Assert.AreNotSame(paragraphs[0].ParagraphFormat.TabStops, paragraphs[1].ParagraphFormat.TabStops);

// Une collection d'arrêts de tabulation peut nous indiquer des arrêts de tabulation avant et après certaines positions.
Assert.AreEqual(72.0, tabStops.Before(100.0).Position);
Assert.AreEqual(432.0, tabStops.After(100.0).Position);

// Nous pouvons effacer la collection de tabulations d'un paragraphe pour revenir au comportement de tabulation par défaut.
paragraphs[1].ParagraphFormat.TabStops.Clear();

Assert.AreEqual(0, paragraphs[1].ParagraphFormat.TabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.TabStopCollection.docx");
```

### Voir également

* class [TabStopCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
