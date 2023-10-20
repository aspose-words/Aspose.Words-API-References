---
title: Paragraph.GetEffectiveTabStops
linktitle: GetEffectiveTabStops
articleTitle: GetEffectiveTabStops
second_title: Aspose.Words for .NET
description: Paragraph GetEffectiveTabStops yöntem. Stiller veya listeler tarafından dolaylı olarak uygulananlar da dahil olmak üzere bu paragrafa uygulanan tüm sekme duraklarının dizisini döndürür C#'da.
type: docs
weight: 250
url: /tr/net/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph.GetEffectiveTabStops method

Stiller veya listeler tarafından dolaylı olarak uygulananlar da dahil olmak üzere, bu paragrafa uygulanan tüm sekme duraklarının dizisini döndürür.

```csharp
public TabStop[] GetEffectiveTabStops()
```

## Örnekler

Bir paragraf için özel sekme duraklarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Bu koleksiyonda sekme durağı olmayan bir paragraftaysak,
// Microsoft Word'de Sekme tuşuna her bastığımızda imleç 36 nokta atlayacaktır.
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

// Cetveli "Görünüm" sekmesi üzerinden etkinleştirirsek Microsoft Word'de özel sekme durakları ekleyebiliriz.
// Bu cetveldeki her birim iki varsayılan sekme durağıdır, yani 72 noktadır.
// Programlı olarak bu şekilde özel sekme durakları ekleyebiliriz.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// Bu sekme duraklarını Microsoft Word'de "Görünüm" -> aracılığıyla cetveli etkinleştirerek görebiliriz. "Göster" -> "Cetvel".
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// Eklediğimiz herhangi bir sekme karakteri cetveldeki sekme duraklarını kullanacak ve şunları yapabilecektir:
// sekme liderinin değerine bağlı olarak sekme kalkış ve varış yerleri arasında bir çizgi bırakın.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### Ayrıca bakınız

* class [TabStop](../../tabstop/)
* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
