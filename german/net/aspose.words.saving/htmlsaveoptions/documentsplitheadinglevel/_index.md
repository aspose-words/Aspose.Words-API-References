---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
linktitle: DocumentSplitHeadingLevel
articleTitle: DocumentSplitHeadingLevel
second_title: Aspose.Words für .NET
description: Optimieren Sie die Dokumentaufteilung mit DocumentSplitHeadingLevel von HtmlSaveOptions. Steuern Sie die Überschriftenebenen für eine bessere Organisation. Standardmäßig auf 2 eingestellt.
type: docs
weight: 90
url: /de/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

Gibt die maximale Überschriftenebene an, bei der das Dokument aufgeteilt werden soll. Der Standardwert ist`2` .

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

## Bemerkungen

Wann[`DocumentSplitCriteria`](../documentsplitcriteria/) beinhaltetHeadingParagraph und diese Eigenschaft ist auf einen Wert zwischen 1 und 9 eingestellt, dann wird das Dokument in Absätze aufgeteilt, die mit formatiert sind.**Überschrift 1** ,**Überschrift 2** ,**Überschrift 3**usw. Stile bis zur angegebenen Überschriftenebene.

Standardmäßig nur**Überschrift 1** Und**Überschrift 2** Absätze führen dazu, dass das Dokument aufgeteilt wird. Wenn Sie diese Eigenschaft auf Null setzen, wird das Dokument bei Überschriftenabsätzen überhaupt nicht aufgeteilt.

## Beispiele

Zeigt, wie ein ausgegebenes HTML-Dokument anhand von Überschriften in mehrere Teile aufgeteilt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Jeder Absatz, den wir mit einem „Überschrift“-Stil formatieren, kann als Überschrift dienen.
// Jede Überschrift kann auch eine Überschriftenebene haben, die durch die Nummer ihres Überschriftenstils bestimmt wird.
// Die folgenden Überschriften beziehen sich auf die Ebenen 1–3.
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

// Erstellen Sie ein HtmlSaveOptions-Objekt und legen Sie die Aufteilungskriterien auf „HeadingParagraph“ fest.
// Diese Kriterien teilen das Dokument an Absätzen mit dem Stil "Überschrift" in mehrere kleinere Dokumente auf,
// und speichern Sie jedes Dokument in einer separaten HTML-Datei im lokalen Dateisystem.
// Wir legen auch die maximale Überschriftenebene fest, die das Dokument in zwei Teile aufteilt.
// Beim Speichern des Dokuments wird es in Überschriften der Ebenen 1 und 2 aufgeteilt, nicht jedoch in Überschriften der Ebenen 3 bis 9.
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// Unser Dokument hat vier Überschriften der Ebenen 1 - 2. Eine dieser Überschriften wird nicht
// ein Teilungspunkt, da er sich am Anfang des Dokuments befindet.
// Der Speichervorgang teilt unser Dokument an drei Stellen in vier kleinere Dokumente auf.
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
