---
title: PdfSaveOptions.RenderChoiceFormFieldBorder
linktitle: RenderChoiceFormFieldBorder
articleTitle: RenderChoiceFormFieldBorder
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „RenderChoiceFormFieldBorder“ von PdfSaveOptions das Design von PDF-Formularen verbessert, indem sie die Grenzen der Auswahlfelder steuert und so für ein besseres Benutzererlebnis sorgt.
type: docs
weight: 290
url: /de/net/aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/
---
## PdfSaveOptions.RenderChoiceFormFieldBorder property

Gibt an, ob der Feldrand des PDF-Auswahlformulars gerendert werden soll.

```csharp
public bool RenderChoiceFormFieldBorder { get; set; }
```

## Bemerkungen

PDF-Auswahlformularfelder werden für den Export von SDT Combo Box Content Control, SDT Drop-Down List Content Control und Legacy Drop-Down Form Field verwendet, wenn[`PreserveFormFields`](../preserveformfields/) Option ist aktiviert.

Der Standardwert ist`WAHR`.

## Beispiele

Zeigt, wie der Feldrand eines PDF-Auswahlformulars gerendert wird.

```csharp
Document doc = new Document(MyDir + "Legacy drop-down.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
saveOptions.RenderChoiceFormFieldBorder = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderChoiceFormFieldBorder.pdf", saveOptions);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
