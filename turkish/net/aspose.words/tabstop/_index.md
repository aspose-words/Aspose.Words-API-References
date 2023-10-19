---
title: TabStop Class
linktitle: TabStop
articleTitle: TabStop
second_title: Aspose.Words for .NET
description: Aspose.Words.TabStop sınıf. Tek bir özel sekme durağını temsil eder.TabStopnesne the nin bir üyesidirTabStopCollection koleksiyon C#'da.
type: docs
weight: 6200
url: /tr/net/aspose.words/tabstop/
---
## TabStop class

Tek bir özel sekme durağını temsil eder.`TabStop`nesne the 'nin bir üyesidir[`TabStopCollection`](../tabstopcollection/) koleksiyon.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokümantasyon makalesi.

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
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | Bu sekme durağındaki metnin hizalamasını alır veya ayarlar. |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | İadeler`doğru` bu sekme durağı bu konumdaki mevcut sekme duraklarını siliyorsa. |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | Sekme karakterinin altında görüntülenen öncü çizginin türünü alır veya ayarlar. |
| [Position](../../aspose.words/tabstop/position/) { get; } | Sekme durağının konumunu nokta olarak alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(*TabStop*) | Belirtilenle karşılaştırır`TabStop` . |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | Bu nesnenin karma kodunu hesaplar. |

## Notlar

Normalde sekme durağı, sekme durağının bulunduğu konumu belirtir. Ancak sekme durakları üst stillerden miras alınabildiğinden, alt object 'nin belirli bir konumda sekme durağı olmadığını açıkça tanımlaması gerekebilir. Belirli bir konumda devralınan bir sekme durağını clear için, bir`TabStop` nesne ve set [`Alignment`](./alignment/) ileClear.

Daha fazla bilgi için bakınız[`TabStopCollection`](../tabstopcollection/).

## Örnekler

İçindekiler ile ilgili paragraflarda sağ sekme durağının konumunun nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// İçindekiler sonuç tabanlı stillerle tüm paragrafları yineleyin; bu, TOC ve TOC9 arasındaki herhangi bir stildir.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Bu paragrafta kullanılan ilk sekmeyi alın, bu sayfa numaralarını hizalamak için kullanılan sekme olmalıdır.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // İlk varsayılan sekmeyi değiştirin, özel bir sekme durağıyla durdurun.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
