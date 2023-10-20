---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: Aspose.Words per .NET
description: Aspose.Words.Fields.IBibliographyStylesProvider interfaccia. Implementa questa interfaccia per fornire uno stile bibliografico per ilFieldBibliography EFieldCitation campi quando vengono aggiornati in C#.
type: docs
weight: 2670
url: /it/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

Implementa questa interfaccia per fornire uno stile bibliografico per il[`FieldBibliography`](../fieldbibliography/) E[`FieldCitation`](../fieldcitation/) campi quando vengono aggiornati.

```csharp
public interface IBibliographyStylesProvider
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(*string*) | Restituisce lo stile della bibliografia. |

## Esempi

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

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
