---
title: FieldIncludeText
second_title: Aspose.Words for .NET API Referansı
description: INCLUDETEXT alanını uygular.
type: docs
weight: 1900
url: /tr/net/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class

INCLUDETEXT alanını uygular.

```csharp
public class FieldIncludeText : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldIncludeText](fieldincludetext/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldincludetext/bookmarkname/) { get; set; } | Dahil edilecek yer iminin adını alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [Encoding](../../aspose.words.fields/fieldincludetext/encoding/) { get; set; } | Başvurulan dosya içindeki verilere uygulanan kodlamayı alır veya ayarlar. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [LockFields](../../aspose.words.fields/fieldincludetext/lockfields/) { get; set; } | Dahil edilen belgedeki alanların güncellenmesinin engellenip engellenmeyeceğini alır veya ayarlar. |
| [MimeType](../../aspose.words.fields/fieldincludetext/mimetype/) { get; set; } | Başvurulan dosyanın MIME türünü alır veya ayarlar. |
| [NamespaceMappings](../../aspose.words.fields/fieldincludetext/namespacemappings/) { get; set; } | XPath sorguları için ad alanı eşlemelerini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [SourceFullName](../../aspose.words.fields/fieldincludetext/sourcefullname/) { get; set; } | Bir IRI kullanarak belgenin konumunu alır veya ayarlar. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [TextConverter](../../aspose.words.fields/fieldincludetext/textconverter/) { get; set; } | Dahil edilen dosyanın biçimi için metin dönüştürücünün adını alır veya ayarlar. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |
| [XPath](../../aspose.words.fields/fieldincludetext/xpath/) { get; set; } | XML dosyasının istenen bölümü için XPath'i alır veya ayarlar. |
| [XslTransformation](../../aspose.words.fields/fieldincludetext/xsltransformation/) { get; set; } | XML verilerini biçimlendirmek için XSL Dönüşümünün konumunu alır veya ayarlar. |

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

Başka bir belgede bulunan metin ve grafiklerin tamamını veya bir kısmını ekler.

### Örnekler

INCLUDETEXT alanının nasıl oluşturulacağını ve özelliklerinin nasıl ayarlanacağını gösterir.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Aşağıda, yerel dosya sisteminde bir XML dosyasının içeriğini görüntülemek için INCLUDETEXT alanlarını kullanmanın iki yolu bulunmaktadır.
    // 1 - Bir XML belgesinde bir XSL dönüşümü gerçekleştirin:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 - Bir XML belgesinden belirli öğeleri almak için bir XPath kullanın:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");

/// <summary>
/// Özel özelliklere sahip bir INCLUDETEXT alanı eklemek için bir belge oluşturucu kullanın.
/// </summary>
public FieldIncludeText CreateFieldIncludeText(DocumentBuilder builder, string sourceFullName, bool lockFields, string mimeType, string textConverter, string encoding)
{
    FieldIncludeText fieldIncludeText = (FieldIncludeText)builder.InsertField(FieldType.FieldIncludeText, true);
    fieldIncludeText.SourceFullName = sourceFullName;
    fieldIncludeText.LockFields = lockFields;
    fieldIncludeText.MimeType = mimeType;
    fieldIncludeText.TextConverter = textConverter;
    fieldIncludeText.Encoding = encoding;

    return fieldIncludeText;
}
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
