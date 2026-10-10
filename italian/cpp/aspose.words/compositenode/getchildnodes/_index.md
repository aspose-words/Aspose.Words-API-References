---
title: "Metodo Aspose::Words::CompositeNode::GetChildNodes"
linktitle: "GetChildNodes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::CompositeNode::GetChildNodes. Restituisce una collezione live di nodi figlio che corrispondono al tipo specificato in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words/compositenode/getchildnodes/
---
## CompositeNode::GetChildNodes method


Restituisce una collezione dinamica di nodi figlio che corrispondono al tipo specificato.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::CompositeNode::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Specifica il tipo di nodi da selezionare. |
| isDeep | bool | **true** per selezionare tutti i nodi figlio ricorsivamente; **false** per selezionare solo tra i figli immediati. |

### ReturnValue

Una collezione live di nodi figlio del tipo specificato.
## Note


La collezione di nodi restituita da questo metodo è sempre live.

Una collezione live è sempre sincronizzata con il documento. Ad esempio, se selezioni tutte le sezioni in un documento e le enumeri attraverso la collezione eliminando le sezioni, la sezione viene rimossa dalla collezione immediatamente quando viene rimossa dal documento.

## Esempi



Mostra come stampare tutti i commenti di un documento e le loro risposte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// Se un commento non ha antenati, è un commento di "livello superiore" rispetto a un commento di tipo risposta.
// Stampa tutti i commenti di livello superiore insieme a eventuali risposte associate.
for (auto&& comment : comments->LINQ_OfType<System::SharedPtr<Aspose::Words::Comment> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Comment>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Comment> c)>>([](System::SharedPtr<Aspose::Words::Comment> c) -> bool
{
    return c->get_Ancestor() == nullptr;
})))->LINQ_ToList())
{
    std::cout << "Top-level comment:" << std::endl;
    std::cout << System::String::Format(u"\t\"{0}\", by {1}", comment->GetText().Trim(), comment->get_Author()) << std::endl;
    std::cout << System::String::Format(u"Has {0} replies", comment->get_Replies()->get_Count()) << std::endl;
    for (auto&& commentReply : System::IterateOver<Aspose::Words::Comment>(comment->get_Replies()))
    {
        std::cout << System::String::Format(u"\t\"{0}\", by {1}", commentReply->GetText().Trim(), commentReply->get_Author()) << std::endl;
    }
    std::cout << std::endl;
}
```


Mostra come estrarre le immagini da un documento e salvarle nel file system locale come file individuali.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Ottieni la raccolta di forme dal documento,
// e salva i dati dell'immagine di ogni forma contenente un'immagine come file nel file system locale.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> s)>>([](System::SharedPtr<Aspose::Words::Node> s) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Drawing::Shape>(s))->get_HasImage();
}))));

int32_t imageIndex = 0;
for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        // I dati dell'immagine delle forme possono contenere immagini in molti formati possibili.
        // Possiamo determinare automaticamente un'estensione file per ogni immagine, in base al suo formato.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```


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


Mostra come aggiungere, aggiornare ed eliminare nodi figlio nella collezione di figli di un [CompositeNode](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento vuoto, per impostazione predefinita, ha un paragrafo.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// I nodi compositi, come il nostro paragrafo, possono contenere altri nodi compositi e inline come figli.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// Crea altri tre nodi run.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// Il corpo del documento non visualizzerà questi run finché non li inseriamo in un nodo composito
// che è esso stesso parte dell'albero dei nodi del documento, come abbiamo fatto con il primo run.
// Possiamo determinare dove il contenuto testuale dei nodi che inseriamo
// appare nel documento specificando una posizione di inserimento relativa a un altro nodo nel paragrafo.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// Inserisci il secondo run nel paragrafo davanti al run iniziale.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Inserisci il terzo run dopo il run iniziale.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// Inserisci il primo run all'inizio della collezione di nodi figlio del paragrafo.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Possiamo modificare il contenuto del run modificando ed eliminando i nodi figlio esistenti.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```

## Vedi anche

* Class [NodeCollection](../../nodecollection/)
* Enum [NodeType](../../nodetype/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
