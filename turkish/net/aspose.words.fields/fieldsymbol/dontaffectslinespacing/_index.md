---
title: FieldSymbol.DontAffectsLineSpacing
linktitle: DontAffectsLineSpacing
articleTitle: DontAffectsLineSpacing
second_title: .NET için Aspose.Words
description: FieldSymbol DontAffectsLineSpacing özelliğinin paragraf satır aralığı üzerindeki karakter etkisini nasıl kontrol ettiğini keşfedin. Belge biçimlendirmenizi bugün optimize edin!
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldsymbol/dontaffectslinespacing/
---
## FieldSymbol.DontAffectsLineSpacing property

Alan tarafından alınan karakterin paragrafın satır aralığını etkileyip etkilemediğini alır veya ayarlar.

```csharp
public bool DontAffectsLineSpacing { get; set; }
```

## Örnekler

SYMBOL alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda, tek bir karakteri görüntülemek için SYMBOL alanını kullanmanın üç yolu bulunmaktadır.
// 1 - ANSI karakter koduyla belirtilen © (Telif Hakkı) sembolünü görüntüleyen bir SİMGE alanı ekleyin:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// ANSI karakter kodu "U+00A9" veya tam sayı biçiminde "169", telif hakkı simgesi için ayrılmıştır.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - ∞ (Sonsuzluk) sembolünü görüntüleyen bir SİMGE alanı ekleyin ve görünümünü değiştirin:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// Unicode'da sonsuzluk simgesi "221E" kodunu kaplar.
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// Windows Karakter Eşlemi'ni kullandıktan sonra sembolümüzün yazı tipini değiştiriyoruz
// yazı tipinin o sembolü temsil edebilmesini sağlamak için.
field.FontName = "Calibri";
field.FontSize = "24";

// Uzun semboller için bu bayrağı ayarlayarak, bunların satırlarındaki metnin geri kalanını aşağıya itmemesini sağlayabiliriz.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - あ karakterini görüntüleyen bir SYMBOL alanı ekleyin,
// Shift-JIS'i (Windows-932) destekleyen bir yazı tipiyle kod sayfası:
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
