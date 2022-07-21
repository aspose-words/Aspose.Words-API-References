---
title: FieldEnd
second_title: Aspose.Words for .NET API Referansı
description: Bir belgedeki Word alanının sonunu temsil eder.
type: docs
weight: 1710
url: /tr/net/aspose.words.fields/fieldend/
---
## FieldEnd class

Bir belgedeki Word alanının sonunu temsil eder.

```csharp
public class FieldEnd : FieldChar
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype) { get; } | Alanın türünü döndürür. |
| [Font](../../aspose.words/inline/font) { get; } | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| [HasSeparator](../../aspose.words.fields/fieldend/hasseparator) { get; } | İade **doğru** bu alanda bir ayırıcı varsa. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Bu düğüm başka düğümler içerebiliyorsa true değerini döndürür. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | Bu nesne, değişiklik izleme etkinleştirilirken Microsoft Word'de silindiyse true değerini döndürür. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty) { get; set; } | Alandaki geçerli sonucun belgede yapılan diğer değişiklikler nedeniyle artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | Değişiklik izleme etkinken nesnenin biçimlendirmesi Microsoft Word'de değiştirilirse doğru döndürür. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | Bu nesne, değişiklik izleme etkinken Microsoft Word'e eklendiyse true değerini döndürür. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked) { get; set; } | Üst alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | İade **doğru** değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | İade **doğru** bu nesne, değişiklik izleme etkinken Microsoft Word'de taşındıysa (yerleştirildiyse). |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words.fields/fieldend/nodetype) { get; } | İadeFieldEnd . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Bu düğümün hemen üst öğesini alır. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | Üst öğeyi alır[`Paragraph`](../../aspose.words/paragraph) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldend/accept)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone)(bool) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| [GetField](../../aspose.words.fields/fieldchar/getfield)() | char. alanı için bir alan döndürür |
| override [GetText](../../aspose.words/specialchar/gettext)() | Bu düğümün temsil ettiği özel karakteri alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove)() | Kendini üst öğeden kaldırır. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

[`FieldEnd`](../fieldend) satır içi düzeyde bir düğümdür ve tarafından temsil edilen [`FieldEndChar`](../../aspose.words/controlchar/fieldendchar) belgedeki kontrol karakteri.

[`FieldEnd`](../fieldend) sadece çocuğu olabilir[`Paragraph`](../../aspose.words/paragraph).

Bir Microsoft Word belgesindeki tam alan, alan başlangıç karakteri, alan kodu, alan ayırıcı karakter, alan sonucu ve alan bitiş karakterinden oluşan karmaşık bir yapıdır. Bazı alanlarda yalnızca alan başlangıcı, alan kodu ve alan sonu bulunur.

Bir belgeye kolayca yeni bir alan eklemek için[`InsertField`](../../aspose.words/documentbuilder/insertfield) yöntemi.

### Örnekler

Bir alan koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");
    doc.UpdateFields();

    FieldCollection fields = doc.Range.Fields;

    Assert.AreEqual(6, fields.Count);

    // Alan koleksiyonunu yineleyin ve içeriği yazdırın ve yazın
    // özel bir ziyaretçi uygulaması kullanan her alanın.
    FieldVisitor fieldVisitor = new FieldVisitor();

    using (IEnumerator<Field> fieldEnumerator = fields.GetEnumerator())
    {
        while (fieldEnumerator.MoveNext())
        {
            if (fieldEnumerator.Current != null)
            {
                fieldEnumerator.Current.Start.Accept(fieldVisitor);
                fieldEnumerator.Current.Separator?.Accept(fieldVisitor);
                fieldEnumerator.Current.End.Accept(fieldVisitor);
            }
            else
            {
                Console.WriteLine("There are no fields in the document.");
            }
        }
    }

    Console.WriteLine(fieldVisitor.GetText());

/// <summary>
/// Alan bilgilerini yazdıran belge ziyaretçisi uygulaması.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Ziyaretçi tarafından toplanan belgenin düz metnini alır.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Belgede bir FieldStart düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir FieldSeparator düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir FieldEnd düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### Ayrıca bakınız

* class [FieldChar](../fieldchar)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
