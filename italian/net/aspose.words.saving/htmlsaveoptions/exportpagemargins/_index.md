---
title: HtmlSaveOptions.ExportPageMargins
second_title: Aspose.Words per .NET API Reference
description: HtmlSaveOptions proprietà. Specifica se i margini della pagina vengono esportati in HTML MHTML o EPUB. Limpostazione predefinita èfalso .
type: docs
weight: 220
url: /it/net/aspose.words.saving/htmlsaveoptions/exportpagemargins/
---
## HtmlSaveOptions.ExportPageMargins property

Specifica se i margini della pagina vengono esportati in HTML, MHTML o EPUB. L'impostazione predefinita è`falso` .

```csharp
public bool ExportPageMargins { get; set; }
```

### Osservazioni

Aspose.Words non mostra l'area dei margini della pagina per impostazione predefinita. Se alcuni elementi sono completamente o parzialmente tagliati dal bordo del documento, l'area visualizzata può essere estesa con questa opzione.

### Esempi

Mostra come mostrare gli oggetti fuori limite nei documenti HTML di output.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Usa un builder per inserire una forma senza avvolgimento.
Shape shape = builder.InsertShape(ShapeType.Cube, 200, 200);

shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.WrapType = WrapType.None;

// I valori di posizione della forma negativi possono posizionare la forma al di fuori dei limiti della pagina.
// Se esportiamo questo in HTML, la forma apparirà troncata.
shape.Left = -150;

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions
// per decidere se regolare la pagina per visualizzare completamente gli oggetti fuori limite.
// Se impostiamo il flag "ExportPageMargins" su "true", la forma sarà completamente visibile nell'HTML di output.
// Se impostiamo il flag "ExportPageMargins" su "false",
// il nostro documento visualizzerà la forma troncata come la vedremmo in Microsoft Word.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageMargins = exportPageMargins };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    Assert.True(outDocContents.Contains("<style type=\"text/css\">div.Section1 { margin:70.85pt }</style>"));
    Assert.True(outDocContents.Contains("<div class=\"Section1\"><p style=\"margin-top:0pt; margin-left:151pt; margin-bottom:0pt\">"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));
    Assert.True(outDocContents.Contains("<div><p style=\"margin-top:0pt; margin-left:221.85pt; margin-bottom:0pt\">"));
}
```

### Guarda anche

* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlsaveoptions/)
* assemblea [Aspose.Words](../../../)


