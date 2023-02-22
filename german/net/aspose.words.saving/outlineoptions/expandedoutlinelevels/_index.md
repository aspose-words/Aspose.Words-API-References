---
title: OutlineOptions.ExpandedOutlineLevels
second_title: Aspose.Words für .NET-API-Referenz
description: OutlineOptions eigendom. Gibt an wie viele Ebenen in der Dokumentgliederung erweitert angezeigt werden wenn die Datei angezeigt wird.
type: docs
weight: 60
url: /de/net/aspose.words.saving/outlineoptions/expandedoutlinelevels/
---
## OutlineOptions.ExpandedOutlineLevels property

Gibt an, wie viele Ebenen in der Dokumentgliederung erweitert angezeigt werden, wenn die Datei angezeigt wird.

```csharp
public int ExpandedOutlineLevels { get; set; }
```

### Bemerkungen

Beachten Sie, dass diese Optionen beim Speichern in XPS nicht funktionieren.

Geben Sie 0 an, und die Dokumentgliederung wird reduziert; Geben Sie 1 an und die erste Ebene items in der Gliederung wird erweitert und so weiter.

Der Standardwert ist 0. Der gültige Bereich ist 0 bis 9.

### Beispiele

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

// Das ausgegebene PDF-Dokument enthält eine Gliederung, die ein Inhaltsverzeichnis ist, das Überschriften im Dokumentkörper auflistet.
// Durch Klicken auf einen Eintrag in dieser Gliederung gelangen wir zur Position der entsprechenden Überschrift.
// Setzen Sie die Eigenschaft "HeadingsOutlineLevels" auf "4", um alle Überschriften, deren Ebenen höher als 4 sind, von der Gliederung auszuschließen.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Wenn ein Gliederungseintrag nachfolgende Einträge einer höheren Ebene zwischen sich und dem nächsten Eintrag der gleichen oder niedrigeren Ebene hat,
// Links neben dem Eintrag erscheint ein Pfeil. Dieser Eintrag ist der "Eigentümer" mehrerer solcher "Untereinträge".
// In unserem Dokument sind die Gliederungseinträge der 5. Überschriftenebene Untereinträge der zweiten Gliederungsebene der 4. Ebene,
 // Die Einträge der 4. und 5. Überschriftenebene sind Untereinträge des zweiten Eintrags der 3. Ebene und so weiter.
// In der Gliederung können wir auf den Pfeil des „Besitzer“-Eintrags klicken, um alle seine Untereinträge zu reduzieren/erweitern.
// Legen Sie die Eigenschaft "ExpandedOutlineLevels" auf "2" fest, um automatisch alle Einträge der Überschriftenebene 2 und der unteren Gliederung zu erweitern
 // und alle Einträge der Ebene und 3 und höher reduzieren, wenn wir das Dokument öffnen.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Siehe auch

* class [OutlineOptions](../)
* namensraum [Aspose.Words.Saving](../../outlineoptions/)
* Montage [Aspose.Words](../../../)


