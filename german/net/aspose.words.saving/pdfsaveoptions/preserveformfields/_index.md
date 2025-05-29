---
title: PdfSaveOptions.PreserveFormFields
linktitle: PreserveFormFields
articleTitle: PreserveFormFields
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die PreserveFormFields-Eigenschaft von PdfSaveOptions Microsoft Word-Formularfelder in PDFs beibehält oder in Text konvertiert. Verbessern Sie die Qualität Ihrer Dokumente!
type: docs
weight: 280
url: /de/net/aspose.words.saving/pdfsaveoptions/preserveformfields/
---
## PdfSaveOptions.PreserveFormFields property

Gibt an, ob Microsoft Word-Formularfelder als Formularfelder in PDF erhalten bleiben oder in Text konvertiert werden sollen. Der Standardwert ist`FALSCH` .

```csharp
public bool PreserveFormFields { get; set; }
```

## Bemerkungen

Zu den Formularfeldern von Microsoft Word gehören Texteingabe-, Dropdown- und Kontrollkästchen-Steuerelemente.

Bei Einstellung auf`FALSCH` werden diese Felder als Text in PDF exportiert. Wenn Sie auf`WAHR`, Diese Felder werden als PDF-Formularfelder exportiert.

Beim Exportieren von Formularfeldern als Formularfelder in PDF kann es zu Formatierungsverlusten kommen, da PDF-Formularfelder „form “ nicht alle Funktionen von Microsoft Word-Formularfeldern unterstützen.

Außerdem hängt die Ausgabegröße von der Inhaltsgröße ab, da bearbeitbare Formulare in Microsoft Word Inline-Objekte sind.

Bearbeitbare Formulare sind aufgrund der PDF/A-Konformität verboten.`FALSCH` Beim Speichern im PDF/A-Format wird der Wert automatisch verwendet.

Formularfelder werden beim Speichern im PDF/UA-Format nicht unterstützt.`FALSCH` Wert wird automatisch verwendet.

## Beispiele

Zeigt, wie ein Dokument mit der Save-Methode und der PdfSaveOptions-Klasse im PDF-Format gespeichert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Fügen Sie ein Kombinationsfeld ein, das es einem Benutzer ermöglicht, eine Option aus einer Sammlung von Zeichenfolgen auszuwählen.
builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions pdfOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „PreserveFormFields“ auf „true“, um Formularfelder als interaktive Objekte im Ausgabe-PDF zu speichern.
// Setzen Sie die Eigenschaft "PreserveFormFields" auf "false", um alle Formularfelder im Dokument einzufrieren.
// ihre aktuellen Werte und zeigen Sie sie als einfachen Text im Ausgabe-PDF an.
pdfOptions.PreserveFormFields = preserveFormFields;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
