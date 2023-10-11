---
title: ImportFormatOptions.IgnoreHeaderFooter
second_title: Aspose.Words for .NET API Referansı
description: ImportFormatOptions mülk. Üstbilgi/altbilgi içeriğinin kaynak biçimlendirmesinin göz ardı edildiğini belirten bir boole değeri alır veya ayarlar ifKeepSourceFormatting modu kullanılır. Varsayılan değerdoğru .
type: docs
weight: 40
url: /tr/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Üstbilgi/altbilgi içeriğinin kaynak biçimlendirmesinin göz ardı edildiğini belirten bir boole değeri alır veya ayarlar ifKeepSourceFormatting modu kullanılır. Varsayılan değer:`doğru` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

### Örnekler

Üstbilgi/altbilgi içeriğinin kaynak biçimlendirmesinin yoksayılıp yok sayılacağının nasıl belirleneceğini gösterir.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### Ayrıca bakınız

* class [ImportFormatOptions](../)
* ad alanı [Aspose.Words](../../importformatoptions/)
* toplantı [Aspose.Words](../../../)


