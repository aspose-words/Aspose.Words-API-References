---
title: OdtSaveOptions.MeasureUnit
linktitle: MeasureUnit
articleTitle: MeasureUnit
second_title: Aspose.Words per .NET
description: Personalizza l'unità di misura del tuo documento con OdtSaveOptions. Scegli le tue unità di misura preferite per la precisione l'unità predefinita è Centimetri.
type: docs
weight: 40
url: /it/net/aspose.words.saving/odtsaveoptions/measureunit/
---
## OdtSaveOptions.MeasureUnit property

Consente di specificare le unità di misura da applicare al contenuto del documento. Il valore predefinito èCentimeters

```csharp
public OdtSaveMeasureUnit MeasureUnit { get; set; }
```

## Osservazioni

Open Office utilizza i centimetri per specificare lunghezze, larghezze e altre proprietà di formattazione e contenuto misurabili nei documenti, mentre MS Office utilizza i pollici.

## Esempi

Mostra come utilizzare diverse unità di misura per definire i parametri di stile di un documento ODT salvato.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Quando esportiamo il documento in formato .odt, possiamo utilizzare un oggetto OdtSaveOptions per modificare il modo in cui salviamo il documento.
// Possiamo impostare la proprietà "MeasureUnit" su "OdtSaveMeasureUnit.Centimeters"
 // per definire contenuti quali parametri di stile utilizzando il sistema metrico utilizzato da Open Office.
// Possiamo impostare la proprietà "MeasureUnit" su "OdtSaveMeasureUnit.Inches"
// per definire contenuti quali parametri di stile utilizzando il sistema imperiale, utilizzato da Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Guarda anche

* enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* class [OdtSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
