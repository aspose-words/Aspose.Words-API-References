---
title: PageVerticalAlignment Enum
linktitle: PageVerticalAlignment
articleTitle: PageVerticalAlignment
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.PageVerticalAlignment per un allineamento ottimale del testo sulle pagine. Migliora il layout del tuo documento con una giustificazione verticale precisa!
type: docs
weight: 5100
url: /it/net/aspose.words/pageverticalalignment/
---
## PageVerticalAlignment enumeration

Specifica la giustificazione verticale del testo su ogni pagina.

```csharp
public enum PageVerticalAlignment
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Bottom | `3` | Il testo è allineato in fondo alla pagina. |
| Center | `1` | Il testo è allineato al centro della pagina. |
| Justify | `2` | Il testo è distribuito per riempire la pagina. |
| Top | `0` | Il testo è allineato nella parte superiore della pagina. |

## Esempi

Mostra come applicare e ripristinare le impostazioni di impostazione della pagina alle sezioni di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifica le proprietà di impostazione della pagina per la sezione corrente del builder e aggiungi del testo.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Se iniziamo una nuova sezione utilizzando un generatore di documenti,
// erediterà le proprietà di impostazione della pagina corrente del builder.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Possiamo ripristinare i valori predefiniti delle proprietà di impostazione della pagina utilizzando il metodo "ClearFormatting".
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### Guarda anche

* class [PageSetup](../pagesetup/)
* property [VerticalAlignment](../pagesetup/verticalalignment/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
