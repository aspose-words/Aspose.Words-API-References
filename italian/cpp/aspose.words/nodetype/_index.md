---
title: "Aspose::Words::NodeType enum"
linktitle: "NodeType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::NodeType enum. Specifica il tipo di nodo di un documento Word in C++."
type: docs
weight: 102000
url: /it/cpp/aspose.words/nodetype/
---
## NodeType enum


Specifica il tipo di un nodo di documento Word.

```cpp
enum class NodeType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Any | 0 | Indica tutti i tipi di nodo. Consente di selezionare tutti i figli. |
| Document | 1 | Un oggetto [Document](../document/) che, come radice dell'albero del documento, fornisce l'accesso all'intero documento Word. Un nodo [Document](../document/) può contenere nodi [Section](../section/). |
| Section | 2 | Un oggetto [Section](../section/) che corrisponde a una sezione in un documento Word. Un nodo [Section](../section/) può contenere nodi [Body](../body/) e [HeaderFooter](../headerfooter/). |
| Body | 3 | Un oggetto [Body](../body/) che contiene il testo principale di una sezione (storia del testo principale). Un nodo [Body](../body/) può contenere nodi [Paragraph](../paragraph/) e [Table](../../aspose.words.tables/table/). |
| HeaderFooter | 4 | Un oggetto [HeaderFooter](../headerfooter/) che contiene il testo di un'intestazione o di un piè di pagina specifico all'interno di una sezione. Un nodo [HeaderFooter](../headerfooter/) può contenere nodi [Paragraph](../paragraph/) e [Table](../../aspose.words.tables/table/). |
| Table | 5 | Un oggetto [Table](../../aspose.words.tables/table/) che rappresenta una tabella in un documento Word. Un nodo [Table](../../aspose.words.tables/table/) può contenere nodi [Row](../../aspose.words.tables/row/). |
| Row | 6 | Una riga di una tabella. Un nodo [Row](../../aspose.words.tables/row/) può contenere nodi [Cell](../../aspose.words.tables/cell/). |
| Cell | 7 | Una cella di una riga di tabella. Un nodo [Cell](../../aspose.words.tables/cell/) può contenere nodi [Paragraph](../paragraph/) e [Table](../../aspose.words.tables/table/). |
| Paragraph | 8 | Un paragrafo di testo. Un nodo [Paragraph](../paragraph/) è un contenitore per elementi di livello inline [Run](../run/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [Footnote](../../aspose.words.notes/footnote/), [Comment](../comment/), [SpecialChar](../specialchar/), così come [BookmarkStart](../bookmarkstart/) e [BookmarkEnd](../bookmarkend/). |
| BookmarkStart | 9 | Un inizio di un marcatore di segnalibro. |
| BookmarkEnd | 10 | Una fine di un marcatore di segnalibro. |
| EditableRangeStart | 11 | Un inizio di un intervallo modificabile. |
| EditableRangeEnd | 12 | Una fine di un intervallo modificabile. |
| MoveFromRangeStart | 13 | Un inizio di un intervallo MoveFrom. |
| MoveFromRangeEnd | 14 | Una fine di un intervallo MoveFrom. |
| MoveToRangeStart | 15 | Un inizio di un intervallo MoveTo. |
| MoveToRangeEnd | 16 | Una fine di un intervallo MoveTo. |
| GroupShape | 17 | Un gruppo di forme, immagini, oggetti OLE o altre forme di gruppo. Un nodo [GroupShape](../../aspose.words.drawing/groupshape/) può contenere altri nodi [Shape](../../aspose.words.drawing/shape/) e [GroupShape](../../aspose.words.drawing/groupshape/). |
| Shape | 18 | Un oggetto di disegno, come una forma OfficeArt, un'immagine o un oggetto OLE. Un nodo [Shape](../../aspose.words.drawing/shape/) può contenere nodi [Paragraph](../paragraph/) e [Table](../../aspose.words.tables/table/). |
| Comment | 19 | Un commento in un documento Word. Un nodo [Comment](../comment/) può avere nodi [Paragraph](../paragraph/) e [Table](../../aspose.words.tables/table/). |
| Footnote | 20 | Una nota a piè di pagina o una nota finale in un documento Word. Un nodo [Footnote](../../aspose.words.notes/footnote/) può avere nodi [Paragraph](../paragraph/) e [Table](../../aspose.words.tables/table/). |
| Run | 21 | Una sequenza di testo. |
| FieldStart | 22 | Un carattere speciale che indica l'inizio di un campo Word. |
| FieldSeparator | 23 | Un carattere speciale che separa il codice del campo dal risultato del campo. |
| FieldEnd | 24 | Un carattere speciale che indica la fine di un campo Word. |
| FormField | 25 | Un campo modulo. |
| SpecialChar | 26 | Un carattere speciale che non è uno dei tipi di carattere speciale più specifici. |
| SmartTag | 27 | Un tag intelligente attorno a una o più strutture in linea (sequenze, immagini, campi, ecc.) all'interno di un paragrafo. |
| StructuredDocumentTag | 28 | Consente di definire informazioni specifiche per il cliente e il loro modo di presentazione. |
| StructuredDocumentTagRangeStart | 29 | Un inizio di tag di documento strutturato **ranged** che accetta contenuti a più sezioni. |
| StructuredDocumentTagRangeEnd | 30 | Una fine di tag di documento strutturato **ranged** che accetta contenuti a più sezioni. |
| GlossaryDocument | 31 | Un documento di glossario all'interno del documento principale. |
| BuildingBlock | 32 | Un blocco di costruzione all'interno di un documento di glossario (ad es. voce del documento di glossario). |
| CommentRangeStart | 33 | Un nodo marcatore che rappresenta l'inizio di un intervallo commentato. |
| CommentRangeEnd | 34 | Un nodo marcatore che rappresenta la fine di un intervallo commentato. |
| OfficeMath | 35 | Un oggetto Office [Math](../../aspose.words.math/). Può essere un'equazione, una funzione, una matrice o uno degli altri oggetti matematici. Può essere una collezione di oggetti matematici e può anche contenere alcuni oggetti non matematici come sequenze di testo. |
| SubDocument | 36 | Un nodo subdocumento che è un collegamento a un altro documento. |
| System | 37 | Riservato per uso interno da parte di [Aspose.Words](../). |
| Null | 38 | Riservato per uso interno da parte di [Aspose.Words](../). |


## Esempi



Mostra come attraversare la collezione di nodi figlio di un nodo composito.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Aggiungi due run e una shape come nodi figlio al primo paragrafo di questo documento.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Nota che 'CustomNodeId' non viene salvato in un file di output ed esiste solo durante la vita del nodo.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Itera attraverso la collezione di figli immediati del paragrafo,
// e stampa tutti i run o le shape che troviamo al suo interno.
System::SharedPtr<Aspose::Words::NodeCollection> children = paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count());

for (auto&& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
        case Aspose::Words::NodeType::Run:
            std::cout << "Run contents:" << std::endl;
            std::cout << System::String::Format(u"\t\"{0}\"", child->GetText().Trim()) << std::endl;
            break;

        case Aspose::Words::NodeType::Shape:
        {
            auto childShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(child);
            std::cout << "Shape:" << std::endl;
            std::cout << System::String::Format(u"\t{0}, {1}x{2}", childShape->get_ShapeType(), childShape->get_Width(), childShape->get_Height()) << std::endl;
            ASSERT_EQ(100, shape->get_CustomNodeId());
            break;
        }

        default:
            break;
    }
}
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
