---
title: PdfSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klonmethode von PdfSaveOptions, um mühelos einen vollständigen Klon Ihrer Objekte zu erstellen und so Ihre PDF-Verwaltungsfunktionen zu verbessern.
type: docs
weight: 370
url: /de/net/aspose.words.saving/pdfsaveoptions/clone/
---
## PdfSaveOptions.Clone method

Erstellt einen tiefen Klon dieses Objekts.

```csharp
public PdfSaveOptions Clone()
```

## Beispiele

Zeigt, wie alle Felder in einem Dokument unmittelbar vor dem Speichern als PDF aktualisiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Text mit den Feldern PAGE und NUMPAGES einfügen. Diese Felder zeigen in Echtzeit nicht den richtigen Wert an.
// Wir müssen sie manuell aktualisieren, indem wir Aktualisierungsmethoden wie „Field.Update()“ und „Document.UpdateFields()“ verwenden.
// jedes Mal müssen sie genaue Werte anzeigen.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „UpdateFields“ auf „false“, um nicht alle Felder in einem Dokument direkt vor einem Speichervorgang zu aktualisieren.
// Dies ist die bevorzugte Option, wenn wir wissen, dass alle unsere Felder vor dem Speichern auf dem neuesten Stand sind.
// Setzen Sie die Eigenschaft "UpdateFields" auf "true", um das gesamte Dokument zu durchlaufen
// Felder und aktualisieren Sie sie, bevor wir es als PDF speichern. Dadurch wird sichergestellt, dass alle Felder angezeigt werden
// die genauesten Werte im PDF.
options.UpdateFields = updateFields;

// Wir können PdfSaveOptions-Objekte klonen.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### Siehe auch

* class [PdfSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
