---
title: Fill.Patterned
second_title: Aspose.Words for .NET API Referansı
description: Fill yöntem. Belirtilen dolguyu bir kalıba ayarlar.
type: docs
weight: 170
url: /tr/net/aspose.words.drawing/fill/patterned/
---
## Patterned(PatternType) {#patterned}

Belirtilen dolguyu bir kalıba ayarlar.

```csharp
public void Patterned(PatternType patternType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |

### Örnekler

Bir şekil için desenin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Bir kalıba doldurmanın belirtilen birkaç yolu vardır.
// 1 - Şekil dolgusuna desen uygula:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Ön plan ve arka plan renkleriyle deseni şekil dolgusuna uygulayın:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Ayrıca bakınız

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../fill/)
* toplantı [Aspose.Words](../../../)

---

## Patterned(PatternType, Color, Color) {#patterned_1}

Belirtilen dolguyu bir kalıba ayarlar.

```csharp
public void Patterned(PatternType patternType, Color foreColor, Color backColor)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |
| foreColor | Color | Ön plan dolgusunun rengi. |
| backColor | Color | Arka plan dolgusunun rengi. |

### Örnekler

Bir şekil için desenin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// Bir kalıba doldurmanın belirtilen birkaç yolu vardır.
// 1 - Şekil dolgusuna desen uygula:
fill.Patterned(PatternType.DiagonalBrick);

// 2 - Ön plan ve arka plan renkleriyle deseni şekil dolgusuna uygulayın:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### Ayrıca bakınız

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../fill/)
* toplantı [Aspose.Words](../../../)


