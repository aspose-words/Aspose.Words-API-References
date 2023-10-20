---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
linktitle: IncludeTextboxesFootnotesEndnotesInStat
articleTitle: IncludeTextboxesFootnotesEndnotesInStat
second_title: Aspose.Words pour .NET
description: Document IncludeTextboxesFootnotesEndnotesInStat propriété. Spécifie sil faut inclure des zones de texte des notes de bas de page et des notes de fin dans les statistiques du nombre de mots en C#.
type: docs
weight: 220
url: /fr/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

Spécifie s'il faut inclure des zones de texte, des notes de bas de page et des notes de fin dans les statistiques du nombre de mots.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

## Exemples

Montre comment inclure ou exclure des zones de texte, des notes de bas de page et des notes de fin des statistiques du nombre de mots.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

// Par défaut, l'option est définie sur 'false'.
doc.UpdateWordCount();
// Les mots comptent sans zones de texte, notes de bas de page et notes de fin.
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Words);            

doc.IncludeTextboxesFootnotesEndnotesInStat = true;
doc.UpdateWordCount();
// Les mots comptent avec les zones de texte, les notes de bas de page et les notes de fin.
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
