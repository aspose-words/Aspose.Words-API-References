---
title: Class FieldEQ
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldEQ sınıf. EQ alanını uygular.
type: docs
weight: 1680
url: /tr/net/aspose.words.fields/fieldeq/
---
## FieldEQ class

EQ alanını uygular.

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
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Örnekler

Çeşitli matematiksel denklemleri görüntülemek için EQ alanının nasıl kullanılacağını gösterir.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bir EQ alanı, bir veya daha fazla öğeden oluşan matematiksel bir denklem görüntüler.
    // Her öğe şu biçimi alır: [switch][options][arguments].
    // Bir anahtar ve birkaç olası seçenek olabilir.
    // Argümanlar, yuvarlak parantez içine alınmış, virgülle ayrılmış değerler kümesidir.

    // Burada, "Kesir"e karşılık gelen "\f" anahtarıyla bir EQ alanı eklemek için bir belge oluşturucu kullanıyoruz.
    // 1 ve 4 değerlerini argüman olarak ileteceğiz ve herhangi bir seçenek kullanmayacağız.
    // Bu alan, pay olarak 1 ve payda olarak 4 olan bir kesir gösterecektir.
    FieldEQ field = InsertFieldEQ(builder, @"\f(1,4)");

    Assert.AreEqual(@" EQ \f(1,4)", field.GetFieldCode());

    // Bir EQ alanı, sırayla yerleştirilmiş birden çok öğe içerebilir.
    // İç elemanları yerleştirerek elemanları iç içe de yerleştirebiliriz.
    // dış elemanların argüman parantezlerinin içinde.
    // Anahtarların tam listesini ve kullanımlarını burada bulabiliriz:
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

    // Aşağıda, farklı türde nesneler oluşturmak için kullanabileceğimiz dokuz farklı EQ alan anahtarının uygulamaları bulunmaktadır.
    // 1 - "\a" dizi anahtarı, sola hizalanmış, 2 sütun, 3 nokta yatay ve dikey boşluk:
    InsertFieldEQ(builder, @"\a \al \co2 \vs3 \hs3(4x,- 4y,-4x,+ y)");

    // 2 - İçeriği bir dizi köşeli parantez içine almak için köşeli ayraç anahtarı "\b", köşeli ayraç karakteri "[":
    // Çıktıda tamamen bir matris gibi görünecek olan bir diziyi parantez içine yerleştirdiğimizi unutmayın.
    InsertFieldEQ(builder, @"\b \bc\[ (\a \al \co3 \vs3 \hs3(1,0,0,0,1,0,0,0,1))");

    // 3 - "\d" yer değiştirme anahtarı, "B" metnini "A"nın sağında 30 boşluk bırakarak, boşluğu alt çizgi olarak gösterir:
    InsertFieldEQ(builder, @"A \d \fo30 \li() B");

    // 4 - Birden çok kesirden oluşan formül:
    InsertFieldEQ(builder, @"\f(d,dx)(u + v) = \f(du,dx) + \f(dv,dx)");

    // 5 - Toplam sembollü "\i" integral anahtarı:
    InsertFieldEQ(builder, @"\i \su(n=1,5,n)");

    // 6 - "\l" liste anahtarı:
    InsertFieldEQ(builder, @"\l(1,1,2,3,n,8,13)");

    // 7 - x'in küp kökünü gösteren "\r" radikal anahtarı:
    InsertFieldEQ(builder, @"\r (3,x)");

    // 8 - Alt simge/üst simge anahtarı "/s", önce bir üst simge ve sonra bir alt simge olarak:
    InsertFieldEQ(builder, @"\s \up8(Superscript) Text \s \do8(Subscript)");

    // 9 - Girişin üstünde, altında, solunda ve sağında çizgiler bulunan "\x" kutu anahtarı:
    InsertFieldEQ(builder, @"\x \to \bo \le \ri(5)");

    // Bazı daha karmaşık kombinasyonlar.
    InsertFieldEQ(builder, @"\a \ac \vs1 \co1(lim,n→∞) \b (\f(n,n2 + 12) + \f(n,n2 + 22) + ... + \f(n,n2 + n2))");
    InsertFieldEQ(builder, @"\i (,,  \b(\f(x,x2 + 3x + 2))) \s \up10(2)");
    InsertFieldEQ(builder, @"\i \in( tan x, \s \up2(sec x), \b(\r(3) )\s \up4(t) \s \up7(2)  dt)");

    doc.Save(ArtifactsDir + "Field.EQ.docx");

/// <summary>
/// EQ alanı eklemek, argümanlarını ayarlamak ve yeni bir paragraf başlatmak için bir belge oluşturucu kullanın.
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


