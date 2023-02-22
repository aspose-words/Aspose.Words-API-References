---
title: Class DocumentVisitor
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.DocumentVisitor sınıf. Özel belge ziyaretçileri için temel sınıf.
type: docs
weight: 460
url: /tr/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

Özel belge ziyaretçileri için temel sınıf.

```csharp
public abstract class DocumentVisitor
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab/)(AbsolutePositionTab) | Bir[`AbsolutePositionTab`](../absolutepositiontab/) belgede düğümle karşılaşıldı. |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend/)(Body) | Bir bölümdeki ana metin öyküsünün numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart/)(Body) | Bir bölümdeki ana metin öyküsünün numaralandırılması başladığında çağrılır. |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend/)(BookmarkEnd) | Belgede bir yer işaretinin sonuyla karşılaşıldığında çağrılır. |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart/)(BookmarkStart) | Belgede bir yer işareti başlangıcı ile karşılaşıldığında çağrılır. |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend/)(BuildingBlock) | Bir yapı taşının numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart/)(BuildingBlock) | Bir yapı taşının numaralandırılması başladığında çağrılır. |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend/)(Cell) | Bir tablo hücresinin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart/)(Cell) | Bir tablo hücresinin numaralandırılması başladığında çağrılır. |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend/)(Comment) | Bir yorum metninin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend/)(CommentRangeEnd) | Yorumlanan bir metin aralığının sonuyla karşılaşıldığında çağrılır. |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart/)(CommentRangeStart) | Yorumlanmış bir metin aralığının başlangıcıyla karşılaşıldığında çağrılır. |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart/)(Comment) | Bir yorum metninin numaralandırılması başladığında çağrılır. |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend/)(Document) | Belgenin numaralandırılması bittiğinde çağrılır. |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart/)(Document) | Belgenin numaralandırılması başladığında çağrılır. |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend/)(EditableRangeEnd) | Belgede düzenlenebilir bir aralığın sonuyla karşılaşıldığında çağrılır. |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart/)(EditableRangeStart) | Belgede düzenlenebilir bir aralığın başlangıcıyla karşılaşıldığında çağrılır. |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend/)(FieldEnd) | Belgede bir alan bittiğinde çağrılır. |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator/)(FieldSeparator) | Belgede bir alan ayırıcıyla karşılaşıldığında çağrılır. |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart/)(FieldStart) | Belgede bir alan başladığında çağrılır. |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend/)(Footnote) | Bir dipnotun veya sonnot metninin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart/)(Footnote) | Bir dipnotun veya sonnot metninin numaralandırılması başladığında çağrılır. |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield/)(FormField) | Belgede bir form alanıyla karşılaşıldığında çağrılır. |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend/)(GlossaryDocument) | Sözlük belgesinin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart/)(GlossaryDocument) | Bir sözlük belgesinin numaralandırılması başladığında çağrılır. |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend/)(GroupShape) | Bir grup şeklinin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart/)(GroupShape) | Bir grup şeklinin numaralandırılması başladığında çağrılır. |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend/)(HeaderFooter) | Bir bölümdeki üstbilgi veya altbilginin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart/)(HeaderFooter) | Bir bölümdeki üstbilgi veya altbilginin numaralandırılması başladığında çağrılır. |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend/)(OfficeMath) | Bir Office Math nesnesinin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart/)(OfficeMath) | Bir Office Math nesnesinin numaralandırılması başladığında çağrılır. |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend/)(Paragraph) | Paragrafın numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart/)(Paragraph) | Bir paragrafın numaralandırılması başladığında çağrılır. |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend/)(Row) | Bir tablo satırının numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart/)(Row) | Bir tablo satırının numaralandırılması başladığında çağrılır. |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun/)(Run) | içinde bir metin akışıyla karşılaşıldığında çağrılır. |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend/)(Section) | Bir bölümün numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart/)(Section) | Bir bölümün numaralandırılması başladığında çağrılır. |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend/)(Shape) | Şeklin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart/)(Shape) | Bir şeklin numaralandırılması başladığında çağrılır. |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend/)(SmartTag) | Akıllı etiketin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart/)(SmartTag) | Akıllı etiketin numaralandırılması başladığında çağrılır. |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar/)(SpecialChar) | Bir[`SpecialChar`](../specialchar/) belgede düğümle karşılaşıldı. |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend/)(StructuredDocumentTag) | Yapılandırılmış bir belge etiketinin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend/)(StructuredDocumentTagRangeEnd) |  |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart/)(StructuredDocumentTagRangeStart) |  |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart/)(StructuredDocumentTag) | Yapılandırılmış bir belge etiketinin numaralandırılması başladığında çağrılır. |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument/)(SubDocument) | Bir alt Belge ile karşılaşıldığında çağrılır. |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend/)(Table) | Bir tablonun numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart/)(Table) | Bir tablonun numaralandırılması başladığında çağrılır. |

### Notlar

İle birlikte **Belge Ziyaretçisi** belge ağacı üzerinde numaralandırma gerektiren özel operasyonlar tanımlayabilir ve yürütebilirsiniz.

Örneğin, Aspose.Words şunları kullanır: **Belge Ziyaretçisi** tasarruf için dahili olarak **Belge** çeşitli biçimlerde ve bir belgenin bir parçası üzerinde alanları veya yer imlerini bulma gibi diğer işlemler için.

Kullanmak **Belge Ziyaretçisi**:

1. Türetilmiş bir sınıf oluşturun **Belge Ziyaretçisi**.
2. Bazı özel işlemleri gerçekleştirmek için VisitXXX yöntemlerinin bazılarına veya tümüne uygulamaları geçersiz kılın ve sağlayın.
3. Telefon etmek[`Düğüm.Kabul Et`](../node/accept/) üzerinde **düğüm** that numaralandırmayı başlatmak istediğiniz.

**Belge Ziyaretçisi**Yalnızca belirli ziyaretçisi için gerekli yöntemlerin geçersiz kılınması gerektiğinden, yeni belge ziyaretçileri oluşturmayı kolaylaştırmak için VisitXXX yöntemlerinin tümü için varsayılan uygulamalar sağlar. Tüm ziyaretçi yöntemlerini geçersiz kılmak gerekli değildir.

Daha fazla bilgi için Ziyaretçi tasarım modeline bakın.

### Örnekler

Bir belgenin düğüm yapısını yazdırmak için belge ziyaretçisinin nasıl kullanılacağını gösterir.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // Bir belge ziyaretçisini kabul etmek için bir bileşik düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve ardından tüm düğümün alt öğelerini derinlik öncelikli bir şekilde çaprazlar.
    // Ziyaretçi, ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Bir düğümün alt düğümler ağacında çapraz geçiş yapar.
/// Bu ağacın bir dizge biçiminde bir haritasını oluşturur.
/// </summary>
public class DocStructurePrinter : DocumentVisitor
{
    public DocStructurePrinter()
    {
        mAcceptingNodeChildTree = new StringBuilder();
    }

    public string GetText()
    {
        return mAcceptingNodeChildTree.ToString();
    }

    /// <summary>
    /// Bir Belge düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitDocumentStart(Document doc)
    {
        int childNodeCount = doc.GetChildNodes(NodeType.Any, true).Count;

        IndentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
        mDocTraversalDepth++;

        // Ziyaretçinin diğer düğümleri ziyaret etmeye devam etmesine izin ver.
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belge düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Bölüm düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // Belge içindeki bölümümüzün indeksini alın.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir Bölüm düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Gövde düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir Body düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitBodyEnd(Body body)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Body end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Paragraf düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitParagraphStart(Paragraph paragraph)
    {
        IndentAndAppendLine("[Paragraph start]");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Paragraf düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitParagraphEnd(Paragraph paragraph)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Paragraph end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Çalıştırma düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Alt Belge düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitSubDocument(SubDocument subDocument)
    {
        IndentAndAppendLine("[SubDocument]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin belge ağacında ne kadar derin olduğuna bağlı olarak girinti yapın.
    /// </summary>
    /// <param name="metin"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++) mAcceptingNodeChildTree.Append("|  ");

        mAcceptingNodeChildTree.AppendLine(text);
    }

    private int mDocTraversalDepth;
    private readonly StringBuilder mAcceptingNodeChildTree;
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


