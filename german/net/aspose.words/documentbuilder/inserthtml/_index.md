---
title: DocumentBuilder.InsertHtml
linktitle: InsertHtml
articleTitle: InsertHtml
second_title: Aspose.Words für .NET
description: DocumentBuilder InsertHtml methode. Fügt einen HTMLString in das Dokument ein in C#.
type: docs
weight: 350
url: /de/net/aspose.words/documentbuilder/inserthtml/
---
## InsertHtml(*string*) {#inserthtml}

Fügt einen HTML-String in das Dokument ein.

```csharp
public void InsertHtml(string html)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| html | String | Eine HTML-Zeichenfolge zum Einfügen in das Dokument. |

## Bemerkungen

Mit dieser Methode können Sie ein HTML-Fragment oder ein ganzes HTML-Dokument einfügen.

## Beispiele

Zeigt, wie man mit einem Document Builder HTML-Inhalte in ein Dokument einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const string html = "<p align='right'>Paragraph right</p>" + 
                    "<b>Implicit paragraph left</b>" +
                    "<div align='center'>Div center</div>" + 
                    "<h1 align='left'>Heading 1 left.</h1>";

builder.InsertHtml(html);

// Durch das Einfügen von HTML-Code wird die Formatierung jedes Elements in eine entsprechende Dokumenttextformatierung analysiert.
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual("Paragraph right", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

Assert.AreEqual("Implicit paragraph left", paragraphs[1].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.True(paragraphs[1].Runs[0].Font.Bold);

Assert.AreEqual("Div center", paragraphs[2].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Center, paragraphs[2].ParagraphFormat.Alignment);

Assert.AreEqual("Heading 1 left.", paragraphs[3].GetText().Trim());
Assert.AreEqual("Heading 1", paragraphs[3].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtml.docx");
```

Zeigt, wie ein Serienbrief mit einem benutzerdefinierten Rückruf ausgeführt wird, der Seriendaten in Form von HTML-Dokumenten verarbeitet.

```csharp
public void MergeHtml()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(@"MERGEFIELD  html_Title  \b Content");
    builder.InsertField(@"MERGEFIELD  html_Body  \b Content");

    object[] mergeData =
    {
        "<html>" +
            "<h1>" +
                "<span style=\"color: #0000ff; font-family: Arial;\">Hello World!</span>" +
            "</h1>" +
        "</html>", 

        "<html>" +
            "<blockquote>" +
                "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>" +
            "</blockquote>" +
        "</html>"
    };

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertHtml();
    doc.MailMerge.Execute(new[] { "html_Title", "html_Body" }, mergeData);

    doc.Save(ArtifactsDir + "MailMergeEvent.MergeHtml.docx");
}

/// <summary>
/// Wenn der Seriendruck auf ein MERGEFIELD trifft, dessen Name mit dem Präfix „html_“ beginnt,
/// Dieser Rückruf analysiert seine Zusammenführungsdaten als HTML-Inhalt und fügt das Ergebnis dem Dokumentspeicherort des MERGEFIELD hinzu.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Wird aufgerufen, wenn ein Serienbrief Daten in einem MERGEFIELD zusammenführt.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Geparste HTML-Daten zum Hauptteil des Dokuments hinzufügen.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Da wir den zusammengeführten Inhalt bereits manuell eingefügt haben,
             // Wir müssen auf dieses Ereignis nicht reagieren, indem wir Inhalte über die Eigenschaft „Text“ zurückgeben.
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Nichts tun.
    }
}
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertHtml(*string, bool*) {#inserthtml_2}

Fügt einen HTML-String in das Dokument ein.

```csharp
public void InsertHtml(string html, bool useBuilderFormatting)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| html | String | Eine HTML-Zeichenfolge zum Einfügen in das Dokument. |
| useBuilderFormatting | Boolean | Ein Wert, der angibt, ob die Formatierung in angegeben ist[`DocumentBuilder`](../) wird als Basisformatierung für aus HTML importierten Text verwendet. |

