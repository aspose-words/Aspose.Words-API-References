---
title: SaveOptions.UpdateLastSavedTimeProperty
linktitle: UpdateLastSavedTimeProperty
articleTitle: UpdateLastSavedTimeProperty
second_title: Aspose.Words per .NET
description: Ottimizza le tue SaveOptions con la proprietà UpdateLastSavedTime. Controlla gli aggiornamenti di LastSavedTime per una gestione efficiente dei dati e prestazioni migliori.
type: docs
weight: 190
url: /it/net/aspose.words.saving/saveoptions/updatelastsavedtimeproperty/
---
## SaveOptions.UpdateLastSavedTimeProperty property

Ottiene o imposta un valore che determina se il[`LastSavedTime`](../../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la proprietà viene aggiornata prima del salvataggio.

```csharp
public bool UpdateLastSavedTimeProperty { get; set; }
```

## Esempi

Mostra come stabilire se conservare la proprietà "Ultimo salvataggio" del documento durante il salvataggio.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
    doc.BuiltInDocumentProperties.LastSavedTime);

// Quando salviamo il documento in un formato OOXML, possiamo creare un oggetto OoxmlSaveOptions
// e quindi passarlo al metodo di salvataggio del documento per modificare il modo in cui salviamo il documento.
// Imposta la proprietà "UpdateLastSavedTimeProperty" su "true" per
// imposta la proprietà incorporata "Ultimo salvataggio" del documento di output sulla data/ora corrente.
// Imposta la proprietà "UpdateLastSavedTimeProperty" su "false" per
// conserva il valore originale della proprietà incorporata "Ultimo salvataggio" del documento di input.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx");
DateTime lastSavedTimeNew = doc.BuiltInDocumentProperties.LastSavedTime;

if (updateLastSavedTimeProperty)
    Assert.IsTrue((DateTime.Now - lastSavedTimeNew).Days < 1);
else
    Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
        lastSavedTimeNew);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
