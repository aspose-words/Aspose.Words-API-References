---
title: ListLevel.GetEffectiveValue
linktitle: GetEffectiveValue
articleTitle: GetEffectiveValue
second_title: Aspose.Words für .NET
description: Entdecken Sie die ListLevel GetEffectiveValue-Methode, um einfach String-Darstellungen von Listenelementen abzurufen. Passen Sie sie mit NumberStyle und Formatoptionen an!
type: docs
weight: 190
url: /de/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

Gibt die String-Darstellung des[`ListLevel`](../)Objekt für den angegebenen Index des Listenelements. Parameter geben die[`NumberStyle`](../../../aspose.words/numberstyle/) und ein optionaler Formatstring , der verwendet wird, wennCustom ist angegeben.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Der Index des Listenelements (muss im Bereich von 1 bis 32767 liegen). |
| numberStyle | NumberStyle | Die[`NumberStyle`](../../../aspose.words/numberstyle/) der[`ListLevel`](../) Objekt. |
| customNumberStyleFormat | String | Die optionale Formatzeichenfolge, die verwendet wird, wennCustom angegeben ist (zB "a, ç, ĝ, ..."). In anderen Fällen muss dieser Parameter`null` oder leer. |

### Rückgabewert

Die String-Darstellung des[`ListLevel`](../) Objekt, beschrieben durch die*numberStyle* Parameter und der*customNumberStyleFormat* Parameter, im Listenelement an der Position, die durch den*index* parameter.

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentException | *customNumberStyleFormat* Ist`null` oder leer, wenn die*numberStyle* ist benutzerdefiniert.-oder- *customNumberStyleFormat* ist nicht`null` oder leer, wenn die*numberStyle* ist nicht benutzerdefiniert.-oder- *customNumberStyleFormat* ist ungültig. |
| ArgumentOutOfRangeException | Index liegt außerhalb des Bereichs. |

## Beispiele

Zeigt, wie Sie das Format für eine Liste mit dem benutzerdefinierten Zahlenstil erhalten.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Wir können den Wert für den angegebenen Index des Listenelements abrufen.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Siehe auch

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
