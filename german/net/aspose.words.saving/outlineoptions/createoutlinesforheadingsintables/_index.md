---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
linktitle: CreateOutlinesForHeadingsInTables
articleTitle: CreateOutlinesForHeadingsInTables
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „CreateOutlinesForHeadingsInTables“ die Tabellenorganisation verbessert, indem sie Gliederungen für Überschriftenstile ermöglicht und so die Übersichtlichkeit des Dokuments verbessert.
type: docs
weight: 40
url: /de/net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

Gibt an, ob Gliederungen für Überschriften (mit den Überschriftenstilen formatierte Absätze) in Tabellen erstellt werden sollen oder nicht.

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH`.

## Beispiele

Zeigt, wie Gliederungseinträge für Überschriften in Tabellen in PDF-Dokumenten erstellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie eine Tabelle mit drei Zeilen. Die erste Zeile,
// dessen Text wir im Überschriftenstil formatieren, dient als Spaltenüberschrift.
builder.StartTable();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("Customers");
builder.EndRow();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Write("John Doe");
builder.EndRow();
builder.InsertCell();
builder.Write("Jane Doe");
builder.EndTable();

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Das ausgegebene PDF-Dokument enthält eine Gliederung, d. h. ein Inhaltsverzeichnis, das die Überschriften im Dokumenttext auflistet.
// Durch Klicken auf einen Eintrag in dieser Gliederung gelangen wir zur Position der entsprechenden Überschrift.
// Setzen Sie die Eigenschaft "HeadingsOutlineLevels" auf "1", um die Gliederung zu erhalten
// um nur Überschriften mit Überschriftenebenen zu registrieren, die nicht größer als 1 sind.
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// Setzen Sie die Eigenschaft „CreateOutlinesForHeadingsInTables“ auf „false“, um alle Überschriften innerhalb von Tabellen auszuschließen,
// wie das, das wir oben aus der Gliederung erstellt haben.
// Setzen Sie die Eigenschaft „CreateOutlinesForHeadingsInTables“ auf „true“, um alle Überschriften in Tabellen einzuschließen
// in der Gliederung, sofern sie eine Überschriftenebene haben, die nicht größer ist als der Wert der Eigenschaft „HeadingsOutlineLevels“.
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### Siehe auch

* class [OutlineOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
