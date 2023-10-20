---
title: HtmlSaveOptions.ExportXhtmlTransitional
linktitle: ExportXhtmlTransitional
articleTitle: ExportXhtmlTransitional
second_title: Aspose.Words für .NET
description: HtmlSaveOptions ExportXhtmlTransitional eigendom. Gibt an ob die DOCTYPEDeklaration beim Speichern in HTML oder MHTML geschrieben werden soll. WannWAHR  schreibt eine DOCTYPEDeklaration in das Dokument vor dem Wurzelelement. Der Standardwert istFALSCH. Beim Speichern in EPUB oder HTML5 Html5  Die DOCTYPE Deklaration wird immer geschrieben in C#.
type: docs
weight: 280
url: /de/net/aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/
---
## HtmlSaveOptions.ExportXhtmlTransitional property

Gibt an, ob die DOCTYPE-Deklaration beim Speichern in HTML oder MHTML geschrieben werden soll. Wann`WAHR` , schreibt eine DOCTYPE-Deklaration in das Dokument vor dem Wurzelelement. Der Standardwert ist`FALSCH`. Beim Speichern in EPUB oder HTML5 (Html5 ) Die DOCTYPE -Deklaration wird immer geschrieben.

```csharp
public bool ExportXhtmlTransitional { get; set; }
```

## Bemerkungen

Aspose.Words schreibt unabhängig von dieser Einstellung immer wohlgeformtes HTML.

Wann`WAHR`, der Anfang des HTML-Ausgabedokuments sieht folgendermaßen aus:

Aspose.Words zielt darauf ab, XHTML gemäß der XHTML 1.0 Transitional-Spezifikation auszugeben, aber die Ausgabe wird nicht immer anhand der DTD validiert. Einige Strukturen in einem Microsoft Word -Dokument lassen sich nur schwer oder gar nicht einem Dokument zuordnen, das anhand des XHTML-Schemas validiert werden kann. Beispielsweise erlaubt XHTML keine verschachtelten Listen (UL kann nicht in einem anderen UL-Element verschachtelt werden), , aber in Microsoft Word-Dokumenten kommen mehrstufige Listen recht häufig vor.

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

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        "<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>\r\n" +
        "<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">\r\n" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
