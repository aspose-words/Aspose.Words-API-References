---
title: TabStop.IsClear
linktitle: IsClear
articleTitle: IsClear
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété TabStop IsClear améliore votre interface utilisateur en garantissant une gestion transparente des onglets, en effaçant les arrêts existants pour une expérience utilisateur plus fluide.
type: docs
weight: 30
url: /fr/net/aspose.words/tabstop/isclear/
---
## TabStop.IsClear property

Retours`vrai` si ce taquet de tabulation efface tous les taquets de tabulation existants dans cette position.

```csharp
public bool IsClear { get; }
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

* class [TabStop](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
