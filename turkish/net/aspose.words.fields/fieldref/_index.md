---
title: FieldRef
second_title: Aspose.Words for .NET API Referansı
description: REF alanını uygular.
type: docs
weight: 2180
url: /tr/net/aspose.words.fields/fieldref/
---
## FieldRef class

REF alanını uygular.

```csharp
public class FieldRef : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldRef](fieldref/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldref/bookmarkname/) { get; set; } | Başvurulan yer iminin adını alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [IncludeNoteOrComment](../../aspose.words.fields/fieldref/includenoteorcomment/) { get; set; } | Yer imi tarafından işaretlenen dipnot, son not ve ek açıklama numaralarının artırılıp artırılmayacağını ve ilgili dipnotu, son notu ve yorum metnini ekleyip eklememeyi ayarlar. |
| [InsertHyperlink](../../aspose.words.fields/fieldref/inserthyperlink/) { get; set; } | Yer işaretli paragrafa bir köprü oluşturulup oluşturulmayacağını alır veya ayarlar. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldref/insertparagraphnumber/) { get; set; } | Başvurulan paragrafın paragraf numarasının tam olarak belgede göründüğü gibi eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldref/insertparagraphnumberinfullcontext/) { get; set; } | Başvurulan paragrafın paragraf numarasının tam bağlamda eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldref/insertparagraphnumberinrelativecontext/) { get; set; } | Başvurulan paragrafın paragraf numarasının göreli bağlamda eklenip eklenmeyeceğini alır veya ayarlar. |
| [InsertRelativePosition](../../aspose.words.fields/fieldref/insertrelativeposition/) { get; set; } | Başvurulan paragrafın göreli konumunun eklenip eklenmeyeceğini alır veya ayarlar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [NumberSeparator](../../aspose.words.fields/fieldref/numberseparator/) { get; set; } | Sıra numaralarını ve sayfa numaralarını ayırmak için kullanılan karakter sırasını alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldref/suppressnondelimiters/) { get; set; } | Sınırlayıcı olmayan karakterlerin bastırılıp bastırılmayacağını alır veya ayarlar. |
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

Belirtilen yer imi tarafından temsil edilen metin veya grafikleri ekler.

### Örnekler

SET alanıyla işaretlenmiş metnin nasıl oluşturulacağını ve ardından bir REF alanı kullanarak belgede nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // İşaretlenmiş metni bir SET alanıyla adlandırın.
// Bu alan, metin içinde görünen bir yer imi yapısına değil, adlandırılmış bir değişkene "yer imi" anlamına gelir.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Bir REF alanında yer imine ada göre bakın ve içeriğini görüntüleyin.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

Referans yer imlerine REF alanlarının nasıl ekleneceğini gösterir.

```csharp
public void FieldRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #1");
    builder.Write("Text that will appear in REF field");
    builder.InsertFootnote(FootnoteType.Footnote, "MyBookmark footnote #2");
    builder.EndBookmark("MyBookmark");
    builder.MoveToDocumentStart();

    // Köşeli parantezlerin şu anda bulunduğumuz liste seviyesini gösterdiği özel bir liste formatı uygulayacağız.
    builder.ListFormat.ApplyNumberDefault();
    builder.ListFormat.ListLevel.NumberFormat = "> \x0000";

    // Yer imimizdeki metni içerecek, bir köprü görevi görecek ve yer iminin dipnotlarını klonlayacak bir REF alanı ekleyin.
    FieldRef field = InsertFieldRef(builder, "MyBookmark", "", "\n");
    field.IncludeNoteOrComment = true;
    field.InsertHyperlink = true;

    Assert.AreEqual(" REF  MyBookmark \\f \\h", field.GetFieldCode());

    // Bir REF alanı ekleyin ve başvurulan yer iminin bunun üstünde mi yoksa altında mı olduğunu görüntüleyin.
    field = InsertFieldRef(builder, "MyBookmark", "The referenced paragraph is ", " this field.\n");
    field.InsertRelativePosition = true;

    Assert.AreEqual(" REF  MyBookmark \\p", field.GetFieldCode());

    // Yer iminin liste numarasını belgede göründüğü şekilde görüntüleyin.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number is ", "\n");
    field.InsertParagraphNumber = true;

    Assert.AreEqual(" REF  MyBookmark \\n", field.GetFieldCode());

    // Yer iminin liste numarasını görüntüleyin, ancak açılı ayraçlar gibi sınırlayıcı olmayan karakterler atlandı.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's paragraph number, non-delimiters suppressed, is ", "\n");
    field.InsertParagraphNumber = true;
    field.SuppressNonDelimiters = true;

    Assert.AreEqual(" REF  MyBookmark \\n \\t", field.GetFieldCode());

    // Bir liste düzeyi aşağı git.
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">> \x0001";

    // Yer iminin liste numarasını ve üstündeki tüm liste düzeylerinin numaralarını görüntüleyin.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's full context paragraph number is ", "\n");
    field.InsertParagraphNumberInFullContext = true;

    Assert.AreEqual(" REF  MyBookmark \\w", field.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Bu REF alanı ile referans aldığı yer imi arasındaki liste düzeyi numaralarını görüntüleyin.
    field = InsertFieldRef(builder, "MyBookmark", "The bookmark's relative paragraph number is ", "\n");
    field.InsertParagraphNumberInRelativeContext = true;

    Assert.AreEqual(" REF  MyBookmark \\r", field.GetFieldCode());

    // Belgenin sonunda yer imi burada bir liste öğesi olarak görünecektir.
    builder.Writeln("List level above bookmark");
    builder.ListFormat.ListLevelNumber++;
    builder.ListFormat.ListLevel.NumberFormat = ">>> \x0002";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.REF.docx");

/// <summary>
/// Belge oluşturucunun bir REF alanı eklemesini, onunla bir yer işaretine başvurmasını ve ondan önce ve sonra metin eklemesini sağlayın.
/// </summary>
private static FieldRef InsertFieldRef(DocumentBuilder builder, string bookmarkName, string textBefore, string textAfter)
{
    builder.Write(textBefore);
    FieldRef field = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
    field.BookmarkName = bookmarkName;
    builder.Write(textAfter);
    return field;
}
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
