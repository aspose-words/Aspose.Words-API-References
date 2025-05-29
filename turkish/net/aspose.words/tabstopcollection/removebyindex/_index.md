---
title: TabStopCollection.RemoveByIndex
linktitle: RemoveByIndex
articleTitle: RemoveByIndex
second_title: .NET için Aspose.Words
description: RemoveByIndex yöntemiyle sekme duraklarınızı zahmetsizce yönetin. Sorunsuz bir tasarım için koleksiyonunuzdan herhangi bir sekme durağını hızla kaldırın.
type: docs
weight: 110
url: /tr/net/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection.RemoveByIndex method

Koleksiyondan belirtilen dizindeki bir sekme durağını kaldırır.

```csharp
public void RemoveByIndex(int index)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| index | Int32 | Sekme duraklarının koleksiyonuna ait bir dizin. |

## Örnekler

Bir belgedeki sekme durağının dizinine göre nasıl seçileceğini ve kaldırılacağını gösterir.

```csharp
Document doc = new Document();
TabStopCollection tabStops = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.TabStops;

tabStops.Add(ConvertUtil.MillimeterToPoint(30), TabAlignment.Left, TabLeader.Dashes);
tabStops.Add(ConvertUtil.MillimeterToPoint(60), TabAlignment.Left, TabLeader.Dashes);

Assert.AreEqual(2, tabStops.Count);

// İlk sekme durağını kaldır.
tabStops.RemoveByIndex(0);

Assert.AreEqual(1, tabStops.Count);

doc.Save(ArtifactsDir + "TabStopCollection.RemoveByIndex.docx");
```

### Ayrıca bakınız

* class [TabStopCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
