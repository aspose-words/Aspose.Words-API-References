---
title: ParagraphFormat.SpaceBefore
linktitle: SpaceBefore
articleTitle: SpaceBefore
second_title: .NET için Aspose.Words
description: Belgenizin okunabilirliğini ve stilini geliştirmek için paragraf aralıklarını noktalar halinde kolayca ayarlamak üzere ParagraphFormat SpaceBefore özelliğini keşfedin.
type: docs
weight: 330
url: /tr/net/aspose.words/paragraphformat/spacebefore/
---
## ParagraphFormat.SpaceBefore property

Paragraftan önceki boşluk miktarını (nokta cinsinden) alır veya ayarlar.

```csharp
public double SpaceBefore { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentOutOfRangeException | Argüman geçerli değerler aralığının dışında olduğunda fırlatılır. |

## Notlar

Hiçbir etkisi yoktur[`SpaceBeforeAuto`](../spacebeforeauto/) dır`doğru`.

Geçerli değerler 0 ile 1584 (dahil) arasındadır.

## Örnekler

Otomatik paragraf aralığının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bu oluşturucunun oluşturacağı paragraflardan önce ve sonra büyük miktarda boşluk uygulayın.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Otomatik aralık uygulamak için bu bayrakları "true" olarak ayarlayın.
// yukarıda ayarladığımız özelliklerde boşlukları etkili bir şekilde görmezden geliyoruz.
// Bunları "false" olarak bırakmak özel paragraf aralığımızı uygulayacaktır.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Üst ve altlarında boşluk olacak şekilde iki paragraf ekleyin ve belgeyi kaydedin.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

Aynı stildeki paragraflar arasında boşluk bırakmamanın nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bu oluşturucunun oluşturacağı paragraflardan önce ve sonra büyük miktarda boşluk uygulayın.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Uygulamak için "NoSpaceBetweenParagraphsOfSameStyle" bayrağını "true" olarak ayarlayın
// aynı stildeki paragraflar arasında boşluk bırakılmayacak, böylece benzer paragraflar gruplanacak.
// "NoSpaceBetweenParagraphsOfSameStyle" bayrağını "false" olarak bırakın
// her paragrafa eşit aralık uygulamak için.
builder.ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle = noSpaceBetweenParagraphsOfSameStyle;

builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
