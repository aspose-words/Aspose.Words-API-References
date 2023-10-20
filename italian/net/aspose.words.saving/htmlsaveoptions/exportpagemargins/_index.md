---
title: HtmlSaveOptions.ExportPageMargins
linktitle: ExportPageMargins
articleTitle: ExportPageMargins
second_title: Aspose.Words per .NET
description: HtmlSaveOptions ExportPageMargins proprietà. Specifica se i margini della pagina vengono esportati in HTML MHTML o EPUB. Limpostazione predefinita èfalso  in C#.
type: docs
weight: 210
url: /it/net/aspose.words.saving/htmlsaveoptions/exportpagemargins/
---
## HtmlSaveOptions.ExportPageMargins property

Specifica se i margini della pagina vengono esportati in HTML, MHTML o EPUB. L'impostazione predefinita è`falso` .

```csharp
public bool ExportPageMargins { get; set; }
```

## Osservazioni

Aspose.Words non mostra l'area dei margini della pagina per impostazione predefinita. Se qualche elemento è completamente o parzialmente tagliato dal bordo del documento, l'area visualizzata può essere estesa con questa opzione.

## Esempi

Mostra come mostrare oggetti fuori limite nei documenti HTML di output.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilizza un generatore per inserire una forma senza avvolgimento.
Shape shape = builder.InsertShape(ShapeType.Cube, 200, 200);

shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.WrapType = WrapType.None;

// Valori di posizione della forma negativi possono posizionare la forma fuori dai limiti della pagina.
// Se lo esportiamo in HTML, la forma apparirà troncata.
shape.Left = -150;

// Quando si salva il documento in HTML, possiamo passare un oggetto SaveOptions
// per decidere se modificare la pagina per visualizzare completamente gli oggetti fuori limite.
// Se impostiamo il flag "ExportPageMargins" su "true", la forma sarà completamente visibile nell'HTML di output.
// Se impostiamo il flag "ExportPageMargins" su "false",
// il nostro documento visualizzerà la forma troncata come la vedremmo in Microsoft Word.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageMargins = exportPageMargins };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    Assert.True(outDocContents.Contains("<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    Assert.True(outDocContents.Contains("<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));
    Assert.True(outDocContents.Contains("<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
