---
title: TabStop Class
linktitle: TabStop
articleTitle: TabStop
second_title: .NET için Aspose.Words
description: Belge biçimlendirmede özel sekme durakları için çözümünüz olan Aspose.Words.TabStop sınıfını keşfedin. Belgelerinizi hassasiyet ve kolaylıkla geliştirin!
type: docs
weight: 7050
url: /tr/net/aspose.words/tabstop/
---
## TabStop class

Tek bir özel sekme durağını temsil eder.`TabStop` nesne the 'nin bir üyesidir[`TabStopCollection`](../tabstopcollection/) koleksiyon.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) belgeleme makalesi.

```csharp
public sealed class TabStop
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [TabStop](tabstop/#constructor)(*double*) | Bu sınıfın yeni bir örneğini başlatır. |
| [TabStop](tabstop/#constructor_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Bu sınıfın yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | Bu sekme durağında metnin hizalamasını alır veya ayarlar. |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | Geri Döndürür`doğru` eğer bu sekme durağı bu pozisyondaki mevcut sekme duraklarını temizlerse. |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | Sekme karakterinin altında görüntülenen lider çizgisinin türünü alır veya ayarlar. |
| [Position](../../aspose.words/tabstop/position/) { get; } | Sekme durağının konumunu noktalar halinde alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(*TabStop*) | Belirtilenle karşılaştırır`TabStop` . |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | Bu nesne için karma kodunu hesaplar. |

## Notlar

Normalde, bir sekme durağı bir sekme durağının bulunduğu bir konumu belirtir. Ancak, sekme durakları üst stillerden devralınabildiğinden, alt nesne 'nin belirli bir konumda bir sekme durağı olmadığını açıkça tanımlaması gerekebilir. Belirli bir konumda devralınan bir sekme durağını temizlemek için, bir`TabStop` nesne ve set [`Alignment`](./alignment/) ileClear.

Daha fazla bilgi için bkz.[`TabStopCollection`](../tabstopcollection/).

## Örnekler

İçindekiler ile ilgili paragraflarda sağ sekme durağının konumunun nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// TOC sonuç tabanlı stillerle tüm paragraflarda gezinin; bu, TOC ile TOC9 arasındaki herhangi bir stil olabilir.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Bu paragrafta kullanılan ilk sekmeyi al, bu sekme sayfa numaralarını hizalamak için kullanılmalıdır.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // İlk varsayılan sekme durağını özel bir sekme durağıyla değiştir.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
