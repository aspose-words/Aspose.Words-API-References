---
title: ListLevel.GetEffectiveValue
second_title: Aspose.Words for .NET API Reference
description: ListLevel method. Reports the string representation of the ListLevel object for the specified index of the list item. Parameters specify the NumberStyle and an optional format string used when Custom is specified in C#.
type: docs
weight: 190
url: /net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

Reports the string representation of the [`ListLevel`](../) object for the specified index of the list item. Parameters specify the [`NumberStyle`](../../../aspose.words/numberstyle/) and an optional format string used when Custom is specified.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | Int32 | The index of the list item (must be in the range from 1 to 32767). |
| numberStyle | NumberStyle | The [`NumberStyle`](../../../aspose.words/numberstyle/) of the [`ListLevel`](../) object. |
| customNumberStyleFormat | String | The optional format string used when Custom is specified (e.g. "a, ç, ĝ, ..."). In other cases, this parameter must be `null` or empty. |

### Return Value

The string representation of the [`ListLevel`](../) object, described by the *numberStyle* parameter and the *customNumberStyleFormat* parameter, in the list item at the position determined by the *index* parameter.

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentException | *customNumberStyleFormat* is `null` or empty when the *numberStyle* is custom.-or- *customNumberStyleFormat* is not `null` or empty when the *numberStyle* is non-custom.-or- *customNumberStyleFormat* is invalid. |
| ArgumentOutOfRangeException | index is out of range. |

## Examples

Shows how to get the format for a list with the custom number style.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// We can get value for the specified index of the list item.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### See Also

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* namespace [Aspose.Words.Lists](../../listlevel/)
* assembly [Aspose.Words](../../../)
