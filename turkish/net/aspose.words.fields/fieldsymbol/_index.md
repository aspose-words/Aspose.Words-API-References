---
title: FieldSymbol Class
linktitle: FieldSymbol
articleTitle: FieldSymbol
second_title: .NET için Aspose.Words
description: Verimli SYMBOL alanı uygulaması için Aspose.Words.Fields.FieldSymbol sınıfını keşfedin ve belge işleme yeteneklerinizi geliştirin.
type: docs
weight: 2870
url: /tr/net/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class

Bir SYMBOL alanı uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldSymbol : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldSymbol](fieldsymbol/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CharacterCode](../../aspose.words.fields/fieldsymbol/charactercode/) { get; set; } | Karakterin kod noktası değerini ondalık veya onaltılık olarak alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [DontAffectsLineSpacing](../../aspose.words.fields/fieldsymbol/dontaffectslinespacing/) { get; set; } | Alan tarafından alınan karakterin paragrafın satır aralığını etkileyip etkilemediğini alır veya ayarlar. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [FontName](../../aspose.words.fields/fieldsymbol/fontname/) { get; set; } | Alan tarafından alınan karakterin yazı tipinin adını alır veya ayarlar. |
| [FontSize](../../aspose.words.fields/fieldsymbol/fontsize/) { get; set; } | Alan tarafından alınan karakterin yazı tipinin boyutunu nokta cinsinden alır veya ayarlar. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsAnsi](../../aspose.words.fields/fieldsymbol/isansi/) { get; set; } | Karakter kodunun bir ANSI karakterinin değeri olarak yorumlanıp yorumlanmayacağını alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [IsShiftJis](../../aspose.words.fields/fieldsymbol/isshiftjis/) { get; set; } | Karakter kodunun bir SHIFT-JIS karakterinin değeri olarak yorumlanıp yorumlanmayacağını alır veya ayarlar. |
| [IsUnicode](../../aspose.words.fields/fieldsymbol/isunicode/) { get; set; } | Karakter kodunun bir Unicode karakterinin değeri olarak yorumlanıp yorumlanmayacağını alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son alt 'siyse, üst paragrafını döndürür. Alan zaten kaldırılmışsa, şunu döndürür`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alan bağlantısını kaldırma işlemini gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |

## Notlar

Kod noktası değeri ondalık veya onaltılık olarak belirtilen karakteri alır.

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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
