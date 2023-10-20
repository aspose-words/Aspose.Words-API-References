---
title: FieldHyperlink.SubAddress
linktitle: SubAddress
articleTitle: SubAddress
second_title: Aspose.Words für .NET
description: FieldHyperlink SubAddress eigendom. Ruft eine Position in der Datei ab oder legt diese fest beispielsweise ein Lesezeichen an die dieser Hyperlink springt in C#.
type: docs
weight: 60
url: /de/net/aspose.words.fields/fieldhyperlink/subaddress/
---
## FieldHyperlink.SubAddress property

Ruft eine Position in der Datei ab oder legt diese fest, beispielsweise ein Lesezeichen, an die dieser Hyperlink springt.

```csharp
public string SubAddress { get; set; }
```

## Beispiele

Zeigt, wie HYPERLINK-Felder zum Verknüpfen mit Dokumenten im lokalen Dateisystem verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// Wenn wir in Microsoft Word auf dieses HYPERLINK-Feld klicken,
// Es öffnet das verknüpfte Dokument und platziert den Cursor dann auf dem angegebenen Lesezeichen.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// Wenn wir in Microsoft Word auf dieses HYPERLINK-Feld klicken,
// Es öffnet das verknüpfte Dokument und scrollt automatisch nach unten zum angegebenen Iframe.
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### Siehe auch

* class [FieldHyperlink](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
