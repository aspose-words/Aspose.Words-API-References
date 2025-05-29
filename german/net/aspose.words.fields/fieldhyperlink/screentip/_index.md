---
title: FieldHyperlink.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words für .NET
description: Entdecken Sie die QuickInfo-Eigenschaft „FieldHyperlink“, um Ihren Hyperlink-Text anzupassen und so die Benutzerfreundlichkeit und das Engagement zu verbessern. Optimieren Sie Ihre Links noch heute!
type: docs
weight: 50
url: /de/net/aspose.words.fields/fieldhyperlink/screentip/
---
## FieldHyperlink.ScreenTip property

Ruft den QuickInfo-Text für den Hyperlink ab oder legt ihn fest.

```csharp
public string ScreenTip { get; set; }
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
