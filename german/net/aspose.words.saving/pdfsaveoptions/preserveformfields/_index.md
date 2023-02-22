---
title: PdfSaveOptions.PreserveFormFields
second_title: Aspose.Words für .NET-API-Referenz
description: PdfSaveOptions eigendom. Gibt an ob Microsoft WordFormularfelder als Formularfelder in PDF beibehalten oder in Text konvertiert werden sollen. Standard istFALSCH .
type: docs
weight: 240
url: /de/net/aspose.words.saving/pdfsaveoptions/preserveformfields/
---
## PdfSaveOptions.PreserveFormFields property

Gibt an, ob Microsoft Word-Formularfelder als Formularfelder in PDF beibehalten oder in Text konvertiert werden sollen. Standard ist`FALSCH` .

```csharp
public bool PreserveFormFields { get; set; }
```

### Bemerkungen

Microsoft Word-Formularfelder umfassen Texteingabe, Dropdown- und Kontrollkästchen-Steuerelemente.

Wenn eingestellt auf`FALSCH` , werden diese Felder als Text in PDF exportiert. Wenn eingestellt auf`Stimmt`, diese Felder werden als PDF-Formularfelder exportiert.

Beim Exportieren von Formularfeldern in PDF als Formularfelder kann ein gewisser Formatierungsverlust auftreten, da PDF-form -Felder nicht alle Funktionen von Microsoft Word-Formularfeldern unterstützen.

Außerdem hängt die Ausgabegröße von der Inhaltsgröße ab, da bearbeitbare Formulare in Microsoft Word Inline-Objekte sind.

Bearbeitbare Formulare sind durch die PDF/A-Konformität verboten.`FALSCH` Wert wird beim Speichern in PDF/A automatisch verwendet.

Formularfelder werden beim Speichern in PDF/UA nicht unterstützt.`FALSCH` Wert wird automatisch verwendet.

### Beispiele

Zeigt, wie ein Dokument mithilfe der Save-Methode und der PdfSaveOptions-Klasse im PDF-Format gespeichert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Fügen Sie ein Kombinationsfeld ein, das es einem Benutzer ermöglicht, eine Option aus einer Sammlung von Zeichenfolgen auszuwählen.
builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions pdfOptions = new PdfSaveOptions();

// Setzen Sie die Eigenschaft "PreserveFormFields" auf "true", um Formularfelder als interaktive Objekte in der Ausgabe-PDF zu speichern.
// Setzen Sie die Eigenschaft "PreserveFormFields" auf "false", um alle Formularfelder im Dokument einzufrieren
// ihre aktuellen Werte und zeigen sie als Klartext in der Ausgabe-PDF an.
pdfOptions.PreserveFormFields = preserveFormFields;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../pdfsaveoptions/)
* Montage [Aspose.Words](../../../)


