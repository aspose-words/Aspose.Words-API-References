---
title: FieldOptions.BibliographyStylesProvider
linktitle: BibliographyStylesProvider
articleTitle: BibliographyStylesProvider
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldOptions BibliographyStylesProvider per stili bibliografici personalizzabili, migliorando i tuoi campi FieldBibliography e FieldCitation.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldoptions/bibliographystylesprovider/
---
## FieldOptions.BibliographyStylesProvider property

Ottiene o imposta un provider che restituisce uno stile bibliografico per [`FieldBibliography`](../../fieldbibliography/) E[`FieldCitation`](../../fieldcitation/) campi.

```csharp
public IBibliographyStylesProvider BibliographyStylesProvider { get; set; }
```

## Esempi

Mostra come sovrascrivere gli stili predefiniti o fornirne di personalizzati.

```csharp
public void ChangeBibliographyStyles()
{
    Document doc = new Document(MyDir + "Bibliography.docx");

    // Se il documento ha già uno stile, puoi modificarlo con il seguente codice:
    // doc.Bibliography.BibliographyStyle = "Stile personalizzato bibliografia.xsl";

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
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
