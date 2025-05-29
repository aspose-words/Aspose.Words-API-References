---
title: HtmlSaveOptions.NavigationMapLevel
linktitle: NavigationMapLevel
articleTitle: NavigationMapLevel
second_title: Aspose.Words für .NET
description: Entdecken Sie die NavigationMapLevel-Eigenschaft von HtmlSaveOptions zur Steuerung der Überschriftenebenen in EPUB-, MOBI- und AZW3-Exporten. Maximieren Sie die Sichtbarkeit Ihrer Inhalte!
type: docs
weight: 390
url: /de/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

Gibt die maximale Überschriftenebene an, die beim Export in die Formate EPUB, MOBI oder AZW3 in die Navigationskarte eingefügt wird. Der Standardwert ist`3` .

```csharp
public int NavigationMapLevel { get; set; }
```

## Bemerkungen

Die Navigationskarte ermöglicht es Benutzeragenten, eine einfache Navigation durch die Dokumentstruktur zu ermöglichen. Normalerweise entsprechen Navigationspunkte den Überschriften im Dokument. Um Überschriften bis zur Ebene**N** weisen Sie diesen Wert zu`NavigationMapLevel`.

Standardmäßig werden drei Ebenen von Überschriften ausgefüllt: Absätze von Stilen**Überschrift 1** ,**Überschrift 2** und**Überschrift 3**. Sie können diese Eigenschaft auf einen Wert zwischen 1 und 9 setzen, um die entsprechende Höchstebene anzufordern. Wenn Sie sie auf Null setzen, wird die Navigationskarte auf nur die Dokumentwurzel oder Wurzeln von Dokumentteilen reduziert.

## Beispiele

Zeigt, wie ein Inhaltsverzeichnis für Azw3-Dokumente generiert wird.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Azw3);
options.NavigationMapLevel = 2;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```

Zeigt, wie ein Inhaltsverzeichnis für Mobi-Dokumente generiert wird.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mobi);
options.NavigationMapLevel = 5;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateMobiToc.mobi", options);
```

Zeigt, wie Überschriften gefiltert werden, die im Navigationsbereich eines gespeicherten Epub-Dokuments angezeigt werden.

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

// Epub-Reader erstellen normalerweise ein Inhaltsverzeichnis für ihre Dokumente.
// Jeder Absatz mit dem Stil „Überschrift“ im Dokument erstellt einen Eintrag in diesem Inhaltsverzeichnis.
    // Wir können die Eigenschaft „NavigationMapLevel“ verwenden, um eine maximale Überschriftenebene festzulegen.
// Der Epub-Reader fügt dem Inhaltsverzeichnis keine Überschriften mit einer höheren Ebene als der von uns angegebenen hinzu.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.NavigationMapLevel = 2;

// Unser Dokument hat sechs Überschriften, von denen zwei über Ebene 2 liegen.
// Das Inhaltsverzeichnis für dieses Dokument wird vier Einträge haben.
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
