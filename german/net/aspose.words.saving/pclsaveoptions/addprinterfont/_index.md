---
title: PclSaveOptions.AddPrinterFont
linktitle: AddPrinterFont
articleTitle: AddPrinterFont
second_title: Aspose.Words für .NET
description: Entdecken Sie die AddPrinterFont-Methode von PclSaveOptions zum effizienten Hochladen und Verwalten von Druckerschriftarten von Herstellern für eine verbesserte Druckleistung.
type: docs
weight: 50
url: /de/net/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions.AddPrinterFont method

Fügt Informationen zur Schriftart hinzu, die vom Hersteller auf den Drucker hochgeladen werden.

```csharp
public void AddPrinterFont(string fontFullName, string fontPclName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fontFullName | String | Vollständiger Name der Schriftart (z. B. „Times New Roman Bold Italic“). |
| fontPclName | String | Name der Schriftart, die im PCL-Dokument verwendet wird. |

## Bemerkungen

Es gibt 52 Schriftarten, die gemäß PCL-Spezifikation in jeden Drucker integriert werden müssen. Hersteller können ihren Geräten jedoch einige andere Schriftarten hinzufügen.

## Beispiele

Zeigt, wie Sie einen Drucker dazu bringen, alle Vorkommen einer bestimmten Schriftart durch eine andere Schriftart zu ersetzen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// Beim Drucken dieses Dokuments verwendet der Drucker die Schriftart „Courier New“
// um auf Stellen zuzugreifen, an denen in unserem Dokument die Schriftart „Courier“ verwendet wurde.
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### Siehe auch

* class [PclSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
