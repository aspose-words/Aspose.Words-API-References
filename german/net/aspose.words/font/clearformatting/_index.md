---
title: Font.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words für .NET
description: Mit der Font ClearFormatting-Methode können Sie Ihren Text wieder in seinen ursprünglichen Stil zurückversetzen. Freuen Sie sich über eine saubere, einheitliche Formatierung für ein elegantes Erscheinungsbild!
type: docs
weight: 560
url: /de/net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

Setzt die Schriftformatierung auf die Standardeinstellung zurück.

```csharp
public void ClearFormatting()
```

## Bemerkungen

Entfernt alle explizit für das Objekt angegebenen Schriftformatierungen aus which [`Font`](../) wurde abgerufen, sodass die Schriftformatierung vom entsprechenden übergeordneten Element übernommen wird.

## Beispiele

Zeigt, wie ein Hyperlink-Feld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Fügen Sie einen Hyperlink ein und heben Sie ihn mit benutzerdefinierter Formatierung hervor.
// Der Hyperlink ist ein anklickbarer Text, der uns zum in der URL angegebenen Ort führt.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Strg + Linksklick auf den Link im Text in Microsoft Word führt uns über ein neues Webbrowserfenster zur URL.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
