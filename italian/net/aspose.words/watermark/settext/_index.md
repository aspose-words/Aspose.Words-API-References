---
title: Watermark.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words per .NET
description: Watermark SetText metodo. Aggiunge una filigrana di testo nel documento in C#.
type: docs
weight: 40
url: /it/net/aspose.words/watermark/settext/
---
## SetText(*string*) {#settext}

Aggiunge una filigrana di testo nel documento.

```csharp
public void SetText(string text)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| text | String | Testo visualizzato come filigrana. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentOutOfRangeException | Viene generato quando la lunghezza del testo è fuori intervallo o il testo contiene solo spazi bianchi. |
| ArgumentNullException | Genera quando il testo è`nullo` . |

## Osservazioni

La lunghezza del testo deve essere compresa tra 1 e 200 inclusi. Il testo non può essere`nullo` o contenere solo spazi.

## Esempi

Mostra come creare una filigrana di testo.

```csharp
Document doc = new Document();

// Aggiunge una filigrana di testo semplice.
doc.Watermark.SetText("Aspose Watermark");

// Se desideriamo modificare la formattazione del testo utilizzandolo come filigrana,
// possiamo farlo passando un oggetto TextWatermarkOptions durante la creazione della filigrana.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Possiamo rimuovere una filigrana da un documento come questo.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Guarda anche

* class [Watermark](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## SetText(*string, [TextWatermarkOptions](../../textwatermarkoptions/)*) {#settext_1}

Aggiunge una filigrana di testo nel documento.

```csharp
public void SetText(string text, TextWatermarkOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| text | String | Testo visualizzato come filigrana. |
| options | TextWatermarkOptions | Definisce opzioni aggiuntive per la filigrana del testo. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentOutOfRangeException | Viene generato quando la lunghezza del testo è fuori intervallo o il testo contiene solo spazi bianchi. |
| ArgumentNullException | Genera quando il testo è`nullo` . |

## Osservazioni

La lunghezza del testo deve essere compresa tra 1 e 200 inclusi. Il testo non può essere`nullo` o contenere solo spazi.

Se[`TextWatermarkOptions`](../../textwatermarkoptions/) È`nullo`, la filigrana verrà impostata con le opzioni predefinite.

## Esempi

Mostra come creare una filigrana di testo.

```csharp
Document doc = new Document();

// Aggiunge una filigrana di testo semplice.
doc.Watermark.SetText("Aspose Watermark");

// Se desideriamo modificare la formattazione del testo utilizzandolo come filigrana,
// possiamo farlo passando un oggetto TextWatermarkOptions durante la creazione della filigrana.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Possiamo rimuovere una filigrana da un documento come questo.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Guarda anche

* class [TextWatermarkOptions](../../textwatermarkoptions/)
* class [Watermark](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
