---
title: HtmlFixedSaveOptions.SaveFontFaceCssSeparately
linktitle: SaveFontFaceCssSeparately
articleTitle: SaveFontFaceCssSeparately
second_title: Aspose.Words per .NET
description: HtmlFixedSaveOptions SaveFontFaceCssSeparately proprietà. Il flag indica se le regole CSS fontface devono essere inserite in un file separato fontFaces.css quando un documento viene salvato con un foglio di stile esterno ovvero quandoExportEmbeddedCss èfalso . Il valore predefinito èfalso  tutte le regole CSS vengono scritte in un unico file styles.css in C#.
type: docs
weight: 160
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/
---
## HtmlFixedSaveOptions.SaveFontFaceCssSeparately property

Il flag indica se le regole CSS "@font-face" devono essere inserite in un file separato "fontFaces.css" quando un documento viene salvato con un foglio di stile esterno (ovvero quando[`ExportEmbeddedCss`](../exportembeddedcss/) è`falso` ). Il valore predefinito è`falso` , tutte le regole CSS vengono scritte in un unico file "styles.css".

```csharp
public bool SaveFontFaceCssSeparately { get; set; }
```

## Osservazioni

Impostazione di questa proprietà su`VERO` ripristina il vecchio comportamento (file separati) per compatibilità con il codice legacy.

## Esempi

Mostra come inserire CSS in un file separato e aggiungere un prefisso a tutti i nomi delle classi CSS.

```csharp
Document doc = new Document(MyDir + "Bookmarks.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    CssClassNamesPrefix = "myprefix",
    SaveFontFaceCssSeparately = true
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html");

Assert.True(Regex.Match(outDocContents,
    "<div class=\"myprefixdiv myprefixpage\" style=\"width:595[.]3pt; height:841[.]9pt;\">" +
    "<div class=\"myprefixdiv\" style=\"left:85[.]05pt; top:36pt; clip:rect[(]0pt,510[.]25pt,74[.]95pt,-85.05pt[)];\">" +
    "<span class=\"myprefixspan myprefixtext001\" style=\"font-size:11pt; left:294[.]73pt; top:0[.]36pt; line-height:12[.]29pt;\">").Success);

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css");

Assert.True(Regex.Match(outDocContents,
    ".myprefixdiv { position:absolute; } " +
    ".myprefixspan { position:absolute; white-space:pre; color:#000000; font-size:12pt; }").Success);
```

### Guarda anche

* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
