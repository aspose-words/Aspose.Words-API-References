---
title: ImportFormatOptions.ForceCopyStyles
second_title: Aspose.Words for .NET API Referansı
description: ImportFormatOptions mülk. Bir boole değeri alır veya ayarlar.KeepSourceFormatting mode. Varsayılan değeryanlış .
type: docs
weight: 20
url: /tr/net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

Bir boole değeri alır veya ayarlar.KeepSourceFormatting mode. Varsayılan değer`yanlış` .

```csharp
public bool ForceCopyStyles { get; set; }
```

### Notlar

Varsayılan olarak, bir hedef belgede eşleşen bir stil zaten varsa, kaynak stil formatting doğrudan düğüm niteliklerine genişletilir ve bu düğümün stili bir varsayılana sıfırlanır.

Bu seçenek olarak ayarlandığında`doğru`, kaynak stil benzersiz ada sahip hedef belgeye zorla kopyalanacak ve içe aktarılan düğüme uygulanacaktır.

Bu durumda, belge hedefindeki içe aktarılan düğümün biçimlendirmesinin korunacağının garanti edilmediğine dikkat edin.

### Örnekler

Benzersiz adlara sahip kaynak stillerin zorla nasıl kopyalanacağını gösterir.

```csharp
// Her iki belge de MyStyle1 ve MyStyle2'yi içerir, MyStyle3 yalnızca bir kaynak belgede bulunur.
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
* ad alanı [Aspose.Words](../../importformatoptions/)
* toplantı [Aspose.Words](../../../)


