---
title: Fill.Patterned
linktitle: Patterned
articleTitle: Patterned
second_title: Aspose.Words for .NET
description: Fill Patterned yöntem. Belirtilen dolguyu bir desene ayarlar C#'da.
type: docs
weight: 220
url: /tr/net/aspose.words.drawing/fill/patterned/
---
## Patterned(*[PatternType](../../patterntype/)*) {#patterned}

Belirtilen dolguyu bir desene ayarlar.

```csharp
public void Patterned(PatternType patternType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |

## Örnekler

Bir şekil için desenin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Bir deseni doldurmanın birkaç yolu vardır.
// 1 - Deseni şekil dolgusuna uygula:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Şekil dolgusuna ön plan ve arka plan renkleriyle desen uygulayın:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Ayrıca bakınız

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)

---

## Patterned(*[PatternType](../../patterntype/), Color, Color*) {#patterned_1}

Belirtilen dolguyu bir desene ayarlar.

```csharp
public void Patterned(PatternType patternType, Color foreColor, Color backColor)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |
| foreColor | Color | Ön plan dolgusunun rengi. |
| backColor | Color | Arka plan dolgusunun rengi. |

## Örnekler

Bir şekil için desenin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Bir deseni doldurmanın birkaç yolu vardır.
// 1 - Deseni şekil dolgusuna uygula:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Şekil dolgusuna ön plan ve arka plan renkleriyle desen uygulayın:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Ayrıca bakınız

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
