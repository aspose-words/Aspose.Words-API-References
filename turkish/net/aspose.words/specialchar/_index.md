---
title: SpecialChar
second_title: Aspose.Words for .NET API Referansı
description: Belgedeki özel karakterler için temel sınıf.
type: docs
weight: 5800
url: /tr/net/aspose.words/specialchar/
---
## SpecialChar class

Belgedeki özel karakterler için temel sınıf.

```csharp
public class SpecialChar : Inline
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [Font](../../aspose.words/inline/font/) { get; } | Bu nesnenin yazı tipi biçimlendirmesine erişim sağlar. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Bu düğüm başka düğümler içerebiliyorsa true değerini döndürür. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Bu nesne, değişiklik izleme etkinleştirilirken Microsoft Word'de silindiyse true değerini döndürür. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Değişiklik izleme etkinken nesnenin biçimlendirmesi Microsoft Word'de değiştirilirse doğru döndürür. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Bu nesne, değişiklik izleme etkinken Microsoft Word'e eklendiyse true değerini döndürür. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | İade **doğru** değişiklik izleme etkinken bu nesne Microsoft Word'de taşındıysa (silindiyse). |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | İade **doğru** bu nesne, değişiklik izleme etkinken Microsoft Word'de taşındıysa (yerleştirildiyse). |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words/specialchar/nodetype/) { get; } | İade **NodeType.SpecialChar** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün hemen üst öğesini alır. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Üst öğeyi alır[`Paragraph`](../paragraph/) bu düğümün. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/specialchar/accept/)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| override [GetText](../../aspose.words/specialchar/gettext/)() | Bu düğümün temsil ettiği özel karakteri alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

Bir Microsoft Word belgesi, alanları, form alanlarını, şekilleri, OLE nesnelerini, dipnotları vb. temsil eden bir dizi özel karakter içerebilir. Özel karakterlerin list listesi için bkz.[`ControlChar`](../controlchar/).

**ÖzelKarakter** bir satır içi düğümdür ve yalnızca alt öğesi olabilir **Paragraf**.

**ÖzelKarakter** char, Aspose.Words'ün programatik erişim sağladığı özel karakterleri temsil eden daha özel sınıflar için temel sınıf olarak kullanılır.  **ÖzelKarakter** sınıfın kendisi ayrıca, Aspose.Words'ün ayrıntılı programlı erişim sağlamadığı özel karakteri temsil etmek için de kullanılır.

### Örnekler

Bir belgeden tüm gizli içeriği kaldırmak için DocumentVisitor uygulamasının nasıl kullanılacağını gösterir.

```csharp
{
    Document doc = new Document(MyDir + "Hidden content.docx");

    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // Aşağıda bir belge ziyaretçisini kabul edebilecek üç tür alan bulunmaktadır,
    // bu, kabul eden düğümü ziyaret etmesine ve ardından alt düğümlerini derinlik öncelikli bir şekilde geçmesine izin verecek.
    // 1 - Paragraf düğümü:
    Paragraph para = (Paragraph) doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - Tablo düğümü:
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - Belge düğümü:
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");

/// <summary>
/// "Gizli içerik" olarak işaretlenmiş tüm ziyaret edilen düğümleri kaldırır.
/// </summary>
public class RemoveHiddenContentVisitor : DocumentVisitor
{
    /// <summary>
    /// Belgede bir FieldStart düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        if (fieldStart.Font.Hidden)
            fieldStart.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir FieldEnd düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.Font.Hidden)
            fieldEnd.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir FieldSeparator düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        if (fieldSeparator.Font.Hidden)
            fieldSeparator.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Çalıştırma düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (run.Font.Hidden)
            run.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Paragraf düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        if (paragraph.ParagraphBreakFont.Hidden)
            paragraph.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir FormField ile karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFormField(FormField formField)
    {
        if (formField.Font.Hidden)
            formField.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir GroupShape ile karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        if (groupShape.Font.Hidden)
            groupShape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Şekil ile karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        if (shape.Font.Hidden)
            shape.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Açıklama ile karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitCommentStart(Comment comment)
    {
        if (comment.Font.Hidden)
            comment.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Dipnot ile karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitFootnoteStart(Footnote footnote)
    {
        if (footnote.Font.Hidden)
            footnote.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir SpecialCharacter ile karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitSpecialChar(SpecialChar specialChar)
    {
        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Tablo düğümünün ziyareti sona erdiğinde çağrılır.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // Tablo hücrelerinin içindeki içerik, gizli içerik bayrağına sahip olabilir, ancak tabloların kendileri olamaz.
        // Bu tabloda gizli içerikten başka bir şey olmasaydı, bu ziyaretçi hepsini kaldırırdı,
        // ve hiçbir alt düğüm kalmayacaktı.
        // Böylece tablonun kendisini de gizli içerik olarak değerlendirebilir ve kaldırabiliriz.
        // Boş ama gizli içeriği olmayan tablolarda, içinde boş paragraflar bulunan hücreler olacaktır,
        // bu ziyaretçinin kaldırmayacağı.
        if (!table.HasChildNodes)
            table.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Hücre düğümünün ziyareti sona erdiğinde çağrılır.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        if (!cell.HasChildNodes && cell.ParentNode != null)
            cell.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Satır düğümünün ziyareti sona erdiğinde çağrılır.
    /// </summary>
    public override VisitorAction VisitRowEnd(Row row)
    {
        if (!row.HasChildNodes && row.ParentNode != null)
            row.Remove();

        return VisitorAction.Continue;
    }
}
```

### Ayrıca bakınız

* class [Inline](../inline/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
