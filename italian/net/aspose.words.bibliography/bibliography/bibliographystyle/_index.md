---
title: Bibliography.BibliographyStyle
linktitle: BibliographyStyle
articleTitle: BibliographyStyle
second_title: Aspose.Words per .NET
description: Scopri la proprietà BibliographyStyle: gestisci e personalizza facilmente lo stile attivo della tua bibliografia per una migliore organizzazione e presentazione.
type: docs
weight: 10
url: /it/net/aspose.words.bibliography/bibliography/bibliographystyle/
---
## Bibliography.BibliographyStyle property

Ottiene o imposta una stringa che rappresenta il nome dello stile attivo da utilizzare per una bibliografia.

```csharp
public string BibliographyStyle { get; set; }
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

* class [Bibliography](../)
* spazio dei nomi [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* assemblea [Aspose.Words](../../../)
