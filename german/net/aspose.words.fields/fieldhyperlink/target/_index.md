---
title: FieldHyperlink.Target
second_title: Aspose.Words für .NET-API-Referenz
description: FieldHyperlink eigendom. Holt oder setzt das Ziel zu dem der Link umgeleitet werden soll.
type: docs
weight: 70
url: /de/net/aspose.words.fields/fieldhyperlink/target/
---
## FieldHyperlink.Target property

Holt oder setzt das Ziel, zu dem der Link umgeleitet werden soll.

```csharp
public string Target { get; set; }
```

### Beispiele

Zeigt, wie HYPERLINK-Felder verwendet werden, um auf Dokumente im lokalen Dateisystem zu verlinken.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// Wenn wir in Microsoft Word auf dieses HYPERLINK-Feld klicken,
// Es öffnet das verknüpfte Dokument und setzt dann den Cursor auf das angegebene Lesezeichen.
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
* namensraum [Aspose.Words.Fields](../../fieldhyperlink/)
* Montage [Aspose.Words](../../../)


