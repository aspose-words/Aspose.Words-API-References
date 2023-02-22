---
title: TabStopCollection.Add
second_title: Aspose.Words for .NET API Referansı
description: TabStopCollection yöntem. Koleksiyonda bir sekme durağı ekler veya onun yerini alır.
type: docs
weight: 30
url: /tr/net/aspose.words/tabstopcollection/add/
---
## Add(TabStop) {#add}

Koleksiyonda bir sekme durağı ekler veya onun yerini alır.

```csharp
public void Add(TabStop tabStop)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| tabStop | TabStop | Eklenecek bir sekme durağı nesnesi. |

### Notlar

Belirtilen konumda bir sekme durağı zaten varsa, değiştirilir.

### Örnekler

Bir belgeye özel sekme duraklarının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Aşağıda, "ParagraphFormat" özelliği aracılığıyla bir paragrafın sekme durakları koleksiyonuna sekme durakları eklemenin iki yolu vardır.
// 1 - Bir "TabStop" nesnesi oluşturun ve ardından onu koleksiyona ekleyin:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - Yeni bir sekme durağının özellikleri için değerleri "Ekle" yöntemine iletin:
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
* ad alanı [Aspose.Words](../../tabstopcollection/)
* toplantı [Aspose.Words](../../../)

---

## Add(double, TabAlignment, TabLeader) {#add_1}

Koleksiyonda bir sekme durağı ekler veya onun yerini alır.

```csharp
public void Add(double position, TabAlignment alignment, TabLeader leader)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| position | Double | Sekme durağının ekleneceği konum (nokta olarak). |
| alignment | TabAlignment | A[`TabAlignment`](../../tabalignment/)that değeri, sekme durağındaki metnin hizalamasını belirtir. |
| leader | TabLeader | A[`TabLeader`](../../tableader/) that değeri, sekme karakterinin altında görüntülenen öncü satırın türünü belirtir. |

### Notlar

Belirtilen konumda bir sekme durağı zaten varsa, değiştirilir.

### Örnekler

Bir belgeye özel sekme duraklarının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Aşağıda, "ParagraphFormat" özelliği aracılığıyla bir paragrafın sekme durakları koleksiyonuna sekme durakları eklemenin iki yolu vardır.
// 1 - Bir "TabStop" nesnesi oluşturun ve ardından onu koleksiyona ekleyin:
TabStop tabStop = new TabStop(ConvertUtil.InchToPoint(3), TabAlignment.Left, TabLeader.Dashes);
paragraph.ParagraphFormat.TabStops.Add(tabStop);

// 2 - Yeni bir sekme durağının özellikleri için değerleri "Ekle" yöntemine iletin:
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
* ad alanı [Aspose.Words](../../tabstopcollection/)
* toplantı [Aspose.Words](../../../)


