---
title: FontInfoCollection.Contains
second_title: Aspose.Words für .NET-API-Referenz
description: FontInfoCollection methode. Ermittelt ob die Sammlung eine Schriftart mit dem angegebenen Namen enthält.
type: docs
weight: 60
url: /de/net/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection.Contains method

Ermittelt, ob die Sammlung eine Schriftart mit dem angegebenen Namen enthält.

```csharp
public bool Contains(string name)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Der Name der Schriftart, nach der gesucht werden soll, unterscheidet nicht zwischen Groß- und Kleinschreibung. |

### Rückgabewert

`WAHR` wenn der Artikel in der Sammlung gefunden wird; ansonsten,`FALSCH`.

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


