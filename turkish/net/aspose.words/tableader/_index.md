---
title: TabLeader Enum
linktitle: TabLeader
articleTitle: TabLeader
second_title: .NET için Aspose.Words
description: Projelerinizde sekmeler için öncü çizgi stilleri tanımlayan, belge biçimlendirmesini ve okunabilirliğini artıran Aspose.Words.TabLeader enum'unu keşfedin.
type: docs
weight: 7040
url: /tr/net/aspose.words/tableader/
---
## TabLeader enumeration

Sekme karakterinin altında görüntülenen lider çizgisinin türünü belirtir.

```csharp
public enum TabLeader
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Lider çizgisi görüntülenmiyor. |
| Dots | `1` | Lider çizgisi noktalardan oluşur. |
| Dashes | `2` | Lider çizgisi çizgilerden oluşur. |
| Line | `3` | Lider çizgisi tek bir çizgidir. |
| Heavy | `4` | Lider çizgisi tek bir kalın çizgidir. |
| MiddleDot | `5` | Lider çizgisi orta noktalardan oluşur. |

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
