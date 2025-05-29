---
title: ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle
linktitle: NoSpaceBetweenParagraphsOfSameStyle
articleTitle: NoSpaceBetweenParagraphsOfSameStyle
second_title: .NET için Aspose.Words
description: ParagraphFormat NoSpaceBetweenParagraphsOfSameStyle özelliğini keşfedin. Aynı stildeki paragraflar arasındaki boşluğu ortadan kaldırarak belge düzeninizi optimize edin.
type: docs
weight: 250
url: /tr/net/aspose.words/paragraphformat/nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle property

Ne zaman`doğru` ,[`SpaceBefore`](../spacebefore/) Ve[`SpaceAfter`](../spaceafter/) Aynı stildeki paragraflar arasında göz ardı edilecektir

```csharp
public bool NoSpaceBetweenParagraphsOfSameStyle { get; set; }
```

## Notlar

Bu ayar yalnızca bir paragraf stiline uygulandığında etkili olur. Doğrudan bir paragrafa uygulandığında, hiçbir etkisi olmaz.

## Örnekler

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
