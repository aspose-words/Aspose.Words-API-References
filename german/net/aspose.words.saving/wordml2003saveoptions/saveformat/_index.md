---
title: WordML2003SaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die SaveFormat-Eigenschaft von WordML2003SaveOptions Dokumentspeicherformate definiert. Stellen Sie die nahtlose Kompatibilität Ihrer Dateien mit WordML sicher!
type: docs
weight: 20
url: /de/net/aspose.words.saving/wordml2003saveoptions/saveformat/
---
## WordML2003SaveOptions.SaveFormat property

Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nurWordML .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Beispiele

Zeigt, wie der Rohinhalt des Ausgabedokuments verwaltet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Erstellen Sie ein "WordML2003SaveOptions"-Objekt, das an die "Save"-Methode des Dokuments übergeben wird
// um die Art und Weise zu ändern, wie wir das Dokument im WordML-Speicherformat speichern.
WordML2003SaveOptions options = new WordML2003SaveOptions();

Assert.AreEqual(SaveFormat.WordML, options.SaveFormat);

// Setzen Sie die Eigenschaft "PrettyFormat" auf "true", um die Einrückung von Tabulatorzeichen anzuwenden und
// Zeilenumbrüche, um den Rohinhalt des Ausgabedokuments leichter lesbar zu machen.
// Setzen Sie die Eigenschaft „PrettyFormat“ auf „false“, um den Rohinhalt des Dokuments in einem fortlaufenden Textkörper zu speichern.
options.PrettyFormat = prettyFormat;

doc.Save(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml", options);

string fileContents = File.ReadAllText(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml");
string newLine = Environment.NewLine;

if (prettyFormat)
    Assert.True(fileContents.Contains(
        $"<o:DocumentProperties>{newLine}\t\t" +
            $"<o:Revision>1</o:Revision>{newLine}\t\t" +
            $"<o:TotalTime>0</o:TotalTime>{newLine}\t\t" +
            $"<o:Pages>1</o:Pages>{newLine}\t\t" +
            $"<o:Words>0</o:Words>{newLine}\t\t" +
            $"<o:Characters>0</o:Characters>{newLine}\t\t" +
            $"<o:Lines>1</o:Lines>{newLine}\t\t" +
            $"<o:Paragraphs>1</o:Paragraphs>{newLine}\t\t" +
            $"<o:CharactersWithSpaces>0</o:CharactersWithSpaces>{newLine}\t\t" +
            $"<o:Version>11.5606</o:Version>{newLine}\t" +
        "</o:DocumentProperties>"));
else
    Assert.True(fileContents.Contains(
        "<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>" +
        "<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" +
        "<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
```

### Siehe auch

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [WordML2003SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
