---
title: Paragraph.GetEffectiveTabStops
linktitle: GetEffectiveTabStops
articleTitle: GetEffectiveTabStops
second_title: .NET için Aspose.Words
description: Gelişmiş biçimlendirme için stiller ve listeler dahil olmak üzere bir paragraftaki tüm sekme duraklarını almak üzere GetEffectiveTabStops yöntemini keşfedin.
type: docs
weight: 270
url: /tr/net/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph.GetEffectiveTabStops method

Bu paragrafa uygulanan tüm sekme duraklarının dizisini döndürür; buna stiller veya listeler tarafından dolaylı olarak uygulananlar da dahildir.

```csharp
public TabStop[] GetEffectiveTabStops()
```

## Örnekler

Bir paragraf için özel sekme duraklarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Bu koleksiyonda sekme durağı olmayan bir paragraftaysak,
// Microsoft Word'de Tab tuşuna her bastığımızda imleç 36 puan atlayacaktır.
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

// Microsoft Word'de "Görünüm" sekmesinden cetveli etkinleştirirsek özel sekme durakları ekleyebiliriz.
// Bu cetveldeki her birim, 72 puan olan iki varsayılan sekme durağıdır.
// Özel sekme duraklarını programsal olarak şu şekilde ekleyebiliriz.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// Bu sekme duraklarını Microsoft Word'de "Görünüm" -> "Göster" -> "Cetvel" yoluyla cetveli etkinleştirerek görebiliriz.
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// Eklediğimiz herhangi bir sekme karakteri cetveldeki sekme duraklarını kullanacak ve,
// sekme liderinin değerine bağlı olarak sekme kalkış ve varış noktaları arasında bir çizgi bırakın.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### Ayrıca bakınız

* class [TabStop](../../tabstop/)
* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
