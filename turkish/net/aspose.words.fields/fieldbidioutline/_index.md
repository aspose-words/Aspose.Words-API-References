---
title: Class FieldBidiOutline
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldBidiOutline sınıf. BIDIOUTLINE alanını uygular.
type: docs
weight: 1500
url: /tr/net/aspose.words.fields/fieldbidioutline/
---
## FieldBidiOutline class

BIDIOUTLINE alanını uygular.

```csharp
public class FieldBidiOutline : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldBidiOutline](fieldbidioutline/)() | Default_Constructor |

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

### Notlar

Bu alan, paragraf numaralandırmasının her bir level seviyesini sınırlayan ayırıcı dışında, AUTONUMLGL alanıyla aynıdır.

### Örnekler

BIDIOUTLINE alanlarıyla sağdan sola dil uyumlu listelerin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// BIDIOUTLINE alanı, AUTONUM/LISTNUM alanları gibi paragrafları numaralandırır,
// ancak yalnızca İbranice veya Arapça gibi bir sağdan sola düzenleme dili etkinleştirildiğinde görünür.
// Aşağıdaki alan, "1" liste numarasının RTL karşılığı olan ".1"i gösterecektir.
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// ".2" ve ".3" görüntüleyecek iki BIDIOUTLINE alanı daha ekleyin.
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Belgedeki her paragraf için yatay metin hizalamasını RTL'ye ayarlayın.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Microsoft Word'de sağdan sola düzenleme dilini etkinleştirirsek, alanlarımız sayıları görüntüler.
// Aksi takdirde, "###" gösterecektir.
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


