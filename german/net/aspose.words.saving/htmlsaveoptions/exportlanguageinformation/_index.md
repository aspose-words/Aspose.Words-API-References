---
title: HtmlSaveOptions.ExportLanguageInformation
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt an ob Sprachinformationen in HTML MHTML oder EPUB exportiert werden. Standard istFALSCH .
type: docs
weight: 190
url: /de/net/aspose.words.saving/htmlsaveoptions/exportlanguageinformation/
---
## HtmlSaveOptions.ExportLanguageInformation property

Gibt an, ob Sprachinformationen in HTML, MHTML oder EPUB exportiert werden. Standard ist`FALSCH` .

```csharp
public bool ExportLanguageInformation { get; set; }
```

### Bemerkungen

Wenn diese Eigenschaft auf eingestellt ist`Stimmt` Aspose.Words-Ausgaben **lang** HTML-Attribut für die document -Elemente, die die Sprache angeben. Dies kann erforderlich sein, um die sprachbezogene Semantik zu erhalten.

### Beispiele

Zeigt, wie Sprachinformationen beim Speichern in .html beibehalten werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Verwenden Sie den Builder, um Text zu schreiben, während Sie ihn in verschiedenen Gebietsschemas formatieren.
builder.Font.LocaleId = new CultureInfo("en-US").LCID;
builder.Writeln("Hello world!");

builder.Font.LocaleId = new CultureInfo("en-GB").LCID;
builder.Writeln("Hello again!");

builder.Font.LocaleId = new CultureInfo("ru-RU").LCID;
builder.Write("Привет, мир!");

// Beim Speichern des Dokuments im HTML-Format können wir ein SaveOptions-Objekt übergeben
// um das Gebietsschema jedes formatierten Textes entweder beizubehalten oder zu verwerfen.
// Wenn wir das Flag "ExportLanguageInformation" auf "true" setzen,
// Das ausgegebene HTML-Dokument enthält die Locales in den "lang"-Attributen von <span> Stichworte.
// Wenn wir das Flag "ExportLanguageInformation" auf "false" setzen,
// Der Text im ausgegebenen HTML-Dokument enthält keine Gebietsschema-Informationen.
HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportLanguageInformation = exportLanguageInformation,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    Assert.True(outDocContents.Contains("<span>Hello world!</span>"));
    Assert.True(outDocContents.Contains("<span lang=\"en-GB\">Hello again!</span>"));
    Assert.True(outDocContents.Contains("<span lang=\"ru-RU\">Привет, мир!</span>"));
}
else
{
    Assert.True(outDocContents.Contains("<span>Hello world!</span>"));
    Assert.True(outDocContents.Contains("<span>Hello again!</span>"));
    Assert.True(outDocContents.Contains("<span>Привет, мир!</span>"));
}
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


