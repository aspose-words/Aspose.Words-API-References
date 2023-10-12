---
title: Class FieldEQ
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldEQ sınıf. EQ alanını uygular.
type: docs
weight: 1830
url: /tr/net/aspose.words.fields/fieldeq/
---
## FieldEQ class

EQ alanını uygular.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

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
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir alır[`FieldFormat`](../fieldformat/) Alanın formatlamasına yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplanmamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. Olabilir`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [AsOfficeMath](../../aspose.words.fields/fieldeq/asofficemath/)() | EQ alanına karşılık gelen Office Math nesnesini döndürür. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son child 'si ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa şunu döndürür:`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alanın bağlantısını kaldırır. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Örnekler

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

    // Bir EQ alanı, bir veya daha fazla öğeden oluşan bir matematiksel denklemi görüntüler.
    // Her öğe şu biçimi alır: [anahtar][seçenekler][argümanlar].
    // Bir anahtar ve birden fazla olası seçenek olabilir.
    // Argümanlar, yuvarlak parantezler içine alınmış, virgülle ayrılmış değerler kümesidir.

    // Burada "Kesir"e karşılık gelen "\f" anahtarıyla bir EQ alanı eklemek için bir belge oluşturucu kullanıyoruz.
    // 1 ve 4 değerlerini argüman olarak ileteceğiz ve herhangi bir seçenek kullanmayacağız.
    // Bu alanda payı 1, paydası 4 olan bir kesir görüntülenecektir.
    FieldEQ field = InsertFieldEQ(builder, @"\f(1,4)");

    Assert.AreEqual(@" EQ \f(1,4)", field.GetFieldCode());

    // Bir EQ alanı ardışık olarak yerleştirilmiş birden fazla öğe içerebilir.
    // İç elemanları yerleştirerek elemanları iç içe de yerleştirebiliriz.
    // dış elemanların bağımsız değişken parantezlerinin içinde.
    // Anahtarların tam listesini kullanımlarıyla birlikte burada bulabiliriz:
    // https://blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/

     // Aşağıda farklı türde nesneler oluşturmak için kullanabileceğimiz dokuz farklı EQ alan anahtarının uygulamaları bulunmaktadır.
    // 1 - Dizi anahtarı "\a", sola hizalanmış, 2 sütun, 3 nokta yatay ve dikey aralık:
    InsertFieldEQ(builder, @"\a \al \co2 \vs3 \hs3(4x,- 4y,-4x,+ y)");

    // 2 - Köşeli parantez anahtarı "\b", köşeli parantez karakteri "[", içeriği köşeli parantez içine almak için:
    // Çıkışta tamamen bir matris gibi görünecek olan parantezlerin içine bir dizi yerleştirdiğimizi unutmayın.
    InsertFieldEQ(builder, @"\b \bc\[ (\a \al \co3 \vs3 \hs3(1,0,0,0,1,0,0,0,1))");

    // 3 - Yer değiştirme anahtarı "\d", "B" metnini "A"nın 30 boşluk sağına kaydırır ve boşluğu alt çizgi olarak görüntüler:
    InsertFieldEQ(builder, @"A \d \fo30 \li() B");

    // 4 - Çoklu kesirlerden oluşan formül:
    InsertFieldEQ(builder, @"\f(d,dx)(u + v) = \f(du,dx) + \f(dv,dx)");

    // 5 - Toplama sembollü "\i" integral anahtarı:
    InsertFieldEQ(builder, @"\i \su(n=1,5,n)");

    // 6 - Liste anahtarı "\l":
    InsertFieldEQ(builder, @"\l(1,1,2,3,n,8,13)");

    // 7 - X'in küp kökünü görüntüleyen radikal anahtar "\r":
    InsertFieldEQ(builder, @"\r (3,x)");

    // 8 - Alt simge/üst simge geçişi "/s", önce üst simge, sonra alt simge olarak:
    InsertFieldEQ(builder, @"\s \up8(Superscript) Text \s \do8(Subscript)");

    // 9 - Girişin üstünde, altında, solunda ve sağında çizgiler bulunan "\x" kutu anahtarı:
    InsertFieldEQ(builder, @"\x \to \bo \le \ri(5)");

    // Bazı daha karmaşık kombinasyonlar.
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


