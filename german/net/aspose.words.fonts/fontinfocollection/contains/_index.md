---
title: FontInfoCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words für .NET
description: Finden Sie heraus, ob FontInfoCollection eine bestimmte Schriftart enthält. So können Sie Ihre Schriftsammlung ganz einfach verwalten und darauf zugreifen.
type: docs
weight: 60
url: /de/net/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection.Contains method

Bestimmt, ob die Sammlung eine Schriftart mit dem angegebenen Namen enthält.

```csharp
public bool Contains(string name)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Name der zu suchenden Schriftart ohne Berücksichtigung der Groß-/Kleinschreibung. |

### Rückgabewert

`WAHR`wenn der Artikel in der Sammlung gefunden wird; andernfalls`FALSCH`.

## Beispiele

Zeigt Informationen zu den Schriftarten an, die im leeren Dokument vorhanden sind.

```csharp
Document doc = new Document();

// Ein leeres Dokument enthält 3 Standardschriften. Jede Schrift im Dokument
// verfügt über ein entsprechendes FontInfo-Objekt, das Details zu dieser Schriftart enthält.
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### Siehe auch

* class [FontInfoCollection](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
