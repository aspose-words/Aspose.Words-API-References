---
title: FieldHyperlink.Target
linktitle: Target
articleTitle: Target
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldHyperlink Target e configura facilmente il reindirizzamento dei link per una navigazione utente migliorata ed esperienze web fluide.
type: docs
weight: 70
url: /it/net/aspose.words.fields/fieldhyperlink/target/
---
## FieldHyperlink.Target property

Ottiene o imposta la destinazione a cui il collegamento deve essere reindirizzato.

```csharp
public string Target { get; set; }
```

## Esempi

Mostra come utilizzare i campi HYPERLINK per creare collegamenti ai documenti nel file system locale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// Quando clicchiamo su questo campo COLLEGAMENTO IPERTESTUALE in Microsoft Word,
// aprirà il documento collegato e posizionerà il cursore sul segnalibro specificato.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// Quando clicchiamo su questo campo COLLEGAMENTO IPERTESTUALE in Microsoft Word,
// aprirà il documento collegato e scorrerà automaticamente fino all'iframe specificato.
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
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
