---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
linktitle: DocumentSplitHeadingLevel
articleTitle: DocumentSplitHeadingLevel
second_title: Aspose.Words für .NET
description: HtmlSaveOptions DocumentSplitHeadingLevel eigendom. Gibt die maximale Überschriftenebene an auf der das Dokument geteilt werden soll. Der Standardwert ist2  in C#.
type: docs
weight: 90
url: /de/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

Gibt die maximale Überschriftenebene an, auf der das Dokument geteilt werden soll. Der Standardwert ist`2` .

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

## Bemerkungen

Wann[`DocumentSplitCriteria`](../documentsplitcriteria/) beinhaltetHeadingParagraph und diese Eigenschaft auf einen Wert von 1 bis 9 eingestellt ist, wird das Dokument an Absätzen geteilt, die mit formatiert sind.**Überschrift 1** ,**Überschrift 2** ,**Überschrift 3**usw. Stile bis zur angegebenen Überschriftenebene.

Nur standardmäßig**Überschrift 1** Und**Überschrift 2** Absätze führen dazu, dass das Dokument geteilt wird. Wenn diese Eigenschaft auf Null gesetzt wird, wird das Dokument an Überschriftenabsätzen überhaupt nicht geteilt.

## Beispiele

Zeigt, wie ein ausgegebenes HTML-Dokument anhand von Überschriften in mehrere Teile aufgeteilt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Jeder Absatz, den wir mit dem Stil „Überschrift“ formatieren, kann als Überschrift dienen.
// Jede Überschrift kann auch eine Überschriftenebene haben, die durch die Nummer ihres Überschriftenstils bestimmt wird.
// Die folgenden Überschriften entsprechen den Ebenen 1-3.
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #1");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #2");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #3");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #4");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #5");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #6");

// Erstelle ein HtmlSaveOptions-Objekt und setze das Teilungskriterium auf „HeadingParagraph“.
// Diese Kriterien teilen das Dokument an Absätzen mit „Überschriften“-Stilen in mehrere kleinere Dokumente auf,
// und speichern Sie jedes Dokument in einer separaten HTML-Datei im lokalen Dateisystem.
// Wir werden auch die maximale Überschriftenebene festlegen, wodurch das Dokument auf 2 aufgeteilt wird.
// Beim Speichern des Dokuments wird es in die Überschriften der Ebenen 1 und 2 aufgeteilt, nicht jedoch in die Überschriften 3 bis 9.
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// Unser Dokument enthält vier Überschriften der Ebenen 1 bis 2. Eine dieser Überschriften wird es nicht sein
// ein Teilungspunkt, da er sich am Anfang des Dokuments befindet.
// Durch den Speichervorgang wird unser Dokument an drei Stellen in vier kleinere Dokumente aufgeteilt.
doc.Save(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html", options);

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html");

Assert.AreEqual("Heading #1", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-01.html");

Assert.AreEqual("Heading #2\r" +
                "Heading #3", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-02.html");

Assert.AreEqual("Heading #4", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-03.html");

Assert.AreEqual("Heading #5\r" +
                "Heading #6", doc.GetText().Trim());
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
