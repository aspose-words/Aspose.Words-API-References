---
title: FieldHyperlink.Target
linktitle: Target
articleTitle: Target
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldHyperlink Target och konfigurera enkelt länkomdirigering för förbättrad användarnavigering och sömlösa webbupplevelser.
type: docs
weight: 70
url: /sv/net/aspose.words.fields/fieldhyperlink/target/
---
## FieldHyperlink.Target property

Hämtar eller anger målet som länken ska omdirigeras till.

```csharp
public string Target { get; set; }
```

## Exempel

Visar hur man använder HYPERLÄNK-fält för att länka till dokument i det lokala filsystemet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// När vi klickar på det här HYPERLÄNK-fältet i Microsoft Word,
// den öppnar det länkade dokumentet och placerar sedan markören vid det angivna bokmärket.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// När vi klickar på det här HYPERLÄNK-fältet i Microsoft Word,
// det öppnar det länkade dokumentet och scrollar automatiskt ner till den angivna iframen.
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
