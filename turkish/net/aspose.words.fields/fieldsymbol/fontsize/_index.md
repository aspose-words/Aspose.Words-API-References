---
title: FieldSymbol.FontSize
linktitle: FontSize
articleTitle: FontSize
second_title: Aspose.Words for .NET
description: FieldSymbol FontSize mülk. Alan tarafından alınan karakterin yazı tipinin punto cinsinden boyutunu alır veya ayarlar C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.fields/fieldsymbol/fontsize/
---
## FieldSymbol.FontSize property

Alan tarafından alınan karakterin yazı tipinin punto cinsinden boyutunu alır veya ayarlar.

```csharp
public string FontSize { get; set; }
```

## Örnekler

SEMBOL alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda tek bir karakteri görüntülemek için SEMBOL alanını kullanmanın üç yolu verilmiştir.
// 1 - ANSI karakter koduyla belirtilen © (Telif Hakkı) sembolünü görüntüleyen bir SEMBOL alanı ekleyin:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// ANSI karakter kodu "U+00A9" veya tamsayı biçimindeki "169", telif hakkı sembolüne ayrılmıştır.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - ∞ (Sonsuzluk) sembolünü görüntüleyen bir SEMBOL alanı ekleyin ve görünümünü değiştirin:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// Unicode'da sonsuzluk simgesi "221E" kodunun başında gelir.
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// Windows Karakter Eşlemini kullandıktan sonra sembolümüzün yazı tipini değiştirin
// yazı tipinin o sembolü temsil edebildiğinden emin olmak için.
field.FontName = "Calibri";
field.FontSize = "24";

// Metnin geri kalanını kendi satırlarında aşağı itmemeleri için bu bayrağı uzun semboller için ayarlayabiliriz.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - あ karakterini görüntüleyen bir SEMBOL alanı ekleyin,
// Shift-JIS (Windows-932) kod sayfasını destekleyen bir yazı tipiyle:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);
field.FontName = "MS Gothic";
field.CharacterCode = 0x82A0.ToString();
field.IsShiftJis = true;

Assert.AreEqual(" SYMBOL  33440 \\f \"MS Gothic\" \\j", field.GetFieldCode());

builder.Write("Line 3");

doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### Ayrıca bakınız

* class [FieldSymbol](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
