---
title: EditableRangeEnd
second_title: Aspose.Words for .NET API Referansı
description: Bir Word belgesindeki düzenlenebilir aralığın sonunu temsil eder.
type: docs
weight: 1280
url: /tr/net/aspose.words/editablerangeend/
---
## EditableRangeEnd class

Bir Word belgesindeki düzenlenebilir aralığın sonunu temsil eder.

```csharp
public sealed class EditableRangeEnd : Node
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [EditableRangeStart](../../aspose.words/editablerangeend/editablerangestart) { get; } | Karşılık gelen EditableRangeStart, ID tarafından alındı. |
| [Id](../../aspose.words/editablerangeend/id) { get; set; } | Düzenlenebilir aralığın tanımlayıcısını belirtir. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Bu düğüm başka düğümler içerebiliyorsa true değerini döndürür. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words/editablerangeend/nodetype) { get; } | İadeEditableRangeEnd . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Bu düğümün hemen üst öğesini alır. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words/editablerangeend/accept)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [Clone](../../aspose.words/node/clone)(bool) | Düğümün bir kopyasını oluşturur. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| virtual [GetText](../../aspose.words/node/gettext)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove)() | Kendini üst öğeden kaldırır. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

Bir Word belgesindeki eksiksiz bir düzenlenebilir aralık, bir[`EditableRangeStart`](./editablerangestart) ve eşleşen[`EditableRangeEnd`](../editablerangeend) aynı kimlikle

[`EditableRangeStart`](./editablerangestart) ve[`EditableRangeEnd`](../editablerangeend) yalnızca, düzenlenebilir aralığın nerede başlayıp nerede bittiğini belirten bir document içindeki işaretlerdir.

Kullan[`EditableRange`](../editablerange)tek bir nesne olarak düzenlenebilir bir aralığıyla çalışmak için "cephe" olarak sınıflandırın.

Şu anda düzenlenebilir aralıklar yalnızca satır içi düzeyde desteklenir, yani[`Paragraph`](../paragraph), ancak düzenlenebilir aralık başlangıcı ve düzenlenebilir aralık sonu farklı paragraflarda olabilir.

### Örnekler

Düzenlenebilir aralıkların düzenleme haklarının belirli bir grup/kullanıcıyla nasıl sınırlandırılacağını gösterir.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // Belgeleri yazmaya karşı koruduğumuzda, düzenlenebilir aralıklar, kullanıcıların düzenleyebileceği belirli alanları seçmemize izin verir.
    // İzin verilen düzenleyiciler listesini daraltmanın birbirini dışlayan iki yolu vardır.
    // 1 - Bir kullanıcı belirtin:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - İzin verilen kullanıcıların aşağıdakilerle ilişkilendirildiği bir grup belirtin:
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Belgedeki her düzenlenebilir aralığın ayrıntılarını ve içeriğini yazdırın.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// Bir dizgede ziyaret edilen düzenlenebilir aralıkların özelliklerini ve içeriğini toplar.
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
    /// Belgede bir EditableRangeStart düğümüyle karşılaşıldığında çağrılır.
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
    /// Belgede bir EditableRangeEnd düğümüyle karşılaşıldığında çağrılır.
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

* class [Node](../node)
* ad alanı [Aspose.Words](../../aspose.words)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
