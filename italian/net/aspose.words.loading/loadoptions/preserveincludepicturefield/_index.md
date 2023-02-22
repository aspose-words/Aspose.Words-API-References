---
title: LoadOptions.PreserveIncludePictureField
second_title: Aspose.Words per .NET API Reference
description: LoadOptions proprietà. Ottiene o imposta se mantenere il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è false.
type: docs
weight: 120
url: /it/net/aspose.words.loading/loadoptions/preserveincludepicturefield/
---
## LoadOptions.PreserveIncludePictureField property

Ottiene o imposta se mantenere il campo INCLUDEPICTURE durante la lettura dei formati Microsoft Word. Il valore predefinito è false.

```csharp
public bool PreserveIncludePictureField { get; set; }
```

### Osservazioni

Per impostazione predefinita, il campo INCLUDEPICTURE viene convertito in un oggetto forma. Puoi ignorarlo se hai bisogno di il campo da conservare, ad esempio, se desideri aggiornarlo a livello di codice. Si noti tuttavia che questo approccio non è comune per Aspose.Words. Usalo a tuo rischio.

Uno dei possibili casi d'uso potrebbe essere l'utilizzo di un MERGEFIELD come campo figlio per modificare dinamicamente il percorso di origine dell'immagine. In questo caso è necessario che INCLUDEPICTURE sia conservata nel modello.

### Esempi

Mostra come conservare o eliminare i campi INCLUDEPICTURE durante il caricamento di un documento.

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
    // in forme immagine durante il caricamento di un documento che le contiene.
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
* spazio dei nomi [Aspose.Words.Loading](../../loadoptions/)
* assemblea [Aspose.Words](../../../)


