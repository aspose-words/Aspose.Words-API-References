---
title: Class TabStop
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.TabStop sınıf. Tek bir özel sekme durağını temsil eder. bu Sekme Durdur nesne the nin bir üyesidirTabStopCollection koleksiyon.
type: docs
weight: 5900
url: /tr/net/aspose.words/tabstop/
---
## TabStop class

Tek bir özel sekme durağını temsil eder. bu **Sekme Durdur** nesne the 'nin bir üyesidir[`TabStopCollection`](../tabstopcollection/) koleksiyon.

```csharp
public sealed class TabStop
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [TabStop](tabstop/#constructor)(double) | Bu sınıfın yeni bir örneğini başlatır. |
| [TabStop](tabstop/#constructor_1)(double, TabAlignment, TabLeader) | Bu sınıfın yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | Bu sekme durağındaki metnin hizalamasını alır veya ayarlar. |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | Bu sekme durağı, bu konumdaki mevcut sekme duraklarını temizlerse true değerini döndürür. |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | Sekme karakteri altında görüntülenen öncü çizginin türünü alır veya ayarlar. |
| [Position](../../aspose.words/tabstop/position/) { get; } | Sekme durağının konumunu noktalar olarak alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(TabStop) | Belirtilen TabStop. ile karşılaştırır |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | Bu nesne için karma kodu hesaplar. |

### Notlar

Normalde, bir sekme durağı, bir sekme durağının bulunduğu bir konumu belirtir. Ancak, sekme durakları üst stillerden miras alınabileceğinden, alt nesne öğesinin belirli bir konumda sekme durağı olmadığını açıkça tanımlaması gerekebilir. Belirli bir konumda devralınan bir sekme durağını temizlemek için bir **Sekme Durdur** nesne ve set [`Alignment`](./alignment/) ile`TabAlignment.Clear`.

Daha fazla bilgi için, bkz[`TabStopCollection`](../tabstopcollection/).

### Örnekler

TOC ile ilgili paragraflarda sağ sekme durağının konumunun nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// İçindekiler sonuç tabanlı stiller ile tüm paragrafları yineleyin; Bu, TOC ve TOC9 arasındaki herhangi bir stildir.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Bu paragrafta kullanılan ilk sekmeyi alın, bu, sayfa numaralarını hizalamak için kullanılan sekme olmalıdır.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // İlk varsayılan sekmeyi değiştirin, özel bir sekme durağı ile durdurun.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


