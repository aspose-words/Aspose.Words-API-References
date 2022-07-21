---
title: FieldSymbol
second_title: Aspose.Words for .NET API Referansı
description: Bir SEMBOL alanı uygular.
type: docs
weight: 2310
url: /tr/net/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class

Bir SEMBOL alanı uygular.

```csharp
public class FieldSymbol : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldSymbol](fieldsymbol)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CharacterCode](../../aspose.words.fields/fieldsymbol/charactercode) { get; set; } | Karakterin kod noktası değerini ondalık veya onaltılık olarak alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [DontAffectsLineSpacing](../../aspose.words.fields/fieldsymbol/dontaffectslinespacing) { get; set; } | Alan tarafından alınan karakterin paragrafın satır aralığını etkileyip etkilemediğini alır veya ayarlar. |
| [End](../../aspose.words.fields/field/end) { get; } | Alan sonunu temsil eden düğümü alır. |
| [FontName](../../aspose.words.fields/fieldsymbol/fontname) { get; set; } | Alan tarafından alınan karakterin yazı tipinin adını alır veya ayarlar. |
| [FontSize](../../aspose.words.fields/fieldsymbol/fontsize) { get; set; } | Alan tarafından alınan karakterin yazı tipinin punto cinsinden boyutunu alır veya ayarlar. |
| [Format](../../aspose.words.fields/field/format) { get; } | [`FieldFormat`](../fieldformat) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [IsAnsi](../../aspose.words.fields/fieldsymbol/isansi) { get; set; } | Karakter kodunun bir ANSI karakterinin değeri olarak yorumlanıp yorumlanmayacağını alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [IsShiftJis](../../aspose.words.fields/fieldsymbol/isshiftjis) { get; set; } | Karakter kodunun bir SHIFT-JIS karakterinin değeri olarak yorumlanıp yorumlanmayacağını alır veya ayarlar. |
| [IsUnicode](../../aspose.words.fields/fieldsymbol/isunicode) { get; set; } | Karakter kodunun bir Unicode karakterin değeri olarak yorumlanıp yorumlanmayacağını alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Notlar

Kod noktası değeri ondalık veya onaltılık olarak belirtilen karakteri alır.

### Örnekler

SEMBOL alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda, tek bir karakter görüntülemek için bir SEMBOL alanını kullanmanın üç yolu bulunmaktadır.
// 1 - Bir ANSI karakter koduyla belirtilen © (Telif hakkı) sembolünü görüntüleyen bir SEMBOL alanı ekleyin:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// ANSI karakter kodu "U+00A9" veya tamsayı biçiminde "169" telif hakkı sembolü için ayrılmıştır.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - ∞ (Sonsuzluk) sembolünü görüntüleyen bir SEMBOL alanı ekleyin ve görünümünü değiştirin:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// Unicode'da sonsuzluk sembolü "221E" kodunu kaplar.
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// Windows Karakter Haritasını kullandıktan sonra sembolümüzün yazı tipini değiştirin
// yazı tipinin bu sembolü temsil etmesini sağlamak için.
field.FontName = "Calibri";
field.FontSize = "24";

// Metnin geri kalanını satırlarında aşağı itmemelerini sağlamak için bu bayrağı uzun semboller için ayarlayabiliriz.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - あ karakterini gösteren bir SEMBOL alanı ekleyin,
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

* class [Field](../field)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
