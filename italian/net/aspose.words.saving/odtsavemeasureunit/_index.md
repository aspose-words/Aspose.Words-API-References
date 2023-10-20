---
title: OdtSaveMeasureUnit Enum
linktitle: OdtSaveMeasureUnit
articleTitle: OdtSaveMeasureUnit
second_title: Aspose.Words per .NET
description: Aspose.Words.Saving.OdtSaveMeasureUnit enum. Unità di misura specificate da applicare al contenuto misurabile del documento come forma larghezza e altro durante il salvataggio in C#.
type: docs
weight: 5320
url: /it/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

Unità di misura specificate da applicare al contenuto misurabile del documento come forma, larghezza e altro durante il salvataggio.

```csharp
public enum OdtSaveMeasureUnit
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Centimeters | `0` | Specifica che il contenuto del documento viene salvato utilizzando centimetri. |
| Inches | `1` | Specifica che il contenuto del documento viene salvato utilizzando pollici. |

## Esempi

Mostra come utilizzare diverse unità di misura per definire i parametri di stile di un documento ODT salvato.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Quando esportiamo il documento in .odt, possiamo utilizzare un oggetto OdtSaveOptions per modificare il modo in cui salviamo il documento.
// Possiamo impostare la proprietà "MeasureUnit" su "OdtSaveMeasureUnit.Centimeters"
 // per definire contenuti come parametri di stile utilizzando il sistema metrico utilizzato da Open Office.
// Possiamo impostare la proprietà "MeasureUnit" su "OdtSaveMeasureUnit.Inches"
// per definire contenuti come parametri di stile utilizzando il sistema imperiale, utilizzato da Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
