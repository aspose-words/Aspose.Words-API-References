---
title: Paragraph.GetEffectiveTabStops
second_title: Aspose.Words for .NET API Referansı
description: Paragraph yöntem. Stiller veya listeler tarafından dolaylı olarak uygulananlar da dahil olmak üzere bu paragrafa uygulanan tüm sekme duraklarının dizisini döndürür.
type: docs
weight: 250
url: /tr/net/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph.GetEffectiveTabStops method

Stiller veya listeler tarafından dolaylı olarak uygulananlar da dahil olmak üzere, bu paragrafa uygulanan tüm sekme duraklarının dizisini döndürür.

```csharp
public TabStop[] GetEffectiveTabStops()
```

### Örnekler

Bir paragraf için özel sekme duraklarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Bu koleksiyonda sekme durakları olmayan bir paragraftaysak,
// Microsoft Word'de Sekme tuşuna her bastığımızda imleç 36 puan atlayacaktır.
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

// Cetveli "Görünüm" sekmesinden etkinleştirirsek, Microsoft Word'de özel sekme durakları ekleyebiliriz.
// Bu cetveldeki her birim, 72 nokta olan iki varsayılan sekme durağıdır.
// Programlı olarak bu şekilde özel sekme durakları ekleyebiliriz.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// Microsoft Word'de cetveli "Görünüm" -> ile etkinleştirerek bu sekme duraklarını görebiliriz. "Göster" -> "Cetvel".
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// Eklediğimiz herhangi bir sekme karakteri, cetvel üzerindeki sekme duraklarından faydalanacak ve şunları yapabilir:
// sekme liderinin değerine bağlı olarak, sekme çıkış ve varış yerleri arasında bir çizgi bırakın.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### Ayrıca bakınız

* class [TabStop](../../tabstop/)
* class [Paragraph](../)
* ad alanı [Aspose.Words](../../paragraph/)
* toplantı [Aspose.Words](../../../)


