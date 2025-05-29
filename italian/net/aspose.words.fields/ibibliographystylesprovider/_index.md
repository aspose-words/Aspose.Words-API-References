---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: Aspose.Words per .NET
description: Migliora la formattazione dei tuoi documenti con l'interfaccia Aspose.Words.IBibliographyStylesProvider, perfetta per personalizzare gli stili bibliografici nelle citazioni.
type: docs
weight: 3080
url: /it/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

Implementa questa interfaccia per fornire uno stile bibliografico per [`FieldBibliography`](../fieldbibliography/) E[`FieldCitation`](../fieldcitation/) campi quando vengono aggiornati.

```csharp
public interface IBibliographyStylesProvider
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(*string*) | Restituisce lo stile della bibliografia. |

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

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
