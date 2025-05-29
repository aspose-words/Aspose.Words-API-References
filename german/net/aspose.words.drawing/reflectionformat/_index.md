---
title: ReflectionFormat Class
linktitle: ReflectionFormat
articleTitle: ReflectionFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.ReflectionFormat für erweiterte Objektreflexionsformatierung. Verbessern Sie Ihr Dokumentdesign durch nahtlose Integration!
type: docs
weight: 1570
url: /de/net/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class

Stellt die Reflexionsformatierung für ein Objekt dar.

```csharp
public class ReflectionFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Blur](../../aspose.words.drawing/reflectionformat/blur/) { get; set; } | Ruft einen Double-Wert ab oder legt ihn fest, der den Grad des auf den Reflexionseffekt angewendeten Unschärfeeffekts in Punkten angibt. Der Standardwert ist 0,0. |
| [Distance](../../aspose.words.drawing/reflectionformat/distance/) { get; set; } | Ruft einen Double-Wert ab oder legt ihn fest, der den Abstand des reflektierten Bilds vom Objekt in Punkten angibt. Der Standardwert ist 0,0. |
| [Size](../../aspose.words.drawing/reflectionformat/size/) { get; set; } | Ruft einen Double-Wert zwischen 0,0 und 1,0 ab oder legt ihn fest, der die Größe der Reflexion als Prozentsatz des reflektierten Objekts darstellt. Der Standardwert ist 0,0. |
| [Transparency](../../aspose.words.drawing/reflectionformat/transparency/) { get; set; } | Ruft einen Double-Wert zwischen 0,0 (undurchsichtig) und 1,0 (durchsichtig) ab oder legt ihn fest, der den Grad der Transparenz für den Reflexionseffekt darstellt. Der Standardwert ist 0,0. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Remove](../../aspose.words.drawing/reflectionformat/remove/)() | Entfernt`ReflectionFormat` vom übergeordneten Objekt. |

## Bemerkungen

Verwenden Sie die[`Reflection`](../shapebase/reflection/) Eigenschaft, um auf Reflexionseigenschaften eines Objekts zuzugreifen. Sie erstellen keine Instanzen der`ReflectionFormat` Klasse direkt.

## Beispiele

Zeigt, wie mit dem Reflexionsformeffekt interagiert wird.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Reflection.Transparency = 0.37;
shape.Reflection.Size = 0.48;
shape.Reflection.Blur = 17.5;
shape.Reflection.Distance = 9.2;

doc.Save(ArtifactsDir + "Shape.Reflection.docx");

doc = new Document(ArtifactsDir + "Shape.Reflection.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

ReflectionFormat reflectionFormat = shape.Reflection;

Assert.AreEqual(0.37d, reflectionFormat.Transparency, 0.01d);
Assert.AreEqual(0.48d, reflectionFormat.Size, 0.01d);
Assert.AreEqual(17.5d, reflectionFormat.Blur, 0.01d);
Assert.AreEqual(9.2d, reflectionFormat.Distance, 0.01d);

reflectionFormat.Remove();

Assert.AreEqual(0, reflectionFormat.Transparency);
Assert.AreEqual(0, reflectionFormat.Size);
Assert.AreEqual(0, reflectionFormat.Blur);
Assert.AreEqual(0, reflectionFormat.Distance);
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
