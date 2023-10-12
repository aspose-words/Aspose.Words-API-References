---
title: FileFormatUtil.SaveFormatToLoadFormat
second_title: Aspose.Words für .NET-API-Referenz
description: FileFormatUtil methode. Konvertiert aSaveFormat Wert zu aLoadFormat Wert wenn möglich.
type: docs
weight: 90
url: /de/net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

Konvertiert a[`SaveFormat`](../../saveformat/) Wert zu a[`LoadFormat`](../../loadformat/) Wert wenn möglich.

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentException | Wirft, wenn keine Konvertierung möglich ist. |

### Beispiele

Zeigt, wie ein Speicherformat in das entsprechende Ladeformat konvertiert wird.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// Bei einigen Dateitypen können Dokumente gespeichert, aber nicht mit Aspose.Words geladen werden.
// Wenn wir versuchen, ein Speicherformat dieses Typs in ein Ladeformat zu konvertieren, wird eine Ausnahme ausgelöst.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### Siehe auch

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* namensraum [Aspose.Words](../../fileformatutil/)
* Montage [Aspose.Words](../../../)


