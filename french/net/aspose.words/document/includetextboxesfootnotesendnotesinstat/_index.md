---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
linktitle: IncludeTextboxesFootnotesEndnotesInStat
articleTitle: IncludeTextboxesFootnotesEndnotesInStat
second_title: Aspose.Words pour .NET
description: Optimisez le nombre de mots de votre document grâce à la propriété IncludeTextboxesFootnotesEndnotesInStat. Contrôlez facilement les zones de texte, les notes de bas de page et les notes de fin !
type: docs
weight: 230
url: /fr/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

Spécifie s'il faut inclure les zones de texte, les notes de bas de page et les notes de fin dans les statistiques de comptage de mots.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

## Exemples

Montre comment inclure ou exclure des zones de texte, des notes de bas de page et des notes de fin des statistiques de comptage de mots.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

// Par défaut, l'option est définie sur « false ».
doc.UpdateWordCount();
// Les mots comptent sans les zones de texte, les notes de bas de page et les notes de fin.
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
