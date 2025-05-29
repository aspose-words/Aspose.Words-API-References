---
title: SaveOptions.UpdateCreatedTimeProperty
linktitle: UpdateCreatedTimeProperty
articleTitle: UpdateCreatedTimeProperty
second_title: Aspose.Words per .NET
description: Ottimizza le tue SaveOptions con la proprietà UpdateCreatedTime. Controlla gli aggiornamenti di CreatedTime prima del salvataggio, migliorando l'accuratezza dei dati. Valore predefinito: false.
type: docs
weight: 160
url: /it/net/aspose.words.saving/saveoptions/updatecreatedtimeproperty/
---
## SaveOptions.UpdateCreatedTimeProperty property

Ottiene o imposta un valore che determina se il[`CreatedTime`](../../../aspose.words.properties/builtindocumentproperties/createdtime/) la proprietà viene aggiornata prima del salvataggio. Il valore predefinito è`falso` ;

```csharp
public bool UpdateCreatedTimeProperty { get; set; }
```

## Esempi

Mostra come aggiornare la proprietà "CreatedTime" di un documento durante il salvataggio.

```csharp
Document doc = new Document();

DateTime createdTime = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.CreatedTime = createdTime;

// Questo flag determina se l'ora di creazione, che è una proprietà incorporata, viene aggiornata.
// In tal caso, la data dell'operazione di salvataggio più recente del documento
// con questo oggetto SaveOptions passato come parametro viene utilizzato come ora di creazione.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Aprire il documento salvato, quindi verificare il valore della proprietà.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
    Assert.AreNotEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
else
    Assert.AreEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
```

### Guarda anche

* class [SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
