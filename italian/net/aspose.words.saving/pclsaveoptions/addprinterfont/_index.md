---
title: PclSaveOptions.AddPrinterFont
linktitle: AddPrinterFont
articleTitle: AddPrinterFont
second_title: Aspose.Words per .NET
description: PclSaveOptions AddPrinterFont metodo. Aggiunge informazioni sul carattere caricato sulla stampante dal produttore in C#.
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
| fontFullName | String | Nome completo del carattere (ad esempio "Times New Roman Bold Italic"). |
| fontPclName | String | Nome del carattere utilizzato nel documento Pcl. |

## Osservazioni

Ci sono 52 caratteri che devono essere integrati in qualsiasi stampante secondo le specifiche Pcl. Tuttavia i produttori possono aggiungere altri caratteri ai propri dispositivi.

## Esempi

Mostra come fare in modo che una stampante sostituisca tutte le istanze di un carattere specifico con un carattere diverso.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// Quando si stampa questo documento, la stampante utilizzerà il carattere "Courier New".
// per accedere ai luoghi in cui il nostro documento utilizzava il carattere "Courier".
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### Guarda anche

* class [PclSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
