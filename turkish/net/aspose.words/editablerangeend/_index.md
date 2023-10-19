---
title: EditableRangeEnd Class
linktitle: EditableRangeEnd
articleTitle: EditableRangeEnd
second_title: Aspose.Words for .NET
description: Aspose.Words.EditableRangeEnd sınıf. Bir Word belgesindeki düzenlenebilir aralığın sonunu temsil eder C#'da.
type: docs
weight: 1430
url: /tr/net/aspose.words/editablerangeend/
---
## EditableRangeEnd class

Bir Word belgesindeki düzenlenebilir aralığın sonunu temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokümantasyon makalesi.

```csharp
public sealed class EditableRangeEnd : Node
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [EditableRangeStart](../../aspose.words/editablerangeend/editablerangestart/) { get; } | Karşılık gelen[`EditableRangeStart`](../editablerangestart/) , ID. tarafından alındı |
| [Id](../../aspose.words/editablerangeend/id/) { get; set; } | Düzenlenebilir aralığın tanımlayıcısını belirtir. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | İadeler`doğru` bu düğüm başka düğümler içeriyorsa. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonra gelen düğümü alır. |
| override [NodeType](../../aspose.words/editablerangeend/nodetype/) { get; } | İadelerEditableRangeEnd . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün doğrudan ebeveynini alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir değeri döndürür[`Range`](../range/) Bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/editablerangeend/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Ziyaretçi kabul eder. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Belirtilenin ilk atayı alır[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atayı alır. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ön sipariş ağaç geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Düğümün içeriğini belirtilen formatta bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

Bir Word belgesindeki düzenlenebilir aralığın tamamı aşağıdakilerden oluşur:[`EditableRangeStart`](./editablerangestart/) ve eşleşen bir`EditableRangeEnd` aynı kimliğe sahip.

[`EditableRangeStart`](./editablerangestart/) Ve`EditableRangeEnd` düzenlenebilir aralığın nerede başlayıp nerede bittiğini belirten, document içindeki işaretçilerdir yalnızca.

Kullan[`EditableRange`](../editablerange/)Düzenlenebilir bir aralığıyla tek bir nesne olarak çalışmak için sınıfı bir "cephe" olarak kullanın.

Şu anda düzenlenebilir aralıklar yalnızca satır içi düzeyde, yani içeride desteklenmektedir[`Paragraph`](../paragraph/), ancak düzenlenebilir aralık başlangıcı ve düzenlenebilir aralık sonu farklı paragraflarda olabilir.

## Örnekler

Düzenlenebilir aralıkların düzenleme haklarının belirli bir grup/kullanıcıyla nasıl sınırlandırılacağını gösterir.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // Belgeleri yazmaya karşı koruduğumuzda, düzenlenebilir aralıklar kullanıcıların düzenleyebileceği belirli alanları seçmemize olanak tanır.
    // İzin verilen düzenleyicilerin listesini daraltmanın birbirini dışlayan iki yolu vardır.
    // 1 - Bir kullanıcı belirtin:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - İzin verilen kullanıcıların ilişkilendirildiği bir grup belirtin:
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Belgedeki düzenlenebilir her aralığın ayrıntılarını ve içeriğini yazdırın.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// Ziyaret edilen düzenlenebilir aralıkların özelliklerini ve içeriğini bir dizede toplar.
/// </summary>
public class EditableRangePrinter : DocumentVisitor
{
    public EditableRangePrinter()
    {
        mBuilder = new StringBuilder();
    }

    public string ToText()
    {
        return mBuilder.ToString();
    }

    public void Reset()
    {
        mBuilder.Clear();
        mInsideEditableRange = false;
    }

    /// <summary>
    /// Belgede EditableRangeStart düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitEditableRangeStart(EditableRangeStart editableRangeStart)
    {
        mBuilder.AppendLine(" -- Editable range found! -- ");
        mBuilder.AppendLine("\tID:\t\t" + editableRangeStart.Id);
        if (editableRangeStart.EditableRange.SingleUser == string.Empty)
            mBuilder.AppendLine("\tGroup:\t" + editableRangeStart.EditableRange.EditorGroup);
        else
            mBuilder.AppendLine("\tUser:\t" + editableRangeStart.EditableRange.SingleUser);
        mBuilder.AppendLine("\tContents:");

        mInsideEditableRange = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede EditableRangeEnd düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
    {
        mBuilder.AppendLine(" -- End of editable range --\n");

        mInsideEditableRange = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Çalıştırma düğümüyle karşılaşıldığında çağrılır. Bu ziyaretçi yalnızca düzenlenebilir aralıklar içindeki çalıştırmaları kaydeder.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mInsideEditableRange) mBuilder.AppendLine("\t\"" + run.Text + "\"");

        return VisitorAction.Continue;
    }

    private bool mInsideEditableRange;
    private readonly StringBuilder mBuilder;
}
```

### Ayrıca bakınız

* class [Node](../node/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
