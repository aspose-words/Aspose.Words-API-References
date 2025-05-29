---
title: Dml3DEffectsRenderingMode Enum
linktitle: Dml3DEffectsRenderingMode
articleTitle: Dml3DEffectsRenderingMode
second_title: Aspose.Words för .NET
description: Upptäck hur du kan förbättra dina dokument med Aspose.Words Dml3DEffectsRenderingMode-enum för överlägsen 3D-formrendering och visuell effekt.
type: docs
weight: 5650
url: /sv/net/aspose.words.saving/dml3deffectsrenderingmode/
---
## Dml3DEffectsRenderingMode enumeration

Anger hur 3D-formeffekter återges.

```csharp
public enum Dml3DEffectsRenderingMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Basic | `0` | En lätt och stabil rendering, baserad på den interna motorn, men avancerade effekter som belysning, material och andra ytterligare effekter visas inte när det här läget används. Se dokumentationen för mer information. |
| Advanced | `1` | Rendering av en utökad lista med specialeffekter, inklusive avancerade 3D-effekter såsom avfasningar, belysning och material. |

## Exempel

Visar hur 3D-effekter återges.

```csharp
Document doc = new Document(MyDir + "DrawingML shape 3D effects.docx");

RenderCallback warningCallback = new RenderCallback();
doc.WarningCallback = warningCallback;

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.Dml3DEffectsRenderingMode = Dml3DEffectsRenderingMode.Advanced;

doc.Save(ArtifactsDir + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
