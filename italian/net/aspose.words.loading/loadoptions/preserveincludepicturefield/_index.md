---
title: LoadOptions.PreserveIncludePictureField
linktitle: PreserveIncludePictureField
articleTitle: PreserveIncludePictureField
second_title: Aspose.Words per .NET
description: Controlla il campo INCLUDEPICTURE nei formati Microsoft Word con LoadOptions PreserveIncludePictureField. Gestisci facilmente la formattazione dei documenti per risultati ottimali.
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

Per impostazione predefinita, il campo INCLUDEPICTURE viene convertito in un oggetto forma. È possibile ignorare questa impostazione se si desidera che il campo venga mantenuto, ad esempio se si desidera aggiornarlo a livello di codice. Si noti tuttavia che questo approccio non è comune per Aspose.Words. Utilizzatelo a vostro rischio e pericolo.

Uno dei possibili casi d'uso potrebbe essere l'utilizzo di un MERGEFIELD come campo figlio per modificare dinamicamente il percorso sorgente dell'immagine. In questo caso, è necessario che INCLUDEPICTURE venga mantenuto nel modello.

## Esempi

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
    // in forme di immagini quando si carica un documento che le contiene.
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
