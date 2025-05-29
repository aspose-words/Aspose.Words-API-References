---
title: FileFormatUtil.SaveFormatToLoadFormat
linktitle: SaveFormatToLoadFormat
articleTitle: SaveFormatToLoadFormat
second_title: Aspose.Words für .NET
description: Konvertieren Sie SaveFormat mühelos in LoadFormat mit der FileFormatUtil-Methode. Vereinfachen Sie die Dateiverwaltung und verbessern Sie die Kompatibilität!
type: docs
weight: 90
url: /de/net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

Konvertiert eine[`SaveFormat`](../../saveformat/) Wert zu einem[`LoadFormat`](../../loadformat/) Wert wenn möglich.

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentException | Wirft, wenn keine Konvertierung möglich ist. |

## Beispiele

Zeigt, wie ein Speicherformat in das entsprechende Ladeformat konvertiert wird.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// Bei einigen Dateitypen können Dokumente mit Aspose.Words gespeichert, aber nicht geladen werden.
// Wenn wir versuchen, ein Speicherformat dieses Typs in ein Ladeformat zu konvertieren, wird eine Ausnahme ausgelöst.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### Siehe auch

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
