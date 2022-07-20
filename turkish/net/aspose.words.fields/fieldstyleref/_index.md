---
title: FieldStyleRef
second_title: Aspose.Words for .NET API Referansı
description: STYLEREF alanını uygular.
type: docs
weight: 2290
url: /tr/net/aspose.words.fields/fieldstyleref/
---
## FieldStyleRef class

STYLEREF alanını uygular.

```csharp
public class FieldStyleRef : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldStyleRef](fieldstyleref)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format) { get; } | [`FieldFormat`](../fieldformat) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldstyleref/insertparagraphnumber) { get; set; } | Başvurulan paragrafın paragraf numarasının tam olarak belgede göründüğü gibi eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinfullcontext) { get; set; } | Başvurulan paragrafın paragraf numarasının tam bağlamda eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinrelativecontext) { get; set; } | Başvurulan paragrafın paragraf numarasının göreli bağlamda eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertRelativePosition](../../aspose.words.fields/fieldstyleref/insertrelativeposition) { get; set; } | Başvurulan paragrafın göreli konumunun eklenip eklenmeyeceğini alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [SearchFromBottom](../../aspose.words.fields/fieldstyleref/searchfrombottom) { get; set; } | Geçerli sayfanın üstünden değil altından arama yapılıp yapılmayacağını alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [StyleName](../../aspose.words.fields/fieldstyleref/stylename) { get; set; } | Aranacak metnin biçimlendirildiği stilin adını alır veya ayarlar. |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldstyleref/suppressnondelimiters) { get; set; } | Sınırlayıcı olmayan karakterlerin bastırılıp bastırılmayacağını alır veya ayarlar. |
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

STYLEREF, belirtilen stille biçimlendirilmiş belge içindeki bir metin parçasına başvurmak için kullanılır.

### Örnekler

STYLEREF alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir Microsoft Word liste şablonu kullanarak bir liste oluşturun.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// Oluşturulan bu listede "1.a )" görüntülenecektir.
 // Köşeli ayraçtan önceki boşluk, bastırabileceğimiz sınırlayıcı olmayan bir karakterdir.
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// STYLEREF alanlarının başvuracağı metin ekleyin ve paragraf stilleri uygulayın.
builder.ListFormat.List = list;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Başlığa bir STYLEREF alanı yerleştirin ve belgedeki ilk "Liste Paragrafı" stili metni görüntüleyin.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// Altbilgiye bir STYLEREF alanı yerleştirin ve son metni göstermesini sağlayın.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// Listelerin liste numaralarını referans almak için STYLEREF alanlarını da kullanabiliriz.
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### Ayrıca bakınız

* class [Field](../field)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
