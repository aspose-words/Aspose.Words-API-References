---
title: TxtSaveOptions.AddBidiMarks
second_title: Aspose.Words per .NET API Reference
description: TxtSaveOptions proprietà. Specifica se aggiungere contrassegni bidirezionali prima di ogni esecuzione BiDi durante lesportazione in formato testo normale.
type: docs
weight: 20
url: /it/net/aspose.words.saving/txtsaveoptions/addbidimarks/
---
## TxtSaveOptions.AddBidiMarks property

Specifica se aggiungere contrassegni bidirezionali prima di ogni esecuzione BiDi durante l'esportazione in formato testo normale.

Il valore predefinito è **falso**.

```csharp
public bool AddBidiMarks { get; set; }
```

### Esempi

Mostra come inserire il carattere Unicode "MARK DA DESTRA A SINISTRA" (U+200F) prima di ogni Run bidirezionale nel testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.ParagraphFormat.Bidi = true;
builder.Writeln("שלום עולם!");
builder.Writeln("مرحبا بالعالم!");

// Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento come testo normale.
TxtSaveOptions saveOptions = new TxtSaveOptions { Encoding = System.Text.Encoding.Unicode};

// Imposta la proprietà "AddBidiMarks" su "true" per aggiungere segni prima dell'esecuzione
// con testo da destra a sinistra per indicare il fatto.
// Imposta la proprietà "AddBidiMarks" su "false" per scrivere tutto da sinistra a destra
// e da destra a sinistra funzionano allo stesso modo senza che nulla indichi quale sia quale.
saveOptions.AddBidiMarks = addBidiMarks;

doc.Save(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt", saveOptions);

string docText = System.Text.Encoding.Unicode.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    Assert.AreEqual("\uFEFFHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    Assert.True(docText.Contains("\u200f"));
}
else
{
    Assert.AreEqual("\uFEFFHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    Assert.False(docText.Contains("\u200f"));
}
```

### Guarda anche

* class [TxtSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../txtsaveoptions/)
* assemblea [Aspose.Words](../../../)


