---
title: Document.ShowSpellingErrors
linktitle: ShowSpellingErrors
articleTitle: ShowSpellingErrors
second_title: Aspose.Words pour .NET
description: Document ShowSpellingErrors propriété. Spécifie sil faut afficher les fautes dorthographe dans ce document en C#.
type: docs
weight: 400
url: /fr/net/aspose.words/document/showspellingerrors/
---
## Document.ShowSpellingErrors property

Spécifie s'il faut afficher les fautes d'orthographe dans ce document.

```csharp
public bool ShowSpellingErrors { get; set; }
```

## Exemples

Montre comment afficher/masquer les erreurs dans le document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère deux phrases contenant des erreurs qui seront relevées
// par les vérificateurs orthographiques et grammaticaux de Microsoft Word.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// Si ces options sont activées, alors les fautes d'orthographe seront soulignées
// dans le document de sortie par une ligne rouge irrégulière et une double ligne bleue mettra en évidence les erreurs grammaticales.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
