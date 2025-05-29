---
title: PdfSaveOptions.UseSdtTagAsFormFieldName
linktitle: UseSdtTagAsFormFieldName
articleTitle: UseSdtTagAsFormFieldName
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die UseSdtTagAsFormFieldName-Eigenschaft von PdfSaveOptions PDF-Formulare durch die Verwendung von SDT-Steuertags für eine bessere Organisation und Übersichtlichkeit verbessert.
type: docs
weight: 340
url: /de/net/aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/
---
## PdfSaveOptions.UseSdtTagAsFormFieldName property

Gibt an, ob das SDT-Steuerelement-Tag oder die ID-Eigenschaft als Name des Formularfelds in PDF verwendet werden soll.

```csharp
public bool UseSdtTagAsFormFieldName { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH`.

Bei Einstellung auf`FALSCH`, die SDT-Steuerelement-ID-Eigenschaft wird als Name des Formularfelds in PDF verwendet.

Bei Einstellung auf`WAHR`, die SDT-Steuerelement-Tag-Eigenschaft wird als Name des Formularfelds in PDF verwendet.

Wenn eingestellt auf`WAHR` und das Tag leer ist, wird die ID-Eigenschaft als Formularfeldname verwendet.

Wenn eingestellt auf`WAHR` und Tag-Werte nicht eindeutig sind, werden doppelte Tag-Werte in build eindeutige PDF-Formularfeldnamen geändert.

## Beispiele

Zeigt, wie das SDT-Steuerelement-Tag oder die ID-Eigenschaft als Name eines Formularfelds in PDF verwendet wird.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
// Wenn auf „false“ gesetzt, wird die SDT-Steuerelement-ID-Eigenschaft als Name des Formularfelds im PDF verwendet.
// Wenn auf „true“ gesetzt, wird die Tag-Eigenschaft des SDT-Steuerelements als Name des Formularfelds im PDF verwendet.
saveOptions.UseSdtTagAsFormFieldName = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.SdtTagAsFormFieldName.pdf", saveOptions);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
