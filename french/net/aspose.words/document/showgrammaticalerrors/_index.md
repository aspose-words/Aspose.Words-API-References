---
title: Document.ShowGrammaticalErrors
linktitle: ShowGrammaticalErrors
articleTitle: ShowGrammaticalErrors
second_title: Aspose.Words pour .NET
description: Contrôlez la visibilité des erreurs grammaticales dans votre document grâce à la propriété ShowGrammaticalErrors. Améliorez la clarté et le professionnalisme de votre rédaction sans effort.
type: docs
weight: 410
url: /fr/net/aspose.words/document/showgrammaticalerrors/
---
## Document.ShowGrammaticalErrors property

Spécifie s'il faut afficher les erreurs de grammaire dans ce document.

```csharp
public bool ShowGrammaticalErrors { get; set; }
```

## Exemples

Montre comment afficher/masquer les erreurs dans le document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer deux phrases contenant des erreurs qui seraient relevées
// par les correcteurs d'orthographe et de grammaire de Microsoft Word.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// Si ces options sont activées, les fautes d'orthographe seront soulignées
// dans le document de sortie par une ligne rouge dentelée, et une double ligne bleue mettra en évidence les erreurs grammaticales.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
