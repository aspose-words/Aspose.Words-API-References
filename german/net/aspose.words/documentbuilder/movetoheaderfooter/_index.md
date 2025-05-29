---
title: DocumentBuilder.MoveToHeaderFooter
linktitle: MoveToHeaderFooter
articleTitle: MoveToHeaderFooter
second_title: Aspose.Words für .NET
description: Navigieren Sie mit der DocumentBuilder MoveToHeaderFooter-Methode mühelos zu Kopf- und Fußzeilen und steigern Sie so die Effizienz Ihrer Dokumentbearbeitung.
type: docs
weight: 580
url: /de/net/aspose.words/documentbuilder/movetoheaderfooter/
---
## DocumentBuilder.MoveToHeaderFooter method

Bewegt den Cursor an den Anfang einer Kopf- oder Fußzeile im aktuellen Abschnitt.

```csharp
public void MoveToHeaderFooter(HeaderFooterType headerFooterType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | Gibt die Kopf- oder Fußzeile an, zu der gewechselt werden soll. |

## Bemerkungen

Nachdem Sie den Cursor in eine Kopf- oder Fußzeile bewegt haben, können Sie den Rest[`DocumentBuilder`](../) -Methoden zum Ändern des Inhalts der Kopf- oder Fußzeile.

Wenn Sie Kopf- und Fußzeilen für die erste Seite unterschiedlich gestalten möchten, müssen Sie festlegen[`DifferentFirstPageHeaderFooter`](../../pagesetup/differentfirstpageheaderfooter/).

Wenn Sie Kopf- und Fußzeilen für gerade und ungerade Seiten unterschiedlich gestalten möchten, müssen Sie festlegen[`OddAndEvenPagesHeaderFooter`](../../pagesetup/oddandevenpagesheaderfooter/).

Verwenden[`MoveToSection`](../movetosection/) aus der Kopfzeile in den Haupttext zu gelangen.

## Beispiele

Zeigt, wie Sie ein Bild einfügen und als Wasserzeichen verwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie das Bild in die Kopfzeile ein, damit es auf jeder Seite sichtbar ist.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Platzieren Sie das Bild in der Mitte der Seite.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

Zeigt, wie Sie mit DocumentBuilder Kopf- und Fußzeilen in einem Dokument erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie an, dass wir für die erste, die gerade und die ungerade Seite unterschiedliche Kopf- und Fußzeilen wünschen.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Erstellen Sie die Kopfzeilen und fügen Sie dem Dokument dann drei Seiten hinzu, um jeden Kopfzeilentyp anzuzeigen.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

### Siehe auch

* enum [HeaderFooterType](../../headerfootertype/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
