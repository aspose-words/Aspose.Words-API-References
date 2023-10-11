---
title: OdtSaveOptions.MeasureUnit
second_title: Aspose.Words per .NET API Reference
description: OdtSaveOptions proprietà. Permette di specificare le unità di misura da applicare al contenuto del documento. Il valore predefinito èCentimeters
type: docs
weight: 30
url: /it/net/aspose.words.saving/odtsaveoptions/measureunit/
---
## OdtSaveOptions.MeasureUnit property

Permette di specificare le unità di misura da applicare al contenuto del documento. Il valore predefinito èCentimeters

```csharp
public OdtSaveMeasureUnit MeasureUnit { get; set; }
```

### Osservazioni

Open Office utilizza i centimetri per specificare lunghezze, larghezze e altre formattazioni misurabili e proprietà del contenuto nei documenti mentre MS Office utilizza i pollici.

### Esempi

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

* enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* class [OdtSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../odtsaveoptions/)
* assemblea [Aspose.Words](../../../)


