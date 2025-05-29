---
title: FieldHyperlink.Address
linktitle: Address
articleTitle: Address
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldHyperlink Address. Gestisci facilmente le destinazioni dei collegamenti ipertestuali per una navigazione fluida nelle tue applicazioni. Migliora l'esperienza utente oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldhyperlink/address/
---
## FieldHyperlink.Address property

Ottiene o imposta una posizione in cui salta questo collegamento ipertestuale.

```csharp
public string Address { get; set; }
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
