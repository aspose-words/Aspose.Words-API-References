---
title: Dml3DEffectsRenderingMode Enum
linktitle: Dml3DEffectsRenderingMode
articleTitle: Dml3DEffectsRenderingMode
second_title: Aspose.Words per .NET
description: Scopri come migliorare i tuoi documenti con l'enum Dml3DEffectsRenderingMode di Aspose.Words per un rendering di forme 3D e un impatto visivo superiori.
type: docs
weight: 5650
url: /it/net/aspose.words.saving/dml3deffectsrenderingmode/
---
## Dml3DEffectsRenderingMode enumeration

Specifica come vengono renderizzati gli effetti delle forme 3D.

```csharp
public enum Dml3DEffectsRenderingMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Basic | `0` | Un rendering leggero e stabile, basato sul motore interno, ma gli effetti avanzati come illuminazione, materiali e altri effetti aggiuntivi non vengono visualizzati quando si utilizza questa modalità. Per i dettagli, consultare la documentazione. |
| Advanced | `1` | Rendering di un elenco esteso di effetti speciali, inclusi effetti 3D avanzati come smussi, illuminazione e materiali. |

## Esempi

Mostra come vengono resi gli effetti 3D.

```csharp
Document doc = new Document(MyDir + "DrawingML shape 3D effects.docx");

RenderCallback warningCallback = new RenderCallback();
doc.WarningCallback = warningCallback;

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.Dml3DEffectsRenderingMode = Dml3DEffectsRenderingMode.Advanced;

doc.Save(ArtifactsDir + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
