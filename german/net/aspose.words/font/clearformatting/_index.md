---
title: Font.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words für .NET
description: Font ClearFormatting methode. Setzt die Standardschriftartformatierung zurück in C#.
type: docs
weight: 550
url: /de/net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

Setzt die Standardschriftartformatierung zurück.

```csharp
public void ClearFormatting()
```

## Bemerkungen

Entfernt alle explizit für das Objekt angegebenen Schriftartformatierungen aus which [`Font`](../) wurde erhalten, sodass die Schriftartformatierung vom entsprechenden übergeordneten Element geerbt wird.

## Beispiele

Zeigt, wie ein Hyperlinkfeld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Einen Hyperlink einfügen und ihn mit benutzerdefinierter Formatierung hervorheben.
// Der Hyperlink ist ein anklickbarer Text, der uns zu dem in der URL angegebenen Ort führt.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Strg + Linksklick auf den Link im Text in Microsoft Word führt uns über ein neues Webbrowser-Fenster zur URL.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
