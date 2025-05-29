---
title: HtmlSaveOptions.ExportXhtmlTransitional
linktitle: ExportXhtmlTransitional
articleTitle: ExportXhtmlTransitional
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihr HTML mit der Eigenschaft HtmlSaveOptions ExportXhtmlTransitional. Steuern Sie DOCTYPE-Deklarationen für bessere Kompatibilität in den Formaten HTML, MHTML und EPUB.
type: docs
weight: 280
url: /de/net/aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/
---
## HtmlSaveOptions.ExportXhtmlTransitional property

Gibt an, ob die DOCTYPE-Deklaration beim Speichern in HTML oder MHTML geschrieben werden soll. Wenn`WAHR` , schreibt eine DOCTYPE-Deklaration in das Dokument vor dem Stammelement. Der Standardwert ist`FALSCH`. Beim Speichern im EPUB- oder HTML5-Format (Html5 ) wird immer die DOCTYPE -Deklaration geschrieben.

```csharp
public bool ExportXhtmlTransitional { get; set; }
```

## Bemerkungen

Aspose.Words schreibt unabhängig von dieser Einstellung immer wohlgeformtes HTML.

Wann`WAHR`, sieht der Anfang des HTML-Ausgabedokuments folgendermaßen aus:

Aspose.Words zielt darauf ab, XHTML gemäß der XHTML 1.0 Transitional Specification auszugeben, die Ausgabe wird jedoch nicht immer mit der DTD validiert. Einige Strukturen innerhalb eines Microsoft Word Dokuments lassen sich nur schwer oder gar nicht einem Dokument zuordnen, das mit dem XHTML-Schema validiert wird. Beispielsweise erlaubt XHTML keine verschachtelten Listen (UL kann nicht in einem anderen UL-Element verschachtelt werden), in Microsoft Word-Dokumenten kommen jedoch häufig mehrstufige Listen vor.

```csharp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
<!DOCTYPE html
      PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```

## Beispiele

Zeigt, wie eine DOCTYPE-Überschrift angezeigt wird, wenn Dokumente in den Übergangsstandard Xhtml 1.0 konvertiert werden.

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

// Unser Dokument enthält nur dann eine DOCTYPE-Deklarationsüberschrift, wenn wir das Flag „ExportXhtmlTransitional“ auf „true“ gesetzt haben.
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

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
