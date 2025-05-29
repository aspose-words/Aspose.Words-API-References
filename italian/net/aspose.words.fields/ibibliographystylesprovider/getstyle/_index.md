---
title: IBibliographyStylesProvider.GetStyle
linktitle: GetStyle
articleTitle: GetStyle
second_title: Aspose.Words per .NET
description: Scopri il metodo GetStyle di IBibliographyStylesProvider per recuperare e personalizzare senza sforzo gli stili della tua bibliografia per migliorare la tua scrittura accademica.
type: docs
weight: 10
url: /it/net/aspose.words.fields/ibibliographystylesprovider/getstyle/
---
## IBibliographyStylesProvider.GetStyle method

Restituisce lo stile della bibliografia.

```csharp
public Stream GetStyle(string styleFileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| styleFileName | String | Nome del file in stile bibliografico. |

### Valore di ritorno

ILStream con foglio di stile XSLT in stile bibliografico.

## Osservazioni

L'implementazione dovrebbe restituire`null` per indicare che deve essere utilizzata la versione MS Word dello stile specificato.

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

* interface [IBibliographyStylesProvider](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
