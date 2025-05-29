---
title: Font.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: .NET için Aspose.Words
description: Font Hidden özelliğini keşfedin. Metninizin gizli olarak biçimlendirilip biçimlendirilmediğini kolayca belirleyin. Belgenizin netliğini ve sunumunu bugün geliştirin!
type: docs
weight: 140
url: /tr/net/aspose.words/font/hidden/
---
## Font.Hidden property

Yazı tipi gizli metin olarak biçimlendirilmişse doğrudur.

```csharp
public bool Hidden { get; set; }
```

## Örnekler

Gizli metin dizisinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Gizli bayrağı true olarak ayarlandığında, bu Font nesnesini kullanarak oluşturduğumuz herhangi bir metin belgede görünmez olacaktır.
// "Gizli metin" seçeneğini etkinleştirmediğimiz sürece gizli metni görmeyeceğiz veya vurgulamayacağız
// Microsoft Word'de "Dosya" -> "Seçenekler" -> "Görüntüle" yoluyla bulundu. Metin hala orada olacak,
// ve bu metne programsal olarak erişebileceğiz.
// Hassas bilgileri gizlemek için bu yöntemi kullanmanız önerilmez.
builder.Font.Hidden = true;
builder.Font.Size = 36;

builder.Writeln("This text will not be visible in the document.");

doc.Save(ArtifactsDir + "Font.Hidden.docx");
```

Bir belgeden tüm gizli içeriği kaldırmak için DocumentVisitor uygulamasının nasıl kullanılacağını gösterir.

```csharp
public void RemoveHiddenContentFromDocument()
{
    Document doc = new Document(MyDir + "Hidden content.docx");
    RemoveHiddenContentVisitor hiddenContentRemover = new RemoveHiddenContentVisitor();

    // Aşağıda bir belge ziyaretçisini kabul edebilecek üç tür alan bulunmaktadır:
    // bu, kabul eden düğümü ziyaret etmesine ve daha sonra derinlemesine bir şekilde alt düğümlerini dolaşmasına izin verecektir.
    // 1 - Paragraf düğümü:
    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 4, true);
    para.Accept(hiddenContentRemover);

    // 2 - Tablo düğümü:
    Table table = doc.FirstSection.Body.Tables[0];
    table.Accept(hiddenContentRemover);

    // 3 - Belge düğümü:
    doc.Accept(hiddenContentRemover);

    doc.Save(ArtifactsDir + "Font.RemoveHiddenContentFromDocument.docx");
}

/// <summary>
/// "Gizli içerik" olarak işaretlenen tüm ziyaret edilen düğümleri kaldırır.
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
    /// Belgede bir Yorum ile karşılaşıldığında çağrılır.
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
        Console.WriteLine(specialChar.GetText());

        if (specialChar.Font.Hidden)
            specialChar.Remove();

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Tablo düğümünün ziyareti sona erdiğinde çağrılır.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        // Tablo hücrelerinin içindeki içerik gizli içerik bayrağına sahip olabilir, ancak tabloların kendileri olamaz.
        // Eğer bu tabloda yalnızca gizli içerik olsaydı, bu ziyaretçi bunların hepsini silecekti,
        // ve hiçbir alt düğüm kalmayacaktı.
        // Böylece tablonun kendisini de gizli içerik olarak ele alıp kaldırabiliriz.
        // Boş olan ancak gizli içeriği olmayan tabloların içinde boş paragraflar bulunan hücreler olacaktır,
        // bu ziyaretçinin kaldıramayacağı.
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

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