## Bemerkungen

Mit dieser Methode können Sie ein HTML-Fragment oder ein ganzes HTML-Dokument einfügen.

Wann*useBuilderFormatting* Ist`FALSCH` , [`DocumentBuilder`](../)Die Formatierung wird ignoriert und die Formatierung des eingefügten Textes basiert auf der Standard-HTML-Formatierung. Dadurch sieht der Text so aus, wie er in Browsern gerendert wird.

Wann*useBuilderFormatting* Ist`WAHR` , Die Formatierung des eingefügten Textes basiert auf[`DocumentBuilder`](../) Formatierung, und der Text sieht aus, als wäre er mit eingefügt worden[`Write`](../write/) .

## Beispiele

Zeigt, wie die Formatierung eines Document Builders beim Einfügen von HTML-Inhalten angewendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Legen Sie eine Textausrichtung für den Builder fest, fügen Sie einen HTML-Absatz mit einer angegebenen Ausrichtung und einen ohne ein.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Distributed;
builder.InsertHtml(
    "<p align='right'>Paragraph 1.</p>" +
    "<p>Paragraph 2.</p>", useBuilderFormatting);

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// Für den ersten Absatz ist eine Ausrichtung angegeben. Wenn InsertHtml den HTML-Code analysiert,
// Der im HTML-Code gefundene Absatzausrichtungswert ersetzt immer den Wert des Document Builders.
Assert.AreEqual("Paragraph 1.", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

// Für den zweiten Absatz ist keine Ausrichtung angegeben. Der Ausrichtungswert kann ausgefüllt werden
// durch den Builder-Wert, abhängig von der Flagge, die wir an die InsertHtml-Methode übergeben haben.
Assert.AreEqual("Paragraph 2.", paragraphs[1].GetText().Trim());
Assert.AreEqual(useBuilderFormatting ? ParagraphAlignment.Distributed : ParagraphAlignment.Left,
    paragraphs[1].ParagraphFormat.Alignment);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtmlWithFormatting.docx");
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertHtml(*string, [HtmlInsertOptions](../../htmlinsertoptions/)*) {#inserthtml_1}

Fügt eine HTML-Zeichenfolge in das Dokument ein. Ermöglicht die Angabe zusätzlicher Optionen.

```csharp
public void InsertHtml(string html, HtmlInsertOptions options)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| html | String | Eine HTML-Zeichenfolge zum Einfügen in das Dokument. |
| options | HtmlInsertOptions | Optionen, die beim Einfügen einer HTML-Zeichenfolge verwendet werden. |

## Bemerkungen

Mit dieser Methode können Sie ein HTML-Fragment oder ein ganzes HTML-Dokument einfügen.

## Beispiele

Zeigt, wie Optionen beim Einfügen von HTML verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD Name ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD EMAIL ");
builder.InsertParagraph();

// Standardmäßig fügt „DocumentBuilder.InsertHtml“ ein HTML-Fragment ein, das mit einem HTML-Element auf Blockebene endet.
// Normalerweise wird das Element auf Blockebene geschlossen und ein Absatzumbruch eingefügt.
// Als Ergebnis erscheint nach dem eingefügten Dokument ein neuer leerer Absatz.
// Wenn wir „HtmlInsertOptions.RemoveLastEmptyParagraph“ angeben, werden diese zusätzlichen leeren Absätze entfernt.
builder.MoveToMergeField("NAME");
builder.InsertHtml("<p>John Smith</p>", HtmlInsertOptions.UseBuilderFormatting | HtmlInsertOptions.RemoveLastEmptyParagraph);
builder.MoveToMergeField("EMAIL");
builder.InsertHtml("<p>jsmith@example.com</p>", HtmlInsertOptions.UseBuilderFormatting);

doc.Save(ArtifactsDir + "MailMerge.RemoveLastEmptyParagraph.docx");
```

### Siehe auch

* enum [HtmlInsertOptions](../../htmlinsertoptions/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
