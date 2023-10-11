---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Steuert wie DropdownFormularfelder in HTML oder MHTML gespeichert werden. Der Standardwert istFALSCH .
type: docs
weight: 130
url: /de/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

Steuert, wie Dropdown-Formularfelder in HTML oder MHTML gespeichert werden. Der Standardwert ist`FALSCH` .

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

### Bemerkungen

Wenn eingestellt auf`WAHR` , exportiert Dropdown-Formularfelder als normalen Text. Wann`FALSCH`, exportiert Dropdown-Formularfelder als SELECT-Element in HTML.

Beim Exportieren nach EPUB werden Text-Dropdown-Formularfelder aufgrund der Anforderungen dieses Formats immer als Text gespeichert.

### Beispiele

Zeigt, wie man Dropdown-Kombinationsfeld-Formularfelder beim Speichern im HTML-Format in den Absatztext einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Verwenden Sie einen Dokumentersteller, um ein Kombinationsfeld mit dem ausgewählten Wert „Zwei“ einzufügen.
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// Das Flag „ExportDropDownFormFieldAsText“ dieses SaveOptions-Objekts ermöglicht es uns
// steuern, wie beim Speichern des Dokuments in HTML Dropdown-Kombinationsfelder behandelt werden.
// Wenn Sie es auf „true“ setzen, wird jedes Kombinationsfeld in einfachen Text umgewandelt
// das den aktuell ausgewählten Wert des Kombinationsfelds anzeigt und ihn effektiv einfriert.
// Wenn Sie es auf „false“ setzen, bleibt die Funktionalität des Kombinationsfelds erhalten, indem Sie <select> verwenden. und <Option> Stichworte.
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
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


