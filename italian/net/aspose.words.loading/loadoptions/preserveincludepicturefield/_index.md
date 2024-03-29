---
title: LoadOptions.PreserveIncludePictureField
linktitle: PreserveIncludePictureField
articleTitle: PreserveIncludePictureField
second_title: Aspose.Words per .NET
description: LoadOptions PreserveIncludePictureField proprietà. Ottiene o imposta se preservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito èfalso  in C#.
type: docs
weight: 120
url: /it/net/aspose.words.loading/loadoptions/preserveincludepicturefield/
---
## LoadOptions.PreserveIncludePictureField property

Ottiene o imposta se preservare il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è`falso` .

```csharp
public bool PreserveIncludePictureField { get; set; }
```

## Osservazioni

Per impostazione predefinita, il campo INCLUDEPICTURE viene convertito in un oggetto forma. Puoi sovrascriverlo se hai bisogno che il campo venga preservato, ad esempio, se desideri aggiornarlo a livello di codice. Si noti tuttavia che l'approccio this non è comune per Aspose.Words. Usalo a tuo rischio e pericolo.

Uno dei possibili casi d'uso potrebbe essere l'utilizzo di un MERGEFIELD come campo figlio per modificare dinamicamente il percorso di origine dell'immagine. In questo caso è necessario che INCLUDEPICTURE sia preservato nel modello.

## Esempi

Mostra come preservare o eliminare i campi INCLUDEPICTURE durante il caricamento di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // Possiamo impostare un flag in un oggetto LoadOptions per decidere se convertire tutti i campi INCLUDEPICTURE
    // nelle forme dell'immagine quando si carica un documento che le contiene.
    LoadOptions loadOptions = new LoadOptions
    {
        PreserveIncludePictureField = preserveIncludePictureField
    };

    doc = new Document(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        Assert.True(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));

        doc.UpdateFields();
        doc.Save(ArtifactsDir + "Field.PreserveIncludePicture.docx");
    }
    else
    {
        Assert.False(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));
    }
}
```

### Guarda anche

* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
