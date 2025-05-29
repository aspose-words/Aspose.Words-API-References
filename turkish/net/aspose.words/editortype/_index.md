---
title: EditorType Enum
linktitle: EditorType
articleTitle: EditorType
second_title: .NET için Aspose.Words
description: Belge aralığı düzenlemesi için kullanıcı izinlerini kontrol etmek üzere düzenleme gruplarını tanımlayan Aspose.Words.EditorType enum'unu keşfedin. Belge yönetiminizi bugün geliştirin!
type: docs
weight: 1860
url: /tr/net/aspose.words/editortype/
---
## EditorType enumeration

Bir belgenin içindeki düzenlenebilir bir aralık tarafından tanımlanan tek bir aralığı düzenlemesine izin verilip verilmeyeceğini belirlemek için takma ad olarak kullanılabilecek olası takma adlar (veya düzenleme grupları) kümesini belirtir.

```csharp
public enum EditorType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Unspecified | `0` | Editör türünün belirtilmediği anlamına gelir. |
| Administrators | `1` | Yöneticiler grubuyla ilişkili kullanıcıların, belge koruması etkinleştirildiğinde bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemelerine izin verileceğini belirtir. |
| Contributors | `2` | Katkıda Bulunanlar grubuyla ilişkili kullanıcıların, belge koruması etkinleştirildiğinde bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemelerine izin verileceğini belirtir. |
| Current | `3` | Geçerli grupla ilişkili kullanıcıların, belge koruması etkinleştirildiğinde bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemesine izin verileceğini belirtir. |
| Editors | `4` | Düzenleyiciler grubuyla ilişkili kullanıcıların, belge koruması etkinleştirildiğinde bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemelerine izin verileceğini belirtir. |
| Everyone | `5` | Belgeyi açan tüm kullanıcıların, belge koruması etkinleştirildiğinde bu editing türünü kullanarak düzenlenebilir aralıkları düzenlemesine izin verileceğini belirtir. |
| None | `6` | Belgeyi açan kullanıcıların hiçbirinin, belge koruması etkinleştirildiğinde bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemesine izin verilmeyeceğini belirtir. |
| Owners | `7` | Belge koruması etkinleştirildiğinde, Sahipler grubuyla ilişkili kullanıcıların bu düzenleme türünü kullanarak düzenlenebilir aralıkları düzenlemesine izin verileceğini belirtir. |
| Default | `0` | AynısıUnspecified . |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
