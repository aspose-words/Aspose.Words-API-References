---
title: TabStopCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: TabStopCollection Add yöntem. Koleksiyona bir sekme durağı ekler veya değiştirir C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words/tabstopcollection/add/
---
## Add(*[TabStop](../../tabstop/)*) {#add}

Koleksiyona bir sekme durağı ekler veya değiştirir.

```csharp
public void Add(TabStop tabStop)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| tabStop | TabStop | Eklenecek bir sekme durağı nesnesi. |

## Notlar

Belirtilen konumda zaten bir sekme durağı varsa değiştirilir.

## Örnekler

Bir belgeye özel sekme duraklarının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Aşağıda "ParagraphFormat" özelliği aracılığıyla bir paragrafın sekme durakları koleksiyonuna sekme durakları eklemenin iki yolu verilmiştir.
// 1 - Bir "TabStop" nesnesi oluşturun ve ardından onu koleksiyona ekleyin:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - Yeni bir sekme durağının özelliklerine ilişkin değerleri "Ekle" yöntemine iletin:
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Tüm paragraflara 5 cm'de sekme durakları ekleyin.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Her "sekme" karakteri, oluşturucunun imlecini bir sonraki sekme durağının konumuna götürür.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### Ayrıca bakınız

* class [TabStop](../../tabstop/)
* class [TabStopCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## Add(*double, [TabAlignment](../../tabalignment/), [TabLeader](../../tableader/)*) {#add_1}

Koleksiyona bir sekme durağı ekler veya değiştirir.

```csharp
public void Add(double position, TabAlignment alignment, TabLeader leader)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| position | Double | Sekme durağının ekleneceği konum (nokta cinsinden). |
| alignment | TabAlignment | A[`TabAlignment`](../../tabalignment/) that değeri, sekme durağındaki metnin hizalamasını belirtir. |
| leader | TabLeader | A[`TabLeader`](../../tableader/) değer that sekme karakterinin altında görüntülenen lider çizgisinin türünü belirtir. |

## Notlar

Belirtilen konumda zaten bir sekme durağı varsa değiştirilir.

## Örnekler

Bir belgeye özel sekme duraklarının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Aşağıda "ParagraphFormat" özelliği aracılığıyla bir paragrafın sekme durakları koleksiyonuna sekme durakları eklemenin iki yolu verilmiştir.
// 1 - Bir "TabStop" nesnesi oluşturun ve ardından onu koleksiyona ekleyin:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - Yeni bir sekme durağının özelliklerine ilişkin değerleri "Ekle" yöntemine iletin:
paragraph.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(100), TabAlignment.Left,
    TabLeader.Dashes);

// Tüm paragraflara 5 cm'de sekme durakları ekleyin.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
{
    para.ParagraphFormat.TabStops.Add(ConvertUtil.MillimeterToPoint(50), TabAlignment.Left,
        TabLeader.Dashes);
}

// Her "sekme" karakteri, oluşturucunun imlecini bir sonraki sekme durağının konumuna götürür.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.Save(ArtifactsDir + "TabStopCollection.AddTabStops.docx");
```

### Ayrıca bakınız

* enum [TabAlignment](../../tabalignment/)
* enum [TabLeader](../../tableader/)
* class [TabStopCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
