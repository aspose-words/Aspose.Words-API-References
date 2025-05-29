---
title: FieldDde Class
linktitle: FieldDde
articleTitle: FieldDde
second_title: .NET için Aspose.Words
description: Kusursuz DDE alan uygulaması için Aspose.Words.Fields.FieldDde sınıfını keşfedin. Belge otomasyonunuzu bugün güçlü özellikler ile geliştirin!
type: docs
weight: 2190
url: /tr/net/aspose.words.fields/fielddde/
---
## FieldDde class

DDE alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldDde : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldDde](fielddde/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AutoUpdate](../../aspose.words.fields/fielddde/autoupdate/) { get; set; } | Bu alanın otomatik olarak güncellenip güncellenmeyeceğini alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [InsertAsBitmap](../../aspose.words.fields/fielddde/insertasbitmap/) { get; set; } | Bağlantılı nesnenin bir bitmap olarak eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertAsHtml](../../aspose.words.fields/fielddde/insertashtml/) { get; set; } | Bağlantılı nesnenin HTML biçimli metin olarak eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertAsPicture](../../aspose.words.fields/fielddde/insertaspicture/) { get; set; } | Bağlantılı nesnenin resim olarak eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertAsRtf](../../aspose.words.fields/fielddde/insertasrtf/) { get; set; } | Bağlantılı nesnenin zengin metin biçiminde (RTF) eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertAsText](../../aspose.words.fields/fielddde/insertastext/) { get; set; } | Bağlantılı nesnenin yalnızca metin biçiminde eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertAsUnicode](../../aspose.words.fields/fielddde/insertasunicode/) { get; set; } | Bağlantılı nesnenin Unicode metni olarak eklenip eklenmeyeceğini alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLinked](../../aspose.words.fields/fielddde/islinked/) { get; set; } | Grafik verilerinin belgeyle birlikte depolanmaması yoluyla dosya boyutunun azaltılıp azaltılmayacağını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [ProgId](../../aspose.words.fields/fielddde/progid/) { get; set; } | Bağlantı bilgilerinin uygulama türünü alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [SourceFullName](../../aspose.words.fields/fielddde/sourcefullname/) { get; set; } | Kaynak dosyanın adını ve konumunu alır veya ayarlar. |
| [SourceItem](../../aspose.words.fields/fielddde/sourceitem/) { get; set; } | Bağlantı kurulan kaynak dosyanın bölümünü alır veya ayarlar. |
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

Başka bir uygulamadan kopyalanan bilgiler için bu alan, DDE kullanarak bu bilgileri orijinal kaynak dosyasına bağlar.

## Örnekler

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini görüntülemek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

```csharp
public void FieldLinkedObjectsAsText(InsertLinkedObjectAs insertLinkedObjectAs)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Aşağıda, bağlantılı bir belgedeki içerikleri metin biçiminde görüntülemek için kullanabileceğimiz üç tür alan bulunmaktadır.
    // 1 - Bir BAĞLANTI alanı:
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", MyDir + "Document.docx", null, true);

    // 2 - Bir DDE alanı:
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - Bir DDEAUTO alanı:
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.docx");
}

public void FieldLinkedObjectsAsImage(InsertLinkedObjectAs insertLinkedObjectAs)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Aşağıda, bağlantılı bir belgedeki içerikleri resim biçiminde görüntülemek için kullanabileceğimiz üç tür alan bulunmaktadır.
    // 1 - Bir BAĞLANTI alanı:
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "MySpreadsheet.xlsx",
        "Sheet1!R2C2", true);

    // 2 - Bir DDE alanı:
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - Bir DDEAUTO alanı:
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
}

/// <summary>
/// Bir LINK alanı eklemek ve özelliklerini parametrelere göre ayarlamak için bir belge oluşturucu kullanın.
/// </summary>
private static void InsertFieldLink(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool shouldAutoUpdate)
{
    FieldLink field = (FieldLink)builder.InsertField(FieldType.FieldLink, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;

    builder.Writeln("\n");
}

/// <summary>
/// Bir DDE alanı eklemek için bir belge oluşturucu kullanın ve özelliklerini parametrelere göre ayarlayın.
/// </summary>
private static void InsertFieldDde(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs, string progId,
    string sourceFullName, string sourceItem, bool isLinked, bool shouldAutoUpdate)
{
    FieldDde field = (FieldDde)builder.InsertField(FieldType.FieldDDE, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;

    builder.Writeln("\n");
}

/// <summary>
/// DDEAUTO alanını eklemek ve özelliklerini parametrelere göre ayarlamak için bir belge oluşturucu kullanın.
/// </summary>
private static void InsertFieldDdeAuto(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool isLinked)
{
    FieldDdeAuto field = (FieldDdeAuto)builder.InsertField(FieldType.FieldDDEAuto, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;
}

public enum InsertLinkedObjectAs
{
    // BağlantılıNesneMetinOlarak
    Text,
    Unicode,
    Html,
    Rtf,
    // BağlantılıNesneGörüntüOlarak
    Picture,
    Bitmap
}
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
