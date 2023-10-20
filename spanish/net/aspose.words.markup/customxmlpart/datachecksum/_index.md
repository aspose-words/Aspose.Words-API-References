---
title: CustomXmlPart.DataChecksum
linktitle: DataChecksum
articleTitle: DataChecksum
second_title: Aspose.Words para .NET
description: CustomXmlPart DataChecksum propiedad. Especifica una suma de comprobación de verificación de redundancia cíclica CRC delData contenido en C#.
type: docs
weight: 30
url: /es/net/aspose.words.markup/customxmlpart/datachecksum/
---
## CustomXmlPart.DataChecksum property

Especifica una suma de comprobación de verificación de redundancia cíclica (CRC) del[`Data`](../data/) contenido.

```csharp
public long DataChecksum { get; }
```

## Ejemplos

Muestra cómo se calcula la suma de comprobación en tiempo de ejecución.

```csharp
Document doc = new Document();

StructuredDocumentTag richText = new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(richText);

// La suma de comprobación es de solo lectura y se calcula utilizando los datos de la parte de datos XML personalizada correspondiente.
richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>ContentControl</text></root>"), "/root/text", "");

long checksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(checksum);

richText.XmlMapping.SetMapping(doc.CustomXmlParts.Add(Guid.NewGuid().ToString(),
    "<root><text>Updated ContentControl</text></root>"), "/root/text", "");

long updatedChecksum = richText.XmlMapping.CustomXmlPart.DataChecksum;
Console.WriteLine(updatedChecksum);

// Cambiamos la XmlPart de la etiqueta y la suma de comprobación se actualizó en tiempo de ejecución.
Assert.AreNotEqual(checksum, updatedChecksum);
```

### Ver también

* class [CustomXmlPart](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
