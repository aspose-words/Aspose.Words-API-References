---
title: FileFormatInfo.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: Aspose.Words für .NET
description: Ermitteln Sie mit der Eigenschaft „FileFormatInfo HasMacros“, ob Ihr Dokument VBA-Makros enthält. Sorgen Sie noch heute für Dokumentensicherheit und -funktionalität!
type: docs
weight: 30
url: /de/net/aspose.words/fileformatinfo/hasmacros/
---
## FileFormatInfo.HasMacros property

Rückgaben`WAHR` wenn dieses Dokument VBA-Makros enthält.

```csharp
public bool HasMacros { get; }
```

## Beispiele

Zeigt, wie das Vorhandensein von VBA-Makros überprüft wird, ohne ein Dokument zu laden.

```csharp
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Macro.docm");
Assert.IsTrue(fileFormatInfo.HasMacros);
```

### Siehe auch

* class [FileFormatInfo](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
