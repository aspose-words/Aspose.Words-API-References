---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: .NET için Aspose.Words
description: ImportFormatOptions IgnoreHeaderFooter özelliğini keşfedin, KeepSourceFormatting modunda başlık/altbilgi biçimlendirmesini kontrol edin. Belge içe aktarımlarınızı bugün basitleştirin!
type: docs
weight: 40
url: /tr/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Başlık/altbilgi içeriğinin kaynak biçimlendirmesinin yoksayıldığını belirten bir Boole değeri alır veya ayarlar eğerKeepSourceFormatting mod kullanılır. Varsayılan değer`doğru` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## Örnekler

Başlık/altbilgi içeriğinin kaynak biçimlendirmesinin göz ardı edilip edilmeyeceğinin nasıl belirtileceğini gösterir.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

// 'IgnoreHeaderFooter' yanlışsa, başlık/altbilgi içeriği için orijinal biçimlendirme
// "Header and footer types.docx" kullanılacaktır.
// 'IgnoreHeaderFooter' doğruysa, başlık/altbilgi içeriğinin biçimlendirmesi
// "Document.docx" kullanılacaktır.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### Ayrıca bakınız

* class [ImportFormatOptions](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
