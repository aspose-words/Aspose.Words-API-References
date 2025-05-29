---
title: ListLevel.GetEffectiveValue
linktitle: GetEffectiveValue
articleTitle: GetEffectiveValue
second_title: Aspose.Words för .NET
description: Upptäck ListLevel GetEffectiveValue-metoden för att enkelt hämta strängrepresentationer av listobjekt. Anpassa med NumberStyle och formatalternativ!
type: docs
weight: 190
url: /sv/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

Rapporterar strängrepresentationen av[`ListLevel`](../)objekt för det angivna index för listobjektet. Parametrar anger[`NumberStyle`](../../../aspose.words/numberstyle/) och ett valfritt format string som används närCustom är specificerad.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | Int32 | Indexet för listobjektet (måste vara i intervallet 1 till 32767). |
| numberStyle | NumberStyle | Den[`NumberStyle`](../../../aspose.words/numberstyle/) av[`ListLevel`](../) objekt. |
| customNumberStyleFormat | String | Den valfria formatsträngen som används närCustom är specificerad (t.ex. "a, ç, ĝ, ..."). I andra fall måste denna parameter vara`null` eller tom. |

### Returvärde

Strängrepresentationen av[`ListLevel`](../) objekt, beskrivet av*numberStyle* parametern och *customNumberStyleFormat* parametern, i listobjektet på den position som bestäms av*index* parameter.

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentException | *customNumberStyleFormat* är`null` eller tom när*numberStyle* är anpassad.-eller- *customNumberStyleFormat* är inte`null` eller tom när*numberStyle* är icke-anpassad.-eller- *customNumberStyleFormat* är ogiltig. |
| ArgumentOutOfRangeException | indexet är utanför intervallet. |

## Exempel

Visar hur man hämtar formatet för en lista med det anpassade numeriska formatet.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Vi kan få ett värde för det angivna indexet för listobjektet.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Se även

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)
