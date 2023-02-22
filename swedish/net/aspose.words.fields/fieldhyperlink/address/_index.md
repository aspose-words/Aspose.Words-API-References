---
title: FieldHyperlink.Address
second_title: Aspose.Words för .NET API Referens
description: FieldHyperlink fast egendom. Hämtar eller ställer in en plats där denna hyperlänk hoppar.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldhyperlink/address/
---
## FieldHyperlink.Address property

Hämtar eller ställer in en plats där denna hyperlänk hoppar.

```csharp
public string Address { get; set; }
```

### Exempel

Visar hur man använder HYPERLINK-fält för att länka till dokument i det lokala filsystemet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// När vi klickar på det här HYPERLÄNK-fältet i Microsoft Word,
// det öppnar det länkade dokumentet och placerar sedan markören vid det angivna bokmärket.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// När vi klickar på det här HYPERLÄNK-fältet i Microsoft Word,
// det kommer att öppna det länkade dokumentet och automatiskt rulla ner till den angivna iframen.
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### Se även

* class [FieldHyperlink](../)
* namnutrymme [Aspose.Words.Fields](../../fieldhyperlink/)
* hopsättning [Aspose.Words](../../../)


