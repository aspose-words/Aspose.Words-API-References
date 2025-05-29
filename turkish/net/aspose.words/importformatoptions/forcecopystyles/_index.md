---
title: ImportFormatOptions.ForceCopyStyles
linktitle: ForceCopyStyles
articleTitle: ForceCopyStyles
second_title: .NET için Aspose.Words
description: ImportFormatOptions ForceCopyStyles özelliğini keşfedin, KeepSourceFormatting modunda stil kopyalamayı kolayca kontrol edin. En iyi sonuçlar için varsayılan değer false'tur.
type: docs
weight: 30
url: /tr/net/aspose.words/importformatoptions/forcecopystyles/
---
## ImportFormatOptions.ForceCopyStyles property

Çakışan styles 'yi kopyalamak için bir Boole değeri alır veya ayarlar.KeepSourceFormatting mode. Varsayılan değer`YANLIŞ` .

```csharp
public bool ForceCopyStyles { get; set; }
```

## Notlar

Varsayılan olarak, eşleşen bir stil hedef belgede zaten mevcutsa, kaynak stil formatting doğrudan düğüm özniteliklerine genişletilir ve bu düğümün stili varsayılana sıfırlanır.

Bu seçenek ayarlandığında`doğru`, kaynak stil, benzersiz bir adla hedef belgeye zorla kopyalanacak ve içe aktarılan düğüme uygulanacaktır.

Bu durumda, hedef document içindeki içe aktarılan düğümün biçimlendirmesinin korunacağının garantisi yoktur.

## Örnekler

Kaynak stillerinin benzersiz adlarla zorla nasıl kopyalanacağını gösterir.

```csharp
// Her iki belge de MyStyle1 ve MyStyle2'yi içerir, MyStyle3 yalnızca kaynak belgede bulunur.
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
