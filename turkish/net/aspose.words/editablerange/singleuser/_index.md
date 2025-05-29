---
title: EditableRange.SingleUser
linktitle: SingleUser
articleTitle: SingleUser
second_title: .NET için Aspose.Words
description: Düzenlenebilir aralıkları etkin bir şekilde yönetmek, sorunsuz işbirliği ve kullanıcıya özel erişim kontrolü sağlamak için EditableRange SingleUser özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words/editablerange/singleuser/
---
## EditableRange.SingleUser property

Düzenlenebilir aralık için tek kullanıcıyı döndürür veya ayarlar.

```csharp
public string SingleUser { get; set; }
```

## Notlar

Bu düzenleyici aşağıdaki biçimlerden birinde saklanabilir:

DOMAIN\Kullanıcı Adı - Erişimi geçerli kullanıcının etki alanı kimlik bilgileri kullanılarak doğrulanacak kullanıcılar için.

user@domain.com - Kullanıcının e-posta adresini kimlik bilgisi olarak kullanarak erişimi doğrulanacak kullanıcılar için.

kullanıcı - erişimi geçerli kullanıcının makine kimlik bilgileri kullanılarak doğrulanacak kullanıcılar için.

Belirli düzenlenebilir aralık için aynı anda tek kullanıcı ve editör grubu ayarlanamaz, biri ayarlandığında diğeri temizlenir.

## Örnekler

Düzenlenebilir aralıkların düzenleme haklarının belirli bir grup/kullanıcıyla nasıl sınırlanacağını gösterir.

```csharp
public void Visitor()
{
    Document doc = new Document();
    doc.Protect(ProtectionType.ReadOnly, "MyPassword");

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                    " we cannot edit this paragraph without the password.");

    // Belgeleri yazmaya karşı koruduğumuzda, düzenlenebilir aralıklar kullanıcıların düzenleyebileceği belirli alanları seçmemize olanak tanır.
    // İzin verilen editörlerin listesini daraltmanın iki karşılıklı olarak özel yolu vardır.
    // 1 - Bir kullanıcı belirtin:
    EditableRange editableRange = builder.StartEditableRange().EditableRange;
    editableRange.SingleUser = "john.doe@myoffice.com";
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.SingleUser}.");
    builder.EndEditableRange();

    Assert.AreEqual(EditorType.Unspecified, editableRange.EditorGroup);

    // 2 - İzin verilen kullanıcıların ilişkilendirildiği bir grubu belirtin:
    editableRange = builder.StartEditableRange().EditableRange;
    editableRange.EditorGroup = EditorType.Administrators;
    builder.Writeln($"This paragraph is inside the first editable range, can only be edited by {editableRange.EditorGroup}.");
    builder.EndEditableRange();

    Assert.AreEqual(string.Empty, editableRange.SingleUser);

    builder.Writeln("This paragraph is outside the editable range, and cannot be edited by anybody.");

    // Belgedeki düzenlenebilir her aralığın ayrıntılarını ve içeriklerini yazdır.
    EditableRangePrinter editableRangePrinter = new EditableRangePrinter();

    doc.Accept(editableRangePrinter);

    Console.WriteLine(editableRangePrinter.ToText());
}

/// <summary>
/// Ziyaret edilen düzenlenebilir aralıkların özelliklerini ve içeriklerini bir dizgede toplar.
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

* class [EditableRange](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
