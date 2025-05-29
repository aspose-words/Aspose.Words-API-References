---
title: DocumentVisitor Class
linktitle: DocumentVisitor
articleTitle: DocumentVisitor
second_title: .NET için Aspose.Words
description: Belge işleme ve düzenlemesini geliştirmek için özel belge ziyaretçileri oluşturmanıza yardımcı olacak temeliniz olan Aspose.Words.DocumentVisitor sınıfını keşfedin.
type: docs
weight: 690
url: /tr/net/aspose.words/documentvisitor/
---
## DocumentVisitor class

Özel belge ziyaretçileri için temel sınıf.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Aspose.Words Belge Nesne Modeli (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) belgeleme makalesi.

```csharp
public abstract class DocumentVisitor
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| virtual [VisitAbsolutePositionTab](../../aspose.words/documentvisitor/visitabsolutepositiontab/)(*[AbsolutePositionTab](../absolutepositiontab/)*) | Bir çağrı yapıldığında çağrılır[`AbsolutePositionTab`](../absolutepositiontab/) Belgede düğümle karşılaşıldı. |
| virtual [VisitBodyEnd](../../aspose.words/documentvisitor/visitbodyend/)(*[Body](../body/)*) | Bir bölümdeki ana metin hikayesinin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitBodyStart](../../aspose.words/documentvisitor/visitbodystart/)(*[Body](../body/)*) | Bir bölümdeki ana metin hikayesinin numaralandırılması başladığında çağrılır. |
| virtual [VisitBookmarkEnd](../../aspose.words/documentvisitor/visitbookmarkend/)(*[BookmarkEnd](../bookmarkend/)*) | Belgede bir yer iminin sonuna ulaşıldığında çağrılır. |
| virtual [VisitBookmarkStart](../../aspose.words/documentvisitor/visitbookmarkstart/)(*[BookmarkStart](../bookmarkstart/)*) | Belgede bir yer imi başlangıcıyla karşılaşıldığında çağrılır. |
| virtual [VisitBuildingBlockEnd](../../aspose.words/documentvisitor/visitbuildingblockend/)(*[BuildingBlock](../../aspose.words.buildingblocks/buildingblock/)*) | Bir yapı bloğunun numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitBuildingBlockStart](../../aspose.words/documentvisitor/visitbuildingblockstart/)(*[BuildingBlock](../../aspose.words.buildingblocks/buildingblock/)*) | Bir yapı bloğunun numaralandırılması başladığında çağrılır. |
| virtual [VisitCellEnd](../../aspose.words/documentvisitor/visitcellend/)(*[Cell](../../aspose.words.tables/cell/)*) | Bir tablo hücresinin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitCellStart](../../aspose.words/documentvisitor/visitcellstart/)(*[Cell](../../aspose.words.tables/cell/)*) | Bir tablo hücresinin numaralandırılması başladığında çağrılır. |
| virtual [VisitCommentEnd](../../aspose.words/documentvisitor/visitcommentend/)(*[Comment](../comment/)*) | Bir yorum metninin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitCommentRangeEnd](../../aspose.words/documentvisitor/visitcommentrangeend/)(*[CommentRangeEnd](../commentrangeend/)*) | Yorumlanmış bir metin aralığının sonuna gelindiğinde çağrılır. |
| virtual [VisitCommentRangeStart](../../aspose.words/documentvisitor/visitcommentrangestart/)(*[CommentRangeStart](../commentrangestart/)*) | Yorumlanmış bir metin aralığının başlangıcıyla karşılaşıldığında çağrılır. |
| virtual [VisitCommentStart](../../aspose.words/documentvisitor/visitcommentstart/)(*[Comment](../comment/)*) | Bir yorum metninin numaralandırılması başladığında çağrılır. |
| virtual [VisitDocumentEnd](../../aspose.words/documentvisitor/visitdocumentend/)(*[Document](../document/)*) | Belgenin numaralandırılması tamamlandığında çağrılır. |
| virtual [VisitDocumentStart](../../aspose.words/documentvisitor/visitdocumentstart/)(*[Document](../document/)*) | Belgenin numaralandırılması başladığında çağrılır. |
| virtual [VisitEditableRangeEnd](../../aspose.words/documentvisitor/visiteditablerangeend/)(*[EditableRangeEnd](../editablerangeend/)*) | Belgede düzenlenebilir bir aralığın sonuna ulaşıldığında çağrılır. |
| virtual [VisitEditableRangeStart](../../aspose.words/documentvisitor/visiteditablerangestart/)(*[EditableRangeStart](../editablerangestart/)*) | Belgede düzenlenebilir bir aralığın başlangıcıyla karşılaşıldığında çağrılır. |
| virtual [VisitFieldEnd](../../aspose.words/documentvisitor/visitfieldend/)(*[FieldEnd](../../aspose.words.fields/fieldend/)*) | Belgede bir alan sona erdiğinde çağrılır. |
| virtual [VisitFieldSeparator](../../aspose.words/documentvisitor/visitfieldseparator/)(*[FieldSeparator](../../aspose.words.fields/fieldseparator/)*) | Belgede bir alan ayırıcısı ile karşılaşıldığında çağrılır. |
| virtual [VisitFieldStart](../../aspose.words/documentvisitor/visitfieldstart/)(*[FieldStart](../../aspose.words.fields/fieldstart/)*) | Belgede bir alan başladığında çağrılır. |
| virtual [VisitFootnoteEnd](../../aspose.words/documentvisitor/visitfootnoteend/)(*[Footnote](../../aspose.words.notes/footnote/)*) | Dipnot veya sonnot metninin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitFootnoteStart](../../aspose.words/documentvisitor/visitfootnotestart/)(*[Footnote](../../aspose.words.notes/footnote/)*) | Dipnot veya sonnot metninin numaralandırılması başladığında çağrılır. |
| virtual [VisitFormField](../../aspose.words/documentvisitor/visitformfield/)(*[FormField](../../aspose.words.fields/formfield/)*) | Belgede bir form alanıyla karşılaşıldığında çağrılır. |
| virtual [VisitGlossaryDocumentEnd](../../aspose.words/documentvisitor/visitglossarydocumentend/)(*[GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/)*) | Bir sözlük belgesinin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitGlossaryDocumentStart](../../aspose.words/documentvisitor/visitglossarydocumentstart/)(*[GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/)*) | Bir sözlük belgesinin numaralandırılması başladığında çağrılır. |
| virtual [VisitGroupShapeEnd](../../aspose.words/documentvisitor/visitgroupshapeend/)(*[GroupShape](../../aspose.words.drawing/groupshape/)*) | Bir grup şeklinin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitGroupShapeStart](../../aspose.words/documentvisitor/visitgroupshapestart/)(*[GroupShape](../../aspose.words.drawing/groupshape/)*) | Bir grup şeklinin numaralandırılması başladığında çağrılır. |
| virtual [VisitHeaderFooterEnd](../../aspose.words/documentvisitor/visitheaderfooterend/)(*[HeaderFooter](../headerfooter/)*) | Bir bölümdeki başlık veya altbilginin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitHeaderFooterStart](../../aspose.words/documentvisitor/visitheaderfooterstart/)(*[HeaderFooter](../headerfooter/)*) | Bir bölümdeki üstbilgi veya altbilginin numaralandırılması başladığında çağrılır. |
| virtual [VisitOfficeMathEnd](../../aspose.words/documentvisitor/visitofficemathend/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | Bir Office Math nesnesinin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitOfficeMathStart](../../aspose.words/documentvisitor/visitofficemathstart/)(*[OfficeMath](../../aspose.words.math/officemath/)*) | Bir Office Math nesnesinin numaralandırılması başladığında çağrılır. |
| virtual [VisitParagraphEnd](../../aspose.words/documentvisitor/visitparagraphend/)(*[Paragraph](../paragraph/)*) | Bir paragrafın numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitParagraphStart](../../aspose.words/documentvisitor/visitparagraphstart/)(*[Paragraph](../paragraph/)*) | Bir paragrafın numaralandırılması başladığında çağrılır. |
| virtual [VisitRowEnd](../../aspose.words/documentvisitor/visitrowend/)(*[Row](../../aspose.words.tables/row/)*) | Bir tablo satırının numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitRowStart](../../aspose.words/documentvisitor/visitrowstart/)(*[Row](../../aspose.words.tables/row/)*) | Bir tablo satırının numaralandırılması başladığında çağrılır. |
| virtual [VisitRun](../../aspose.words/documentvisitor/visitrun/)(*[Run](../run/)*) | Bir metin çalışmasıyla karşılaşıldığında çağrılır. |
| virtual [VisitSectionEnd](../../aspose.words/documentvisitor/visitsectionend/)(*[Section](../section/)*) | Bir bölümün numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitSectionStart](../../aspose.words/documentvisitor/visitsectionstart/)(*[Section](../section/)*) | Bir bölümün numaralandırılması başladığında çağrılır. |
| virtual [VisitShapeEnd](../../aspose.words/documentvisitor/visitshapeend/)(*[Shape](../../aspose.words.drawing/shape/)*) | Bir şeklin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitShapeStart](../../aspose.words/documentvisitor/visitshapestart/)(*[Shape](../../aspose.words.drawing/shape/)*) | Bir şeklin numaralandırılması başladığında çağrılır. |
| virtual [VisitSmartTagEnd](../../aspose.words/documentvisitor/visitsmarttagend/)(*[SmartTag](../../aspose.words.markup/smarttag/)*) | Akıllı etiketin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitSmartTagStart](../../aspose.words/documentvisitor/visitsmarttagstart/)(*[SmartTag](../../aspose.words.markup/smarttag/)*) | Akıllı etiketin numaralandırılması başladığında çağrılır. |
| virtual [VisitSpecialChar](../../aspose.words/documentvisitor/visitspecialchar/)(*[SpecialChar](../specialchar/)*) | Bir çağrı yapıldığında çağrılır[`SpecialChar`](../specialchar/) Belgede düğümle karşılaşıldı. |
| virtual [VisitStructuredDocumentTagEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagend/)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/)*) | Yapılandırılmış bir belge etiketinin numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitStructuredDocumentTagRangeEnd](../../aspose.words/documentvisitor/visitstructureddocumenttagrangeend/)(*[StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/)*) | StructuredDocumentTagRangeEnd ile karşılaşıldığında çağrılır. |
| virtual [VisitStructuredDocumentTagRangeStart](../../aspose.words/documentvisitor/visitstructureddocumenttagrangestart/)(*[StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/)*) | StructuredDocumentTagRangeStart ile karşılaşıldığında çağrılır. |
| virtual [VisitStructuredDocumentTagStart](../../aspose.words/documentvisitor/visitstructureddocumenttagstart/)(*[StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/)*) | Yapılandırılmış bir belge etiketinin numaralandırılması başladığında çağrılır. |
| virtual [VisitSubDocument](../../aspose.words/documentvisitor/visitsubdocument/)(*[SubDocument](../subdocument/)*) | Bir alt belgeyle karşılaşıldığında çağrılır. |
| virtual [VisitTableEnd](../../aspose.words/documentvisitor/visittableend/)(*[Table](../../aspose.words.tables/table/)*) | Bir tablonun numaralandırılması sona erdiğinde çağrılır. |
| virtual [VisitTableStart](../../aspose.words/documentvisitor/visittablestart/)(*[Table](../../aspose.words.tables/table/)*) | Bir tablonun numaralandırılması başladığında çağrılır. |

## Notlar

İle`DocumentVisitor` Belge ağacı üzerinde numaralandırma gerektiren özel operations tanımlayabilir ve çalıştırabilirsiniz.

Örneğin, Aspose.Words şunu kullanır:`DocumentVisitor` dahili olarak tasarruf için[`Document`](../document/) çeşitli biçimlerde ve alan veya yer imleri bulma gibi diğer işlemler için bir belge parçası üzerinde .

Kullanmak için`DocumentVisitor`:

1. Türetilmiş bir sınıf oluşturun`DocumentVisitor`.
2. Bazı veya tüm VisitXXX yöntemleri için uygulamaları geçersiz kılın ve sağlayın ve bazı özel işlemleri gerçekleştirin.
3. Arama[`Düğüm.Kabul Et`](../node/accept/) üzerinde[`Node`](../node/) sayımı başlatmak istediğiniz .

`DocumentVisitor` tüm VisitXXX yöntemleri için varsayılan uygulamalar sağlar, böylece yalnızca belirli ziyaretçisi için gereken yöntemlerin geçersiz kılınması gerektiğinden yeni belge ziyaretçileri oluşturmayı kolaylaştırır. Tüm ziyaretçi yöntemlerini geçersiz kılmak gerekli değildir.

Daha fazla bilgi için Ziyaretçi tasarım desenine bakın.

## Örnekler

Bir belgenin düğüm yapısını yazdırmak için belge ziyaretçisinin nasıl kullanılacağını gösterir.

```csharp
public void DocStructureToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    DocStructurePrinter visitor = new DocStructurePrinter();

    // Bir belge ziyaretçisini kabul etmek için bir bileşik düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve sonra düğümün tüm çocuklarını derinlemesine bir şekilde dolaşır.
    // Ziyaretçi ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Bir düğümün alt düğümlerinin ağacını dolaşır.
/// Bu ağacın bir haritasını dize biçiminde oluşturur.
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
    /// Bir Belge düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitDocumentEnd(Document doc)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Document end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Section düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitSectionStart(Section section)
    {
        // Belge içerisindeki bölümümüzün dizinini al.
        NodeCollection docSections = section.Document.GetChildNodes(NodeType.Section, false);
        int sectionIndex = docSections.IndexOf(section);

        IndentAndAppendLine("[Section start] Section index: " + sectionIndex);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir Section düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitSectionEnd(Section section)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Section end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Body düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitBodyStart(Body body)
    {
        int paragraphCount = body.Paragraphs.Count;
        IndentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir Gövde düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
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
    /// Bir Paragraf düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
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
    /// Belgede bir Alt Belge düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
    {
        IndentAndAppendLine("[SdtRangeStart]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Alt Belge düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
    {
        IndentAndAppendLine("[SdtRangeEnd]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin belge ağacında ne kadar derine indiğine bağlı olarak girintisini ayarlayın.
    /// </summary>
    /// <param adı="metin"></param>
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
