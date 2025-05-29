---
title: OutlineOptions.ExpandedOutlineLevels
linktitle: ExpandedOutlineLevels
articleTitle: ExpandedOutlineLevels
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ExpandedOutlineLevels“ in „OutlineOptions“, mit der Sie die Sichtbarkeit der Dokumentgliederung anpassen können, um die Navigation und das Benutzererlebnis zu verbessern.
type: docs
weight: 60
url: /de/net/aspose.words.saving/outlineoptions/expandedoutlinelevels/
---
## OutlineOptions.ExpandedOutlineLevels property

Gibt an, wie viele Ebenen in der Dokumentgliederung beim Anzeigen der Datei erweitert angezeigt werden sollen.

```csharp
public int ExpandedOutlineLevels { get; set; }
```

## Bemerkungen

Beachten Sie, dass diese Optionen beim Speichern im XPS-Format nicht funktionieren.

Geben Sie 0 an, und die Gliederung des Dokuments wird reduziert; geben Sie 1 an, und die erste Ebene „items “ in der Gliederung wird erweitert usw.

Der Standardwert ist 0. Gültiger Bereich ist 0 bis 9.

## Beispiele

Zeigt, wie ein ganzes Dokument mit drei Ebenen in der Dokumentgliederung in PDF konvertiert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Überschriften der Ebenen 1 bis 5 einfügen.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Das ausgegebene PDF-Dokument enthält eine Gliederung, d. h. ein Inhaltsverzeichnis, das die Überschriften im Dokumenttext auflistet.
// Durch Klicken auf einen Eintrag in dieser Gliederung gelangen wir zur Position der entsprechenden Überschrift.
// Setzen Sie die Eigenschaft „HeadingsOutlineLevels“ auf „4“, um alle Überschriften, deren Ebenen über 4 liegen, aus der Gliederung auszuschließen.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Wenn ein Gliederungseintrag nachfolgende Einträge einer höheren Ebene zwischen sich selbst und dem nächsten Eintrag der gleichen oder niedrigeren Ebene hat,
// links neben dem Eintrag erscheint ein Pfeil. Dieser Eintrag ist der „Eigentümer“ mehrerer solcher „Untereinträge“.
// In unserem Dokument sind die Gliederungseinträge der 5. Überschriftenebene Untereinträge des zweiten Gliederungseintrags der 4. Ebene,
// Die Einträge der 4. und 5. Überschriftenebene sind Untereinträge des zweiten Eintrags der 3. Ebene und so weiter.
// In der Gliederung können wir auf den Pfeil des Eintrags „Eigentümer“ klicken, um alle Untereinträge auszublenden/einzuklappen.
// Setzen Sie die Eigenschaft „ExpandedOutlineLevels“ auf „2“, um alle Gliederungseinträge der Überschriftenebene 2 und darunter automatisch zu erweitern
// und reduzieren Sie alle Einträge der Ebene 3 und höher, wenn wir das Dokument öffnen.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Siehe auch

* class [OutlineOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
