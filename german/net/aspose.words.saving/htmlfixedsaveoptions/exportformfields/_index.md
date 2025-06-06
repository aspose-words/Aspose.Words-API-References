---
title: HtmlFixedSaveOptions.ExportFormFields
linktitle: ExportFormFields
articleTitle: ExportFormFields
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „HtmlFixedSaveOptions ExportFormFields“ Ihre Dokumentexporte verbessert, indem sie die Formularfelder interaktiv hält und so die Benutzererfahrung verbessert.
type: docs
weight: 80
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/exportformfields/
---
## HtmlFixedSaveOptions.ExportFormFields property

Ruft ab oder legt fest, ob Formularfelder als interaktive Elemente (als „Eingabe“-Tag) exportiert und nicht in Text oder Grafiken konvertiert werden.

```csharp
public bool ExportFormFields { get; set; }
```

## Beispiele

Zeigt, wie Formularfelder in HTML exportiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertCheckBox("CheckBox", false, 15);

// Wenn wir ein Dokument mit Formularfeldern nach .html exportieren,
// Es gibt zwei Möglichkeiten, wie Aspose.Words Formularfelder exportieren kann.
// Wenn Sie das Flag „ExportFormFields“ auf „true“ setzen, werden sie als interaktive Objekte exportiert.
// Wenn Sie dieses Flag auf „false“ setzen, werden Formularfelder als einfacher Text angezeigt.
// Dadurch werden sie auf ihrem aktuellen Wert eingefroren und der Leser unseres HTML-Dokuments wird daran gehindert
// daran gehindert, mit ihnen zu interagieren.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportFormFields = exportFormFields
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportFormFields.html");

if (exportFormFields)
{
    Assert.True(Regex.Match(outDocContents,
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<input style=\"position:absolute; left:0pt; top:0pt;\" type=\"checkbox\" name=\"CheckBox\" />").Success);
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "<a name=\"CheckBox\" style=\"left:0pt; top:0pt;\"></a>" +
        "<div class=\"awdiv\" style=\"left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;\"").Success);
}
```

### Siehe auch

* class [HtmlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
