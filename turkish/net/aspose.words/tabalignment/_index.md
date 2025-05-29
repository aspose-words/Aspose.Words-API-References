---
title: TabAlignment Enum
linktitle: TabAlignment
articleTitle: TabAlignment
second_title: .NET için Aspose.Words
description: Özelleştirilebilir sekme durağı hizalaması için Aspose.Words.TabAlignment enum'unu keşfedin. Belge biçimlendirmesini bugün hassasiyet ve esneklikle geliştirin!
type: docs
weight: 7030
url: /tr/net/aspose.words/tabalignment/
---
## TabAlignment enumeration

Bir sekme durağının hizalamasını/türünü belirtir.

```csharp
public enum TabAlignment
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Left | `0` | Sekme durağının ardından metni sola hizalar. |
| Center | `1` | Metni sekme durağının etrafına ortalar. |
| Right | `2` | Metni sekme durağında sağa hizalar. |
| Decimal | `3` | Metni ondalık noktaya hizalar. |
| Bar | `4` | Sekme durağı konumunda dikey bir çubuk çizer. |
| List | `6` | Sekme, bir liste öğesindeki sayı/madde işareti ile metin arasındaki bir ayraçtır. |
| Clear | `7` | Bu konumdaki herhangi bir sekme durağını temizler. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
