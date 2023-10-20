---
title: HtmlFixedSaveOptions.ExportFormFields
linktitle: ExportFormFields
articleTitle: ExportFormFields
second_title: Aspose.Words per .NET
description: HtmlFixedSaveOptions ExportFormFields proprietà. Ottiene o imposta lindicazione se i campi del modulo vengono esportati come elementi interattivi come tag input anziché convertiti in testo o grafica in C#.
type: docs
weight: 80
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/exportformfields/
---
## HtmlFixedSaveOptions.ExportFormFields property

Ottiene o imposta l'indicazione se i campi del modulo vengono esportati come elementi interattivi (come tag 'input') anziché convertiti in testo o grafica.

```csharp
public bool ExportFormFields { get; set; }
```

## Esempi

Mostra come esportare i campi del modulo in Html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertCheckBox("CheckBox", false, 15);

// Quando esportiamo un documento con campi modulo in .html,
// ci sono due modi in cui Aspose.Words può esportare i campi del modulo.
// Impostando il flag "ExportFormFields" su "true" li esporterai come oggetti interattivi.
// Impostando questo flag su "false" verranno visualizzati i campi del modulo come testo semplice.
// Questo li congelerà al loro valore corrente e impedirà la lettura del nostro documento HTML
// dalla possibilità di interagire con loro.
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

### Guarda anche

* class [HtmlFixedSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
