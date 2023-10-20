---
title: ListLevel.GetEffectiveValue
linktitle: GetEffectiveValue
articleTitle: GetEffectiveValue
second_title: Aspose.Words für .NET
description: ListLevel GetEffectiveValue methode. Meldet die Zeichenfolgendarstellung vonListLevelObjekt für den angegebenen index des Listenelements. Parameter geben die anNumberStyle und ein optionales Format string  das verwendet wird wennCustom angegeben ist in C#.
type: docs
weight: 190
url: /de/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

Meldet die Zeichenfolgendarstellung von[`ListLevel`](../)Objekt für den angegebenen index des Listenelements. Parameter geben die an[`NumberStyle`](../../../aspose.words/numberstyle/) und ein optionales Format string , das verwendet wird, wennCustom angegeben ist.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Der Index des Listenelements (muss im Bereich von 1 bis 32767 liegen). |
| numberStyle | NumberStyle | Die[`NumberStyle`](../../../aspose.words/numberstyle/) des[`ListLevel`](../) Objekt. |
| customNumberStyleFormat | String | Die optionale Formatzeichenfolge, die verwendet wird, wennCustom angegeben ist (z. B. „a, ç, ĝ, ...“). In anderen Fällen muss dieser Parameter angegeben werden`Null` oder leer. |

### Rückgabewert

Die String-Darstellung von[`ListLevel`](../) Objekt, beschrieben durch die*numberStyle* Parameter and the*customNumberStyleFormat* Parameter, im Listenelement an der durch den definierten Position*index* Parameter.

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentException | *customNumberStyleFormat* Ist`Null` oder leer, wenn die*numberStyle* ist benutzerdefiniert.-oder- *customNumberStyleFormat* ist nicht`Null` oder leer, wenn die*numberStyle* ist nicht benutzerdefiniert.-oder- *customNumberStyleFormat* ist ungültig. |
| ArgumentOutOfRangeException | Der Index liegt außerhalb des zulässigen Bereichs. |

## Beispiele

Zeigt, wie man das Format für eine Liste mit dem benutzerdefinierten Zahlenstil erhält.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Wir können einen Wert für den angegebenen Index des Listenelements abrufen.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Siehe auch

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
