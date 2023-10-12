---
title: ImportFormatOptions.AdjustSentenceAndWordSpacing
second_title: Référence de l'API Aspose.Words pour .NET
description: ImportFormatOptions propriété. Obtient ou définit une valeur booléenne qui spécifie sil faut ajuster automatiquement lespacement des phrases et des mots. La valeur par défaut estFAUX .
type: docs
weight: 20
url: /fr/net/aspose.words/importformatoptions/adjustsentenceandwordspacing/
---
## ImportFormatOptions.AdjustSentenceAndWordSpacing property

Obtient ou définit une valeur booléenne qui spécifie s'il faut ajuster automatiquement l'espacement des phrases et des mots. La valeur par défaut est`FAUX` .

```csharp
public bool AdjustSentenceAndWordSpacing { get; set; }
```

### Exemples

Montre comment ajuster automatiquement l’espacement des phrases et des mots.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(srcDoc);
builder.Write("Dolor sit amet.");

builder = new DocumentBuilder(dstDoc);
builder.Write("Lorem ipsum.");

ImportFormatOptions options = new ImportFormatOptions() { AdjustSentenceAndWordSpacing = true };
builder.InsertDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

Assert.AreEqual("Lorem ipsum. Dolor sit amet.", dstDoc.FirstSection.Body.FirstParagraph.GetText().Trim());
```

### Voir également

* class [ImportFormatOptions](../)
* espace de noms [Aspose.Words](../../importformatoptions/)
* Assemblée [Aspose.Words](../../../)


