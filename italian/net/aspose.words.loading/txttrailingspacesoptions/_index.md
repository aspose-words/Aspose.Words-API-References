---
title: Enum TxtTrailingSpacesOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Loading.TxtTrailingSpacesOptions enum. Specifica le opzioni disponibili per la gestione degli spazi finali durante limportazione daText file.
type: docs
weight: 3740
url: /it/net/aspose.words.loading/txttrailingspacesoptions/
---
## TxtTrailingSpacesOptions enumeration

Specifica le opzioni disponibili per la gestione degli spazi finali durante l'importazione daText file.

```csharp
public enum TxtTrailingSpacesOptions
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Trim | `0` |  |
| Preserve | `1` |  |

### Esempi

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

* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading/)
* assemblea [Aspose.Words](../../)


