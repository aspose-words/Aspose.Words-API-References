---
title: TxtLoadOptions.TrailingSpacesOptions
linktitle: TrailingSpacesOptions
articleTitle: TrailingSpacesOptions
second_title: Aspose.Words per .NET
description: TxtLoadOptions TrailingSpacesOptions proprietà. Ottiene o imposta lopzione preferita per la gestione dello spazio finale. Il valore predefinito èTrim  in C#.
type: docs
weight: 60
url: /it/net/aspose.words.loading/txtloadoptions/trailingspacesoptions/
---
## TxtLoadOptions.TrailingSpacesOptions property

Ottiene o imposta l'opzione preferita per la gestione dello spazio finale. Il valore predefinito èTrim .

```csharp
public TxtTrailingSpacesOptions TrailingSpacesOptions { get; set; }
```

## Esempi

Mostra come tagliare gli spazi bianchi durante il caricamento di documenti di testo normale.

```csharp
string textDoc = "      Line 1 \n" +
                 "    Line 2   \n" +
                 " Line 3       ";

// Crea un oggetto "TxtLoadOptions", che possiamo passare al costruttore di un documento
// per modificare il modo in cui carichiamo un documento di testo normale.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Imposta la proprietà "LeadingSpacesOptions" su "TxtLeadingSpacesOptions.Preserve"
// per preservare tutti gli spazi bianchi all'inizio di ogni riga.
// Imposta la proprietà "LeadingSpacesOptions" su "TxtLeadingSpacesOptions.ConvertToIndent"
// per rimuovere tutti gli spazi bianchi dall'inizio di ogni riga,
// e quindi applica un rientro della prima riga a sinistra al paragrafo per simulare l'effetto degli spazi bianchi.
// Imposta la proprietà "LeadingSpacesOptions" su "TxtLeadingSpacesOptions.Trim"
// per rimuovere tutti i caratteri di spazio bianco dall'inizio di ogni riga.
loadOptions.LeadingSpacesOptions = txtLeadingSpacesOptions;

// Imposta la proprietà "TrailingSpacesOptions" su "TxtTrailingSpacesOptions.Preserve"
 // per preservare tutti gli spazi bianchi alla fine di ogni riga.
 // Imposta la proprietà "TrailingSpacesOptions" su "TxtTrailingSpacesOptions.Trim" su
// rimuove tutti gli spazi bianchi dalla fine di ogni riga.
loadOptions.TrailingSpacesOptions = txtTrailingSpacesOptions;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

switch (txtLeadingSpacesOptions)
{
    case TxtLeadingSpacesOptions.ConvertToIndent:
        Assert.AreEqual(37.8d, paragraphs[0].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(25.2d, paragraphs[1].ParagraphFormat.FirstLineIndent);
        Assert.AreEqual(6.3d, paragraphs[2].ParagraphFormat.FirstLineIndent);

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
    case TxtLeadingSpacesOptions.Preserve:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("      Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("    Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith(" Line 3"));
        break;
    case TxtLeadingSpacesOptions.Trim:
        Assert.True(paragraphs.All(p => ((Paragraph)p).ParagraphFormat.FirstLineIndent == 0.0d));

        Assert.True(paragraphs[0].GetText().StartsWith("Line 1"));
        Assert.True(paragraphs[1].GetText().StartsWith("Line 2"));
        Assert.True(paragraphs[2].GetText().StartsWith("Line 3"));
        break;
}

switch (txtTrailingSpacesOptions)
{
    case TxtTrailingSpacesOptions.Preserve:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1 \r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2   \r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3       \f"));
        break;
    case TxtTrailingSpacesOptions.Trim:
        Assert.True(paragraphs[0].GetText().EndsWith("Line 1\r"));
        Assert.True(paragraphs[1].GetText().EndsWith("Line 2\r"));
        Assert.True(paragraphs[2].GetText().EndsWith("Line 3\f"));
        break;
}
```

### Guarda anche

* enum [TxtTrailingSpacesOptions](../../txttrailingspacesoptions/)
* class [TxtLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
