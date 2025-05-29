---
title: FieldToc.CustomStyles
linktitle: CustomStyles
articleTitle: CustomStyles
second_title: Aspose.Words für .NET
description: Passen Sie Ihr Inhaltsverzeichnis mit der CustomStyles-Eigenschaft von FieldToc an. Fügen Sie ganz einfach individuelle Stile über integrierte Überschriften hinaus hinzu, um die Präsentation zu verbessern.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fieldtoc/customstyles/
---
## FieldToc.CustomStyles property

Ruft eine Liste mit anderen Stilen als den integrierten Überschriftenstilen ab oder legt diese fest, die in das Inhaltsverzeichnis aufgenommen werden sollen.

```csharp
public string CustomStyles { get; set; }
```

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

* class [FieldToc](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
