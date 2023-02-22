---
title: PclSaveOptions.AddPrinterFont
second_title: Aspose.Words per .NET API Reference
description: PclSaveOptions metodo. Aggiunge informazioni sul carattere caricato sulla stampante dal produttore.
type: docs
weight: 50
url: /it/net/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions.AddPrinterFont method

Aggiunge informazioni sul carattere caricato sulla stampante dal produttore.

```csharp
public void AddPrinterFont(string fontFullName, string fontPclName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fontFullName | String | Nome completo del carattere (es. "Times New Roman Bold Italic"). |
| fontPclName | String | Nome del carattere utilizzato nel documento Pcl. |

### Osservazioni

Ci sono 52 font che devono essere costruiti in qualsiasi stampante secondo la specifica Pcl. Tuttavia i produttori possono aggiungere altri font ai loro dispositivi.

### Esempi

Mostra come fare in modo che una stampante sostituisca tutte le istanze di un font specifico con un font diverso.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// Durante la stampa di questo documento, la stampante utilizzerà il carattere "Courier New".
// per accedere ai luoghi in cui il nostro documento utilizzava il carattere "Corriere".
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### Guarda anche

* class [PclSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../pclsaveoptions/)
* assemblea [Aspose.Words](../../../)


