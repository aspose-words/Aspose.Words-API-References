---
title: TxtLoadOptions.AutoNumberingDetection
linktitle: AutoNumberingDetection
articleTitle: AutoNumberingDetection
second_title: Aspose.Words für .NET
description: TxtLoadOptions AutoNumberingDetection eigendom. Ruft einen booleschen Wert ab oder legt diesen fest der angibt ob beim Laden eines Dokuments eine automatische Nummerierungserkennung durchgeführt wird. Der Standardwert istWAHR  in C#.
type: docs
weight: 20
url: /de/net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, ob beim Laden eines Dokuments eine automatische Nummerierungserkennung durchgeführt wird. Der Standardwert ist`WAHR` .

```csharp
public bool AutoNumberingDetection { get; set; }
```

## Beispiele

Zeigt, wie die automatische Nummerierungserkennung deaktiviert wird.

```csharp
TxtLoadOptions options = new TxtLoadOptions { AutoNumberingDetection = false };
Document doc = new Document(MyDir + "Number detection.txt", options);
```

### Siehe auch

* class [TxtLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
