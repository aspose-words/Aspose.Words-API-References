---
title: CustomXmlPart.DataChecksum
linktitle: DataChecksum
articleTitle: DataChecksum
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CustomXmlPart DataChecksum, обеспечивающее целостность данных с надежной контрольной суммой CRC для вашего XML-контента. Повысьте надежность ваших данных!
type: docs
weight: 30
url: /ru/net/aspose.words.markup/customxmlpart/datachecksum/
---
## CustomXmlPart.DataChecksum property

Указывает контрольную сумму циклического избыточного кода (CRC)[`Data`](../data/) содержание.

```csharp
public long DataChecksum { get; }
```

## Примеры

Показывает, как рассчитывается контрольная сумма во время выполнения.

```csharp
Document doc = new Document();

StructuredDocumentTag richText = new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(richText);

// Контрольная сумма доступна только для чтения и вычисляется с использованием данных соответствующей пользовательской части данных XML.
richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>ContentControl</text></root>"), "/root/text", "");

long checksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(checksum);

richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>Updated ContentControl</text></root>"), "/root/text", "");

long updatedChecksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(updatedChecksum);

// Мы изменили XmlPart тега, и контрольная сумма была обновлена во время выполнения.
Assert.AreNotEqual(checksum, updatedChecksum);
```

### Смотрите также

* class [CustomXmlPart](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
