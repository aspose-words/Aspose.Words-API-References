---
title: HtmlFixedSaveOptions.ExportFormFields
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlFixedSaveOptions eigendom. Ruft die Angabe ab ob Formularfelder als interaktive Elemente als EingabeTag exportiert und nicht in Text oder Grafiken konvertiert werden oder legt diese fest.
type: docs
weight: 80
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/exportformfields/
---
## HtmlFixedSaveOptions.ExportFormFields property

Ruft die Angabe ab, ob Formularfelder als interaktive Elemente (als „Eingabe“-Tag) exportiert und nicht in Text oder Grafiken konvertiert werden, oder legt diese fest.

```csharp
public bool ExportFormFields { get; set; }
```

### Beispiele

Zeigt, wie Formularfelder nach HTML exportiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertCheckBox("CheckBox", false, 15);

// Wenn wir ein Dokument mit Formularfeldern nach .html exportieren,
// Es gibt zwei Möglichkeiten, wie Aspose.Words Formularfelder exportieren kann.
// Wenn Sie das Flag „ExportFormFields“ auf „true“ setzen, werden sie als interaktive Objekte exportiert.
// Wenn Sie dieses Flag auf „false“ setzen, werden Formularfelder als einfacher Text angezeigt.
// Dadurch werden sie auf ihrem aktuellen Wert eingefroren und der Leser unseres HTML-Dokuments wird daran gehindert
// von der Möglichkeit, mit ihnen zu interagieren.
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
* namensraum [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* Montage [Aspose.Words](../../../)


