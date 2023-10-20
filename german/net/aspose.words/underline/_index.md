---
title: Underline Enum
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words für .NET
description: Aspose.Words.Underline opsomming. Gibt den Typ der Unterstreichung an die auf eine Schriftart angewendet wird in C#.
type: docs
weight: 6510
url: /de/net/aspose.words/underline/
---
## Underline enumeration

Gibt den Typ der Unterstreichung an, die auf eine Schriftart angewendet wird.

```csharp
public enum Underline
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` |  |
| Single | `1` |  |
| Words | `2` |  |
| Double | `3` |  |
| Dotted | `4` |  |
| Thick | `6` |  |
| Dash | `7` |  |
| DashLong | `39` |  |
| DotDash | `9` |  |
| DotDotDash | `10` |  |
| Wavy | `11` |  |
| DottedHeavy | `20` |  |
| DashHeavy | `23` |  |
| DashLongHeavy | `55` |  |
| DotDashHeavy | `25` |  |
| DotDotDashHeavy | `26` |  |
| WavyHeavy | `27` |  |
| WavyDouble | `43` |  |

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
