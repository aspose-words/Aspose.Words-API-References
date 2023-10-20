---
title: SaveOptions.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words für .NET
description: SaveOptions UpdateFields eigendom. Ruft einen Wert ab oder legt diesen fest der bestimmt ob Felder bestimmter Typen aktualisiert werden sollen bevor das Dokument in einem festen Seitenformat gespeichert wird. Der Standardwert für diese Eigenschaft istWAHR  in C#.
type: docs
weight: 160
url: /de/net/aspose.words.saving/saveoptions/updatefields/
---
## SaveOptions.UpdateFields property

Ruft einen Wert ab oder legt diesen fest, der bestimmt, ob Felder bestimmter Typen aktualisiert werden sollen, bevor das Dokument in einem festen Seitenformat gespeichert wird. Der Standardwert für diese Eigenschaft ist`WAHR` .

```csharp
public bool UpdateFields { get; set; }
```

## Bemerkungen

Ermöglicht die Angabe, ob das Verhalten von MS Word nachgeahmt werden soll oder nicht.

## Beispiele

Zeigt, wie alle Felder in einem Dokument unmittelbar vor dem Speichern als PDF aktualisiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Text mit den Feldern PAGE und NUMPAGES einfügen. Diese Felder zeigen nicht den korrekten Wert in Echtzeit an.
// Wir müssen sie manuell mit Aktualisierungsmethoden wie „Field.Update()“ und „Document.UpdateFields()“ aktualisieren.
// jedes Mal, wenn wir sie benötigen, um genaue Werte anzuzeigen.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „UpdateFields“ auf „false“, um nicht alle Felder in einem Dokument unmittelbar vor einem Speichervorgang zu aktualisieren.
// Dies ist die bevorzugte Option, wenn wir wissen, dass alle unsere Felder vor dem Speichern auf dem neuesten Stand sind.
// Setzen Sie die Eigenschaft „UpdateFields“ auf „true“, um das gesamte Dokument zu durchlaufen
// Felder und aktualisieren Sie sie, bevor wir sie als PDF speichern. Dadurch wird sichergestellt, dass alle Felder angezeigt werden
// die genauesten Werte im PDF.
options.UpdateFields = updateFields;

// Wir können PdfSaveOptions-Objekte klonen.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### Siehe auch

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
