---
title: FieldPrint Class
linktitle: FieldPrint
articleTitle: FieldPrint
second_title: .NET için Aspose.Words
description: Sorunsuz PRINT alanı uygulaması için Aspose.Words.Fields.FieldPrint sınıfını keşfedin. Belge işlemenizi bugün güçlü özellikler ile geliştirin!
type: docs
weight: 2690
url: /tr/net/aspose.words.fields/fieldprint/
---
## FieldPrint class

PRINT alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldPrint : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldPrint](fieldprint/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [PostScriptGroup](../../aspose.words.fields/fieldprint/postscriptgroup/) { get; set; } | PostScript talimatlarının üzerinde çalıştığı çizim dikdörtgenini alır veya ayarlar. |
| [PrinterInstructions](../../aspose.words.fields/fieldprint/printerinstructions/) { get; set; } | Yazıcıya özgü kontrol kodu karakterlerini veya PostScript talimatlarını alır veya ayarlar. |
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

Belge yazdırıldığında yazıcıya özgü kontrol kodu karakterlerini seçili yazıcıya gönderme talimatı.

## Örnekler

PRINT alanının eklenmesini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// PRINT alanı yazıcıya talimat gönderebilir.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// Yazıcının talimatları uygulayacağı alanı ayarlayın.
// Bu durumda PRINT alanımızı içeren paragraf olacaktır.
field.PostScriptGroup = "para";

// Belgemizi yazdırmak için PostScript'i destekleyen bir yazıcı kullandığımızda,
// bu komut "field.PostScriptGroup"ta belirttiğimiz alanın tamamını beyaza çevirecektir.
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
