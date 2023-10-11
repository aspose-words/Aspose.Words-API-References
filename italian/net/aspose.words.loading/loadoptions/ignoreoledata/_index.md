---
title: LoadOptions.IgnoreOleData
second_title: Aspose.Words per .NET API Reference
description: LoadOptions proprietà. Specifica se ignorare i dati OLE.
type: docs
weight: 70
url: /it/net/aspose.words.loading/loadoptions/ignoreoledata/
---
## LoadOptions.IgnoreOleData property

Specifica se ignorare i dati OLE.

```csharp
public bool IgnoreOleData { get; set; }
```

### Osservazioni

Ignorare i dati OLE può ridurre il consumo di memoria e aumentare le prestazioni senza perdita di dati nel caso in cui il formato di destinazione non supporti gli oggetti OLE.

Il valore predefinito è`falso`.

### Esempi

Mostra come inserire dati OLE durante il caricamento.

```csharp
// Ignorare i dati OLE può ridurre il consumo di memoria e aumentare le prestazioni
// senza perdita di dati nel caso in cui il formato di destinazione non supporti gli oggetti OLE.
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Document doc = new Document(MyDir + "OLE objects.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.IgnoreOleData.docx");
```

### Guarda anche

* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../loadoptions/)
* assemblea [Aspose.Words](../../../)


