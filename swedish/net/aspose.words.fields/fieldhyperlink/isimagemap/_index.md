---
title: FieldHyperlink.IsImageMap
linktitle: IsImageMap
articleTitle: IsImageMap
second_title: Aspose.Words för .NET
description: FieldHyperlink IsImageMap fast egendom. Hämtar eller ställer in om koordinater ska läggas till hyperlänken för en bildkarta på serversidan i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldhyperlink/isimagemap/
---
## FieldHyperlink.IsImageMap property

Hämtar eller ställer in om koordinater ska läggas till hyperlänken för en bildkarta på serversidan.

```csharp
public bool IsImageMap { get; set; }
```

## Exempel

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
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
