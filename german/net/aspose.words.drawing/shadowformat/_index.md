---
title: ShadowFormat Class
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.Drawing.ShadowFormat für verbesserte Objektschatteneffekte. Verbessern Sie Ihr Dokumentdesign mit anpassbaren Schattenformatierungsoptionen.
type: docs
weight: 1620
url: /de/net/aspose.words.drawing/shadowformat/
---
## ShadowFormat class

Stellt die Schattenformatierung für ein Objekt dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit grafischen Elementen](https://docs.aspose.com/words/net/working-with-graphic-elements/) Dokumentationsartikel.

```csharp
public class ShadowFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Color](../../aspose.words.drawing/shadowformat/color/) { get; } | Erhält eineColor Objekt, das die Farbe für den Schatten darstellt. Der Standardwert istBlack . |
| [Type](../../aspose.words.drawing/shadowformat/type/) { get; set; } | Ruft ab oder setzt die angegebene[`ShadowType`](../shadowtype/) für ShadowFormat. |
| [Visible](../../aspose.words.drawing/shadowformat/visible/) { get; } | Rückgaben`WAHR` wenn die auf diese Instanz angewendete Formatierung sichtbar ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clear](../../aspose.words.drawing/shadowformat/clear/)() | Löscht das Schattenformat. |

## Beispiele

Zeigt, wie man Schattenfarbe erhält.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
