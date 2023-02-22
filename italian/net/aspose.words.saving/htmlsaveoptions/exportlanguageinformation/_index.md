---
title: HtmlSaveOptions.ExportLanguageInformation
second_title: Aspose.Words per .NET API Reference
description: HtmlSaveOptions proprietà. Specifica se le informazioni sulla lingua vengono esportate in HTML MHTML o EPUB. Limpostazione predefinita èfalso .
type: docs
weight: 190
url: /it/net/aspose.words.saving/htmlsaveoptions/exportlanguageinformation/
---
## HtmlSaveOptions.ExportLanguageInformation property

Specifica se le informazioni sulla lingua vengono esportate in HTML, MHTML o EPUB. L'impostazione predefinita è`falso` .

```csharp
public bool ExportLanguageInformation { get; set; }
```

### Osservazioni

Quando questa proprietà è impostata su`VERO` Uscite Aspose.Words **lang** Attributo HTML sugli elementi document che specificano la lingua. Questo può essere necessario per preservare la semantica relativa al linguaggio.

### Esempi

Mostra come preservare le informazioni sulla lingua durante il salvataggio in .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Usa il builder per scrivere il testo mentre lo formatti in diverse localizzazioni.
builder.Font.LocaleId = new CultureInfo("en-US").LCID;
builder.Writeln("Hello world!");

builder.Font.LocaleId = new CultureInfo("en-GB").LCID;
builder.Writeln("Hello again!");

builder.Font.LocaleId = new CultureInfo("ru-RU").LCID;
builder.Write("Привет, мир!");

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions
// per preservare o eliminare le impostazioni locali di ogni testo formattato.
// Se impostiamo il flag "ExportLanguageInformation" su "true",
// il documento HTML di output conterrà le impostazioni locali negli attributi "lang" di <span> tag.
// Se impostiamo il flag "ExportLanguageInformation" su "false",
// il testo nel documento HTML di output non conterrà alcuna informazione locale.
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

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlsaveoptions/)
* assemblea [Aspose.Words](../../../)


