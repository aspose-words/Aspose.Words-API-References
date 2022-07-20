---
title: CustomTocStyleSeparator
second_title: Aspose.Words für .NET-API-Referenz
description: Ruft benutzerdefiniertes Trennzeichen für den t-Schalter ab oder legt es festFieldTocaspose.words.fields/fieldtoc Feld.
type: docs
weight: 50
url: /de/net/aspose.words.fields/fieldoptions/customtocstyleseparator/
---
## FieldOptions.CustomTocStyleSeparator property

Ruft benutzerdefiniertes Trennzeichen für den \t-Schalter ab oder legt es fest[`FieldToc`](../../fieldtoc) Feld.

```csharp
public string CustomTocStyleSeparator { get; set; }
```

### Bemerkungen

Standardmäßig werden benutzerdefinierte Stile, die durch den Schalter \t in der[`FieldToc`](../../fieldtoc) Felder werden durch ein Trennzeichen aus der aktuellen Kultur getrennt. Diese Eigenschaft überschreibt dieses Verhalten, indem sie ein benutzerdefiniertes Trennzeichen angibt.

### Beispiele

Zeigt, wie ein Inhaltsverzeichnis eingefügt und mit Einträgen auf der Grundlage von Überschriftenstilen gefüllt wird.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Füge ein TOC-Feld ein, das alle Überschriften zu einem Inhaltsverzeichnis zusammenstellt.
    // Für jede Überschrift erstellt dieses Feld eine Zeile mit dem Text in diesem Überschriftenstil auf der linken Seite,
    // und die Seite, auf der die Überschrift erscheint, rechts.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Verwenden Sie die BookmarkName-Eigenschaft, um nur Überschriften aufzulisten
    // die innerhalb der Grenzen eines Lesezeichens mit dem Namen "MyBookmark" erscheinen.
    field.BookmarkName = "MyBookmark";

    // Text mit einem integrierten Überschriftenstil, wie z. B. "Überschrift 1", der darauf angewendet wird, zählt als Überschrift.
    // Wir können zusätzliche Stile benennen, die als Überschriften vom Inhaltsverzeichnis in dieser Eigenschaft und ihren Inhaltsverzeichnisebenen aufgenommen werden sollen.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Standardmäßig werden Styles/TOC-Ebenen in der CustomStyles-Eigenschaft durch ein Komma getrennt,
    // aber wir können in dieser Eigenschaft ein benutzerdefiniertes Trennzeichen setzen.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Konfigurieren Sie das Feld so, dass alle Überschriften ausgeschlossen werden, deren Inhaltsverzeichnis außerhalb dieses Bereichs liegt.
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

    // Bei diesen beiden Überschriften werden die Seitenzahlen weggelassen, da sie im Bereich "2-5" liegen.
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // Dieser Eintrag erscheint nicht, da "Überschrift 4" außerhalb des Bereichs "1-3" liegt, den wir zuvor festgelegt haben.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Dieser Eintrag wird nicht angezeigt, da er sich außerhalb des vom Inhaltsverzeichnis angegebenen Lesezeichens befindet.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");

/// <summary>
/// Beginne eine neue Seite und füge einen Absatz eines bestimmten Stils ein.
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

* class [FieldOptions](../../fieldoptions)
* namensraum [Aspose.Words.Fields](../../fieldoptions)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->