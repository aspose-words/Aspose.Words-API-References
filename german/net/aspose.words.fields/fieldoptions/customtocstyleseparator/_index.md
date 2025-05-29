---
title: FieldOptions.CustomTocStyleSeparator
linktitle: CustomTocStyleSeparator
articleTitle: CustomTocStyleSeparator
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldOptions CustomTocStyleSeparator-Eigenschaft, um den Stiltrenner Ihres FieldToc-Felds für eine verbesserte Dokumentnavigation einfach anzupassen.
type: docs
weight: 60
url: /de/net/aspose.words.fields/fieldoptions/customtocstyleseparator/
---
## FieldOptions.CustomTocStyleSeparator property

Ruft einen benutzerdefinierten Stiltrenner für den \t-Schalter ab oder legt ihn fest in[`FieldToc`](../../fieldtoc/) Feld.

```csharp
public string CustomTocStyleSeparator { get; set; }
```

## Bemerkungen

Standardmäßig werden benutzerdefinierte Stile, die durch den Schalter \t in der[`FieldToc`](../../fieldtoc/) Felder werden durch ein Trennzeichen aus der aktuellen Kultur getrennt. Diese Eigenschaft überschreibt dieses Verhalten durch Angabe eines benutzerdefinierten Trennzeichens.

## Beispiele

Zeigt, wie Sie ein Inhaltsverzeichnis einfügen und es mit Einträgen basierend auf Überschriftenstilen füllen.

```csharp
public void FieldToc()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Fügen Sie ein TOC-Feld ein, das alle Überschriften in einem Inhaltsverzeichnis zusammenfasst.
    // Für jede Überschrift erstellt dieses Feld eine Zeile mit dem Text in diesem Überschriftenstil auf der linken Seite.
    // und rechts die Seite, auf der die Überschrift erscheint.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Verwenden Sie die Eigenschaft BookmarkName, um nur Überschriften aufzulisten
    // die innerhalb der Grenzen eines Lesezeichens mit dem Namen „MyBookmark“ erscheinen.
    field.BookmarkName = "MyBookmark";

    // Text mit einem integrierten Überschriftenstil, z. B. „Überschrift 1“, wird als Überschrift gezählt.
    // In dieser Eigenschaft und den Inhaltsverzeichnisebenen können wir weitere Stile benennen, die als Überschriften vom Inhaltsverzeichnis übernommen werden sollen.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Standardmäßig werden Stile/Inhaltsverzeichnisebenen in der Eigenschaft „CustomStyles“ durch ein Komma getrennt.
    // aber wir können in dieser Eigenschaft ein benutzerdefiniertes Trennzeichen festlegen.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Konfigurieren Sie das Feld so, dass alle Überschriften ausgeschlossen werden, deren Inhaltsverzeichnisebenen außerhalb dieses Bereichs liegen.
    field.HeadingLevelRange = "1-3";

    // Das Inhaltsverzeichnis zeigt nicht die Seitenzahlen von Überschriften an, deren Inhaltsverzeichnisebenen innerhalb dieses Bereichs liegen.
    field.PageNumberOmittingLevelRange = "2-5";

        // Legen Sie eine benutzerdefinierte Zeichenfolge fest, die jede Überschrift von ihrer Seitenzahl trennt.
    field.EntrySeparator = "-";
    field.InsertHyperlinks = true;
    field.HideInWebLayout = false;
    field.PreserveLineBreaks = true;
    field.PreserveTabs = true;
    field.UseParagraphOutlineLevel = false;

    InsertNewPageWithHeading(builder, "First entry", "Heading 1");
    builder.Writeln("Paragraph text.");
    InsertNewPageWithHeading(builder, "Second entry", "Heading 1");
    InsertNewPageWithHeading(builder, "Third entry", "Quote");
    InsertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

    // Bei diesen beiden Überschriften werden die Seitenzahlen weggelassen, da sie im Bereich „2-5“ liegen.
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // Dieser Eintrag wird nicht angezeigt, da „Überschrift 4“ außerhalb des zuvor festgelegten Bereichs „1–3“ liegt.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Dieser Eintrag wird nicht angezeigt, da er außerhalb des im Inhaltsverzeichnis angegebenen Lesezeichens liegt.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");
}

/// <summary>
/// Beginnen Sie eine neue Seite und fügen Sie einen Absatz im angegebenen Stil ein.
/// </summary>
public void InsertNewPageWithHeading(DocumentBuilder builder, string captionText, string styleName)
{
    builder.InsertBreak(BreakType.PageBreak);
    string originalStyle = builder.ParagraphFormat.StyleName;
    builder.ParagraphFormat.Style = builder.Document.Styles[styleName];
    builder.Writeln(captionText);
    builder.ParagraphFormat.Style = builder.Document.Styles[originalStyle];
}
```

### Siehe auch

* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
