---
title: Underline
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt die Art der Unterstreichung an die auf eine Schriftart angewendet wird.
type: docs
weight: 6210
url: /de/net/aspose.words/underline/
---
## Underline enumeration

Gibt die Art der Unterstreichung an, die auf eine Schriftart angewendet wird.

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

### Beispiele

Zeigt, wie ein Hyperlink-Feld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Hyperlink einfügen und mit benutzerdefinierter Formatierung hervorheben.
// Der Hyperlink ist ein anklickbares Textstück, das uns zu der in der URL angegebenen Stelle führt.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", falsch);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Strg + Linksklick auf den Link im Text in Microsoft Word bringt uns über ein neues Webbrowser-Fenster zur URL.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
