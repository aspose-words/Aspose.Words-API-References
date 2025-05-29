---
title: WordML2003SaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words per .NET
description: Scopri come la proprietà SaveFormat di WordML2003SaveOptions definisce i formati di salvataggio dei documenti. Garantisci una compatibilità perfetta con WordML per i tuoi file!
type: docs
weight: 20
url: /it/net/aspose.words.saving/wordml2003saveoptions/saveformat/
---
## WordML2003SaveOptions.SaveFormat property

Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere soloWordML .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Esempi

Mostra come gestire il contenuto grezzo del documento di output.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crea un oggetto "WordML2003SaveOptions" da passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento nel formato di salvataggio WordML.
WordML2003SaveOptions options = new WordML2003SaveOptions();

Assert.AreEqual(SaveFormat.WordML, options.SaveFormat);

// Imposta la proprietà "PrettyFormat" su "true" per applicare l'indentazione del carattere di tabulazione e
// nuove righe per rendere più facile la lettura del contenuto grezzo del documento di output.
// Impostare la proprietà "PrettyFormat" su "false" per salvare il contenuto grezzo del documento in un corpo di testo continuo.
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

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [WordML2003SaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
