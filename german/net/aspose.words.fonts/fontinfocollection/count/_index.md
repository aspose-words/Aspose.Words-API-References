---
title: FontInfoCollection.Count
second_title: Aspose.Words für .NET-API-Referenz
description: FontInfoCollection eigendom. Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab.
type: docs
weight: 10
url: /de/net/aspose.words.fonts/fontinfocollection/count/
---
## FontInfoCollection.Count property

Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab.

```csharp
public int Count { get; }
```

### Beispiele

Zeigt Informationen zu den Schriftarten an, die im leeren Dokument vorhanden sind.

```csharp
Document doc = new Document();

// Ein leeres Dokument enthält 3 Standardschriftarten. Jede Schriftart im Dokument
// verfügt über ein entsprechendes FontInfo-Objekt, das Details zu dieser Schriftart enthält.
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### Siehe auch

* class [FontInfoCollection](../)
* namensraum [Aspose.Words.Fonts](../../fontinfocollection/)
* Montage [Aspose.Words](../../../)


