---
title: OutlineOptions.HeadingsOutlineLevels
second_title: Aspose.Words für .NET-API-Referenz
description: OutlineOptions eigendom. Gibt an wie viele Überschriftenebenen mit den Überschriftenstilen formatierte Absätze in die Dokumentgliederung einbezogen werden sollen.
type: docs
weight: 70
url: /de/net/aspose.words.saving/outlineoptions/headingsoutlinelevels/
---
## OutlineOptions.HeadingsOutlineLevels property

Gibt an, wie viele Überschriftenebenen (mit den Überschriftenstilen formatierte Absätze) in die Dokumentgliederung einbezogen werden sollen.

```csharp
public int HeadingsOutlineLevels { get; set; }
```

### Bemerkungen

Geben Sie 0 an, wenn die Gliederung keine Überschriften enthält. Geben Sie 1 für eine Überschriftenebene in der Gliederung usw. an.

Der Standardwert ist 0. Der gültige Bereich liegt zwischen 0 und 9.

### Beispiele

Zeigt, wie ein gesamtes Dokument mit drei Ebenen in der Dokumentgliederung in PDF konvertiert wird.

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

// Erstellen Sie ein „PdfSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Das ausgegebene PDF-Dokument enthält eine Gliederung, bei der es sich um ein Inhaltsverzeichnis handelt, das die Überschriften im Hauptteil des Dokuments auflistet.
// Durch Klicken auf einen Eintrag in dieser Gliederung gelangen wir zur Position der entsprechenden Überschrift.
// Setzen Sie die Eigenschaft „HeadingsOutlineLevels“ auf „4“, um alle Überschriften, deren Ebenen über 4 liegen, aus der Gliederung auszuschließen.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Wenn ein Gliederungseintrag zwischen sich und dem nächsten Eintrag derselben oder einer niedrigeren Ebene nachfolgende Einträge einer höheren Ebene hat,
// links neben dem Eintrag erscheint ein Pfeil. Dieser Eintrag ist „Eigentümer“ mehrerer solcher „Untereinträge“.
// In unserem Dokument sind die Gliederungseinträge der 5. Überschriftenebene Untereinträge des zweiten Gliederungseintrags der 4. Ebene,
// Die Einträge der 4. und 5. Überschriftenebene sind Untereinträge des zweiten Eintrags der 3. Ebene usw.
// In der Gliederung können wir auf den Pfeil des Eintrags „Eigentümer“ klicken, um alle Untereinträge ein-/auszuklappen.
// Setzen Sie die Eigenschaft „ExpandedOutlineLevels“ auf „2“, um alle Gliederungseinträge der Überschriftenebene 2 und darunter automatisch zu erweitern
// und alle Einträge der Ebene und 3 und höher ausblenden, wenn wir das Dokument öffnen.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Siehe auch

* class [OutlineOptions](../)
* namensraum [Aspose.Words.Saving](../../outlineoptions/)
* Montage [Aspose.Words](../../../)


