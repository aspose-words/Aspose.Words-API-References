---
title: FieldHyperlink.OpenInNewWindow
linktitle: OpenInNewWindow
articleTitle: OpenInNewWindow
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldHyperlink OpenInNewWindow och kontrollera enkelt om länkar öppnas i ett nytt webbläsarfönster för en förbättrad användarupplevelse.
type: docs
weight: 40
url: /sv/net/aspose.words.fields/fieldhyperlink/openinnewwindow/
---
## FieldHyperlink.OpenInNewWindow property

Hämtar eller anger om destinationswebbplatsen ska öppnas i ett nytt webbläsarfönster.

```csharp
public bool OpenInNewWindow { get; set; }
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
