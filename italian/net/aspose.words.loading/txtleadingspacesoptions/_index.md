---
title: TxtLeadingSpacesOptions Enum
linktitle: TxtLeadingSpacesOptions
articleTitle: TxtLeadingSpacesOptions
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words TxtLeadingSpacesOptions per una gestione efficiente degli spazi iniziali durante l'importazione di file di testo. Ottimizza l'elaborazione dei tuoi documenti oggi stesso!
type: docs
weight: 4180
url: /it/net/aspose.words.loading/txtleadingspacesoptions/
---
## TxtLeadingSpacesOptions enumeration

Specifica le opzioni disponibili per la gestione dello spazio iniziale durante l'importazione daText file.

```csharp
public enum TxtLeadingSpacesOptions
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| ConvertToIndent | `0` | Gli spazi iniziali vengono rimossi e convertiti in rientro sinistro. |
| Trim | `1` | Gli spazi iniziali vengono tagliati |
| Preserve | `2` | Gli spazi iniziali vengono mantenuti. |

## Esempi

Mostra come tagliare gli spazi vuoti quando si caricano documenti di testo normale.

```csharp
string textDoc = "      Line 1 \n" +
                 "    Line 2   \n" +
                 " Line 3       ";

// Creiamo un oggetto "TxtLoadOptions", che possiamo passare al costruttore di un documento
// per modificare il modo in cui carichiamo un documento di testo normale.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Imposta la proprietà "LeadingSpacesOptions" su "TxtLeadingSpacesOptions.Preserve"
// per preservare tutti gli spazi vuoti all'inizio di ogni riga.
// Imposta la proprietà "LeadingSpacesOptions" su "TxtLeadingSpacesOptions.ConvertToIndent"
// per rimuovere tutti i caratteri di spazio vuoto dall'inizio di ogni riga,
// e quindi applica un rientro a sinistra della prima riga del paragrafo per simulare l'effetto degli spazi vuoti.
// Imposta la proprietà "LeadingSpacesOptions" su "TxtLeadingSpacesOptions.Trim"
// per rimuovere tutti gli spazi vuoti dall'inizio di ogni riga.
loadOptions.LeadingSpacesOptions = txtLeadingSpacesOptions;

// Imposta la proprietà "TrailingSpacesOptions" su "TxtTrailingSpacesOptions.Preserve"
 // per preservare tutti gli spazi vuoti alla fine di ogni riga.
 // Imposta la proprietà "TrailingSpacesOptions" su "TxtTrailingSpacesOptions.Trim" per
// rimuove tutti gli spazi vuoti dalla fine di ogni riga.
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
