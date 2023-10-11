---
title: FieldOptions.BibliographyStylesProvider
second_title: Aspose.Words per .NET API Reference
description: FieldOptions proprietà. Ottiene o imposta un provider che restituisce uno stile bibliografico per ilFieldBibliography EFieldCitation campi.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldoptions/bibliographystylesprovider/
---
## FieldOptions.BibliographyStylesProvider property

Ottiene o imposta un provider che restituisce uno stile bibliografico per il[`FieldBibliography`](../../fieldbibliography/) E[`FieldCitation`](../../fieldcitation/) campi.

```csharp
public IBibliographyStylesProvider BibliographyStylesProvider { get; set; }
```

### Esempi

Mostra come sovrascrivere gli stili integrati o fornirne uno personalizzato.

```csharp
public void ChangeBibliographyStyles()
{            
    Document doc = new Document(MyDir + "Bibliography.docx");

    doc.FieldOptions.BibliographyStylesProvider = new BibliographyStylesProvider();
    doc.UpdateFields();

    doc.Save(ArtifactsDir + "Field.ChangeBibliographyStyles.docx");
}

public class BibliographyStylesProvider : IBibliographyStylesProvider
{
    Stream IBibliographyStylesProvider.GetStyle(string styleFileName)
    {
        return File.OpenRead(MyDir + "Bibliography custom style.xsl");
    }
}
```

### Guarda anche

* interface [IBibliographyStylesProvider](../../ibibliographystylesprovider/)
* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldoptions/)
* assemblea [Aspose.Words](../../../)


