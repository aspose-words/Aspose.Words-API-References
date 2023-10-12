---
title: FieldHyperlink.ScreenTip
second_title: Aspose.Words per .NET API Reference
description: FieldHyperlink proprietà. Ottiene o imposta il testo della descrizione comando per il collegamento ipertestuale.
type: docs
weight: 50
url: /it/net/aspose.words.fields/fieldhyperlink/screentip/
---
## FieldHyperlink.ScreenTip property

Ottiene o imposta il testo della descrizione comando per il collegamento ipertestuale.

```csharp
public string ScreenTip { get; set; }
```

### Esempi

Mostra come utilizzare i campi HYPERLINK per collegarsi ai documenti nel file system locale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// Quando facciamo clic su questo campo HYPERLINK in Microsoft Word,
// aprirà il documento collegato e posizionerà il cursore sul segnalibro specificato.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// Quando facciamo clic su questo campo HYPERLINK in Microsoft Word,
// aprirà il documento collegato e scorrerà automaticamente verso il basso fino all'iframe specificato.
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### Guarda anche

* class [FieldHyperlink](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldhyperlink/)
* assemblea [Aspose.Words](../../../)


