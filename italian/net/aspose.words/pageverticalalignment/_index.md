---
title: Enum PageVerticalAlignment
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.PageVerticalAlignment enum. Specifica la giustificazione verticale del testo su ogni pagina.
type: docs
weight: 4370
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
| Justify | `2` | Il testo viene distribuito per riempire la pagina. |
| Top | `0` | Il testo è allineato nella parte superiore della pagina. |

### Esempi

Mostra come applicare e ripristinare le impostazioni di impostazione della pagina nelle sezioni di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Modifica le proprietà di impostazione della pagina per la sezione corrente del builder e aggiunge testo.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// Se iniziamo una nuova sezione utilizzando un generatore di documenti,
// erediterà le proprietà di impostazione della pagina corrente del builder.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// Possiamo ripristinare le proprietà di impostazione della pagina ai valori predefiniti utilizzando il metodo "ClearFormatting".
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


