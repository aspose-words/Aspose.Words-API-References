---
title: HtmlSaveOptions.ExportPageMargins
linktitle: ExportPageMargins
articleTitle: ExportPageMargins
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ExportPageMargins di HtmlSaveOptions migliora le tue esportazioni HTML, MHTML ed EPUB controllando i margini di pagina per una presentazione impeccabile.
type: docs
weight: 210
url: /it/net/aspose.words.saving/htmlsaveoptions/exportpagemargins/
---
## HtmlSaveOptions.ExportPageMargins property

Specifica se i margini della pagina vengono esportati in HTML, MHTML o EPUB. Il valore predefinito è`falso` .

```csharp
public bool ExportPageMargins { get; set; }
```

## Osservazioni

Per impostazione predefinita, Aspose.Words non mostra l'area dei margini della pagina. Se uno qualsiasi degli elementi viene tagliato completamente o parzialmente dal bordo del documento, l'area visualizzata può essere estesa con questa opzione.

## Esempi

Mostra come visualizzare oggetti fuori dai limiti nei documenti HTML di output.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilizzare un builder per inserire una forma senza avvolgimento.
Shape shape = builder.InsertShape(ShapeType.Cube, 200, 200);

shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.WrapType = WrapType.None;

// I valori negativi per la posizione della forma potrebbero posizionare la forma al di fuori dei limiti della pagina.
// Se esportiamo questo in HTML, la forma apparirà troncata.
shape.Left = -150;

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions
// per decidere se adattare la pagina in modo da visualizzare completamente gli oggetti fuori dai limiti.
// Se impostiamo il flag "ExportPageMargins" su "true", la forma sarà completamente visibile nell'HTML di output.
// Se impostiamo il flag "ExportPageMargins" su "false",
// il nostro documento visualizzerà la forma troncata, così come la vedremmo in Microsoft Word.
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
