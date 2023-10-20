---
title: PdfSaveOptions.PreserveFormFields
linktitle: PreserveFormFields
articleTitle: PreserveFormFields
second_title: Aspose.Words für .NET
description: PdfSaveOptions PreserveFormFields eigendom. Gibt an ob Microsoft WordFormularfelder als Formularfelder in PDF beibehalten oder in Text konvertiert werden sollen. Die Standardeinstellung istFALSCH  in C#.
type: docs
weight: 270
url: /de/net/aspose.words.saving/pdfsaveoptions/preserveformfields/
---
## PdfSaveOptions.PreserveFormFields property

Gibt an, ob Microsoft Word-Formularfelder als Formularfelder in PDF beibehalten oder in Text konvertiert werden sollen. Die Standardeinstellung ist`FALSCH` .

```csharp
public bool PreserveFormFields { get; set; }
```

## Bemerkungen

Zu den Microsoft Word-Formularfeldern gehören Texteingabe-, Dropdown- und Kontrollkästchen-Steuerelemente.

Wenn eingestellt auf`FALSCH` , werden diese Felder als Text in PDF exportiert. Wenn eingestellt auf`WAHR`, Diese Felder werden als PDF-Formularfelder exportiert.

Beim Exportieren von Formularfeldern als Formularfelder nach PDF kann es zu Formatierungsverlusten kommen, da PDF-Formularfelder nicht alle Funktionen von Microsoft Word-Formularfeldern unterstützen.

Außerdem hängt die Ausgabegröße von der Inhaltsgröße ab, da bearbeitbare Formulare in Microsoft Word Inline-Objekte sind.

Bearbeitbare Formulare sind durch die PDF/A-Konformität verboten.`FALSCH` Beim Speichern in PDF/A wird der Wert automatisch verwendet.

Formularfelder werden beim Speichern in PDF/UA nicht unterstützt.`FALSCH` Der Wert wird automatisch verwendet.

## Beispiele

Zeigt, wie ein Dokument mithilfe der Save-Methode und der PdfSaveOptions-Klasse im PDF-Format gespeichert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Ein Kombinationsfeld einfügen, das es einem Benutzer ermöglicht, eine Option aus einer Sammlung von Zeichenfolgen auszuwählen.
builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions pdfOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „PreserveFormFields“ auf „true“, um Formularfelder als interaktive Objekte in der Ausgabe-PDF zu speichern.
// Setzen Sie die Eigenschaft „PreserveFormFields“ auf „false“, um alle Formularfelder im Dokument einzufrieren
// ihre aktuellen Werte und zeigen sie als Klartext im Ausgabe-PDF an.
pdfOptions.PreserveFormFields = preserveFormFields;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
