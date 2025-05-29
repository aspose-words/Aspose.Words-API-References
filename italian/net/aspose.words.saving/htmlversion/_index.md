---
title: HtmlVersion Enum
linktitle: HtmlVersion
articleTitle: HtmlVersion
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Saving.HtmlVersion per ottimizzare il salvataggio dei documenti nei formati HTML e MHTML, migliorando compatibilità e prestazioni.
type: docs
weight: 5870
url: /it/net/aspose.words.saving/htmlversion/
---
## HtmlVersion enumeration

Indica la versione HTML utilizzata quando si salva il documentoHtml e Mhtml formati.

```csharp
public enum HtmlVersion
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Xhtml | `0` | Salva il documento in conformità con lo standard XHTML 1.0 Transitional. |
| Html5 | `1` | Salva il documento in conformità con lo standard HTML 5. |

## Esempi

Mostra come visualizzare un'intestazione DOCTYPE durante la conversione di documenti nello standard di transizione Xhtml 1.0.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = HtmlVersion.Xhtml,
    ExportXhtmlTransitional = showDoctypeDeclaration,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// Il nostro documento conterrà un'intestazione di dichiarazione DOCTYPE solo se abbiamo impostato il flag "ExportXhtmlTransitional" su "true".
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");
string newLine = Environment.NewLine;

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        $"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{newLine}" +
        $"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{newLine}" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

Mostra come salvare un documento in una versione specifica di HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = htmlVersion,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.HtmlVersions.html", options);

// I nostri documenti HTML presenteranno piccole differenze per essere compatibili con le diverse versioni HTML.
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.HtmlVersions.html");

switch (htmlVersion)
{
    case HtmlVersion.Html5:
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<a id=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<table style=\"padding:0pt; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
        break;
    case HtmlVersion.Xhtml:
        Assert.True(outDocContents.Contains("<a name=\"_Toc76372689\"></a>"));
        Assert.True(outDocContents.Contains("<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
        Assert.True(outDocContents.Contains("<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
        break;
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
