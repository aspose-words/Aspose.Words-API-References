---
title: HtmlSaveOptions.ExportDropDownFormFieldAsText
linktitle: ExportDropDownFormFieldAsText
articleTitle: ExportDropDownFormFieldAsText
second_title: Aspose.Words per .NET
description: HtmlSaveOptions ExportDropDownFormFieldAsText proprietà. Controlla il modo in cui i campi del modulo a discesa vengono salvati in HTML o MHTML. Il valore predefinito èfalso  in C#.
type: docs
weight: 130
url: /it/net/aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/
---
## HtmlSaveOptions.ExportDropDownFormFieldAsText property

Controlla il modo in cui i campi del modulo a discesa vengono salvati in HTML o MHTML. Il valore predefinito è`falso` .

```csharp
public bool ExportDropDownFormFieldAsText { get; set; }
```

## Osservazioni

Quando impostato su`VERO` , esporta i campi del modulo a discesa come testo normale. Quando`falso`, esporta i campi del modulo a discesa come elemento SELECT in HTML.

Quando si esporta in EPUB, i campi del modulo a discesa di testo vengono sempre salvati come testo a causa dei requisiti di questo formato.

## Esempi

Mostra come ottenere che i campi del modulo della casella combinata a discesa si fondano con il testo del paragrafo durante il salvataggio in HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilizzare un generatore di documenti per inserire una casella combinata con il valore "Due" selezionato.
builder.InsertComboBox("MyComboBox", new[] { "One", "Two", "Three" }, 1);

// Il flag "ExportDropDownFormFieldAsText" di questo oggetto SaveOptions ci consente di
// controlla come il salvataggio del documento in HTML tratta le caselle combinate a discesa.
// Impostandolo su "true" ogni casella combinata verrà convertita in testo semplice
// che visualizza il valore attualmente selezionato della casella combinata, bloccandolo di fatto.
// Impostandolo su "false" si manterrà la funzionalità della casella combinata utilizzando <select> e <opzione> tag.
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

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
