---
title: PclSaveOptions.AddPrinterFont
second_title: Aspose.Words für .NET-API-Referenz
description: PclSaveOptions methode. Fügt Informationen über die Schriftart hinzu die vom Hersteller auf den Drucker hochgeladen wird.
type: docs
weight: 50
url: /de/net/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions.AddPrinterFont method

Fügt Informationen über die Schriftart hinzu, die vom Hersteller auf den Drucker hochgeladen wird.

```csharp
public void AddPrinterFont(string fontFullName, string fontPclName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontFullName | String | Vollständiger Name der Schriftart (z. B. „Times New Roman Bold Italic“). |
| fontPclName | String | Name der Schriftart, die im PCL-Dokument verwendet wird. |

### Bemerkungen

Es gibt 52 Schriftarten, die in jedem Drucker gemäß der PCL-Spezifikation erstellt werden müssen. Allerdings können Hersteller ihren Geräten einige andere Schriftarten hinzufügen.

### Beispiele

Zeigt, wie man einen Drucker dazu bringt, alle Instanzen einer bestimmten Schriftart durch eine andere Schriftart zu ersetzen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// Beim Drucken dieses Dokuments verwendet der Drucker die Schriftart „Courier New“.
// um auf Stellen zuzugreifen, an denen in unserem Dokument die Schriftart „Courier“ verwendet wurde.
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### Siehe auch

* class [PclSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../pclsaveoptions/)
* Montage [Aspose.Words](../../../)


