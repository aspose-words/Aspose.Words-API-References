---
title: ImportFormatOptions.ForceCopyStyles
linktitle: ForceCopyStyles
articleTitle: ForceCopyStyles
second_title: Aspose.Words for .NET
description: ImportFormatOptions ForceCopyStyles mülk. Çakışan stillerin nin kopyalanacağını belirten bir boole değeri alır veya ayarlar.KeepSourceFormatting mode. Varsayılan değerYANLIŞ  C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

Çakışan stillerin 'nin kopyalanacağını belirten bir boole değeri alır veya ayarlar.KeepSourceFormatting mode. Varsayılan değer:`YANLIŞ` .

```csharp
public bool ForceCopyStyles { get; set; }
```

## Notlar

Varsayılan olarak, hedef belgede eşleşen bir stil zaten mevcutsa, kaynak stili formatting doğrudan düğüm niteliklerine genişletilir ve bu düğümün stili varsayılana sıfırlanır.

Bu seçenek olarak ayarlandığında`doğru`, kaynak stili benzersiz bir adla hedef belgeye zorla kopyalanacak ve içe aktarılan düğüme uygulanacaktır.

Bu durumda, hedef document 'de içe aktarılan düğümün formatının korunacağının garanti edilmediğini unutmayın.

## Örnekler

Benzersiz adlara sahip kaynak stillerinin zorla nasıl kopyalanacağını gösterir.

```csharp
// Her iki belge de MyStyle1 ve MyStyle2'yi içeriyor, MyStyle3 yalnızca kaynak belgede mevcut.
Document srcDoc = new Document(MyDir + "Styles source.docx");
Document dstDoc = new Document(MyDir + "Styles destination.docx");

ImportFormatOptions options = new ImportFormatOptions { ForceCopyStyles = true };
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

ParagraphCollection paras = dstDoc.Sections[1].Body.Paragraphs;

Assert.AreEqual(paras[0].ParagraphFormat.Style.Name, "MyStyle1_0");
Assert.AreEqual(paras[1].ParagraphFormat.Style.Name, "MyStyle2_0");
Assert.AreEqual(paras[2].ParagraphFormat.Style.Name, "MyStyle3");
```

### Ayrıca bakınız

* class [ImportFormatOptions](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
