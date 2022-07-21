---
title: EditableRange
second_title: Aspose.Words for .NET API Referansı
description: Tek bir düzenlenebilir aralığı temsil eder.
type: docs
weight: 1270
url: /tr/net/aspose.words/editablerange/
---
## EditableRange class

Tek bir düzenlenebilir aralığı temsil eder.

```csharp
public class EditableRange
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [EditableRangeEnd](../../aspose.words/editablerange/editablerangeend) { get; } | Düzenlenebilir aralığın sonunu temsil eden düğümü alır. |
| [EditableRangeStart](../../aspose.words/editablerange/editablerangestart) { get; } | Düzenlenebilir aralığın başlangıcını temsil eden düğümü alır. |
| [EditorGroup](../../aspose.words/editablerange/editorgroup) { get; set; } | Geçerli user öğesinin bu düzenlenebilir aralığı düzenlemesine izin verilip verilmeyeceğini belirlemek için kullanılacak bir takma ad (veya düzenleme grubu) döndürür veya ayarlar. |
| [Id](../../aspose.words/editablerange/id) { get; } | Düzenlenebilir aralık tanımlayıcısını alır. |
| [SingleUser](../../aspose.words/editablerange/singleuser) { get; set; } | Düzenlenebilir aralık için tek kullanıcıyı döndürür veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Remove](../../aspose.words/editablerange/remove)() | Düzenlenebilir aralığı belgeden kaldırır. Düzenlenebilir aralıktaki içeriği kaldırmaz. |

### Notlar

[`EditableRange`](../editablerange) iki düğümü içine alan bir "cephe" nesnesidir[`EditableRangeStart`](./editablerangestart) ve[`EditableRangeEnd`](./editablerangeend) bir belge ağacında ve düzenlenebilir bir aralıkla tek bir nesne olarak çalışmaya izin verir.

### Örnekler

Düzenlenebilir bir aralıkla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Düzenlenebilir aralıklar, korunan belgelerin bölümlerini düzenleme için açık bırakmamıza izin verir.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// İyi biçimlendirilmiş bir düzenlenebilir aralığın bir başlangıç düğümü ve bir bitiş düğümü vardır.
// Bu düğümlerin eşleşen kimlikleri vardır ve düzenlenebilir düğümleri kapsar.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Düzenlenebilir aralığın farklı bölümleri birbirine bağlanır.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Her parçanın düğüm tiplerine bu şekilde ulaşabiliriz. Düzenlenebilir aralığın kendisi bir düğüm değil,
// ancak bir başlangıç, bir son ve bunların kapalı içeriklerinden oluşan bir varlık.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Düzenlenebilir bir aralığı kaldırın. Aralık içindeki tüm düğümler bozulmadan kalacaktır.
editableRange.Remove();
```

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

* ad alanı [Aspose.Words](../../aspose.words)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
