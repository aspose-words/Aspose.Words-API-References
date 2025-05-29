---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
linktitle: ExportDropDownFormFieldAsText
articleTitle: ExportDropDownFormFieldAsText
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft HtmlSaveOptions ExportDropDownFormFieldAsText Ihre HTML/MHTML-Exporte durch die Steuerung von Dropdown-Feldformaten verbessert. Optimieren Sie Ihre Dokumente!
type: docs
weight: 130
url: /de/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

Steuert, wie Dropdown-Formularfelder in HTML oder MHTML gespeichert werden. Der Standardwert ist`FALSCH` .

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

## Bemerkungen

Bei Einstellung auf`WAHR` , exportiert Dropdown-Formularfelder als normalen Text. Wenn`FALSCH`, exportiert Dropdown-Formularfelder als SELECT-Element in HTML.

Beim Exportieren in EPUB werden Text-Dropdown-Formularfelder aufgrund der Anforderungen dieses Formats immer als Text gespeichert.

## Beispiele

Zeigt, wie Dropdown-Kombinationsfeld-Formularfelder beim Speichern im HTML-Format in den Absatztext integriert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Verwenden Sie einen Dokumentgenerator, um ein Kombinationsfeld mit dem ausgewählten Wert „Zwei“ einzufügen.
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// Das Flag "ExportDropDownFormFieldAsText" dieses SaveOptions-Objekts ermöglicht es uns,
// Steuern Sie, wie beim Speichern des Dokuments im HTML-Format mit Dropdown-Kombinationsfeldern verfahren wird.
// Wenn Sie es auf "true" setzen, wird jedes Kombinationsfeld in einfachen Text umgewandelt
// das den aktuell ausgewählten Wert des Kombinationsfelds anzeigt und ihn effektiv einfriert.
// Wenn Sie es auf „false“ setzen, bleibt die Funktionalität des Kombinationsfelds mit den Tags <select> und <option> erhalten.
HtmlSaveOptions options = new HtmlSaveOptions();
options.ExportDropDownFormFieldAsText = exportDropDownFormFieldAsText;    

doc.Save(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.DropDownFormField.html");

if (exportDropDownFormFieldAsText)
    Assert.True(outDocContents.Contains(
        "<span>Two</span>"));
else
    Assert.True(outDocContents.Contains(
        "<select name=\"MyComboBox\">" +
            "<option>One</option>" +
            "<option selected=\"selected\">Two</option>" +
            "<option>Three</option>" +
        "</select>"));
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
