---
title: FieldEQ Class
linktitle: FieldEQ
articleTitle: FieldEQ
second_title: .NET için Aspose.Words
description: Kusursuz EQ alan uygulaması için Aspose.Words.Fields.FieldEQ sınıfını keşfedin. Güçlü özellikler ve esneklikle belge otomasyonunu geliştirin.
type: docs
weight: 2240
url: /tr/net/aspose.words.fields/fieldeq/
---
## FieldEQ class

EQ alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldEQ : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldEQ](fieldeq/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [AsOfficeMath](../../aspose.words.fields/fieldeq/asofficemath/)() | EQ alanına karşılık gelen Office Math nesnesini döndürür. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son alt 'siyse, üst paragrafını döndürür. Alan zaten kaldırılmışsa, şunu döndürür`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alan bağlantısını kaldırma işlemini gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |

## Örnekler

EQ alanının Office Math ile nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Field sample - EQ.docx");
FieldEQ fieldEQ = doc.Range.Fields.OfType<FieldEQ>().First();

OfficeMath officeMath = fieldEQ.AsOfficeMath();

fieldEQ.Start.ParentNode.InsertBefore(officeMath, fieldEQ.Start);
fieldEQ.Remove();

doc.Save(ArtifactsDir + "Field.EQAsOfficeMath.docx");
```

Çeşitli matematiksel denklemleri görüntülemek için EQ alanının nasıl kullanılacağını gösterir.

```csharp
public void FieldEQ()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bir EQ alanı, bir veya daha fazla elemandan oluşan matematiksel bir denklemi görüntüler.
    // Her bir eleman şu formu alır: [anahtar][seçenekler][bağımsız değişkenler].
    // Bir anahtar ve birden fazla olası seçenek olabilir.
    // Argümanlar, yuvarlak parantezlerle çevrelenmiş, virgülle ayrılmış değerler kümesidir.

    // Burada, "\f" anahtarıyla "Kesir"e karşılık gelen bir EQ alanı eklemek için bir belge oluşturucu kullanıyoruz.
    // Argüman olarak 1 ve 4 değerlerini geçireceğiz ve herhangi bir seçenek kullanmayacağız.
    // Bu alan, paydası 1, paydası 4 olan bir kesri görüntüler.
    FieldEQ field = InsertFieldEQ(builder, @"\f(1,4)");

    Assert.AreEqual(@" EQ \f(1,4)", field.GetFieldCode());

    // Bir EQ alanı ardışık olarak yerleştirilmiş birden fazla öğe içerebilir.
    // İç elemanları yerleştirerek elemanları birbirinin içine de yerleştirebiliriz
    // dış elemanların argüman parantezlerinin içinde.
    // Anahtarların tam listesini ve kullanımlarını burada bulabiliriz:
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

     // Aşağıda farklı türde nesneler oluşturmak için kullanabileceğimiz dokuz farklı EQ alan anahtarının uygulamaları bulunmaktadır.
    // 1 - Dizi anahtarı "\a", sola hizalanmış, 2 sütun, 3 yatay ve dikey aralık noktası:
    InsertFieldEQ(builder, @"\a \al \co2 \vs3 \hs3(4x,- 4y,-4x,+ y)");

    // 2 - Parantez anahtarı "\b", parantez karakteri "[", içeriği bir dizi köşeli parantezin içine almak için:
    // Parantezlerin içine bir dizi yerleştirdiğimizi ve bunun çıktıda bir matris gibi görüneceğini unutmayın.
    InsertFieldEQ(builder, @"\b \bc\[ (\a \al \co3 \vs3 \hs3(1,0,0,0,1,0,0,0,1))");

    // 3 - Yer değiştirme anahtarı "\d", "B" metnini "A" metninin 30 satır sağına kaydırır ve boşluğu alt çizgi olarak görüntüler:
    InsertFieldEQ(builder, @"A \d \fo30 \li() B");

    // 4 - Birden fazla kesirden oluşan formül:
    InsertFieldEQ(builder, @"\f(d,dx)(u + v) = \f(du,dx) + \f(dv,dx)");

    // 5 - Toplama sembolü olan integral anahtarı "\i":
    InsertFieldEQ(builder, @"\i \su(n=1,5,n)");

    // 6 - Liste anahtarı "\l":
    InsertFieldEQ(builder, @"\l(1,1,2,3,n,8,13)");

    // 7 - x'in küp kökünü gösteren köklü anahtar "\r":
    InsertFieldEQ(builder, @"\r (3,x)");

    // 8 - Alt simge/üst simge geçişi "/s", önce üst simge olarak, sonra da alt simge olarak:
    InsertFieldEQ(builder, @"\s \up8(Superscript) Text \s \do8(Subscript)");

    // 9 - Girişin üstünde, altında, solunda ve sağında çizgiler bulunan kutu anahtarı "\x":
    InsertFieldEQ(builder, @"\x \to \bo \le \ri(5)");

    // Biraz daha karmaşık kombinasyonlar.
    InsertFieldEQ(builder, @"\a \ac \vs1 \co1(lim,n→∞) \b (\f(n,n2 + 12) + \f(n,n2 + 22) + ... + \f(n,n2 + n2))");
    InsertFieldEQ(builder, @"\i (,,  \b(\f(x,x2 + 3x + 2))) \s \up10(2)");
    InsertFieldEQ(builder, @"\i \in( tan x, \s \up2(sec x), \b(\r(3) )\s \up4(t) \s \up7(2)  dt)");

    doc.Save(ArtifactsDir + "Field.EQ.docx");
}

/// <summary>
/// Bir EQ alanı eklemek, argümanlarını ayarlamak ve yeni bir paragraf başlatmak için bir belge oluşturucu kullanın.
/// </summary>
private static FieldEQ InsertFieldEQ(DocumentBuilder builder, string args)
{
    FieldEQ field = (FieldEQ)builder.InsertField(FieldType.FieldEquation, true);
    builder.MoveTo(field.Separator);
    builder.Write(args);
    builder.MoveTo(field.Start.ParentNode);

    builder.InsertParagraph();
    return field;
}
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
