---
title: "Aspose::Words::CompositeNode::GetChildNodes Methode"
linktitle: "GetChildNodes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::CompositeNode::GetChildNodes-Methode. Gibt eine Live‑Sammlung von Kindknoten zurück, die dem angegebenen Typ entsprechen, in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words/compositenode/getchildnodes/
---
## CompositeNode::GetChildNodes method


Gibt eine Live-Sammlung von Kindknoten zurück, die dem angegebenen Typ entsprechen.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::CompositeNode::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Gibt den Typ der auszuwählenden Knoten an. |
| isDeep | bool | **true** zum Auswählen aller Kindknoten rekursiv; **false** zum Auswählen nur der unmittelbaren Kinder. |

### ReturnValue

Eine Live‑Sammlung von Kindknoten des angegebenen Typs.
## Hinweise


Die von dieser Methode zurückgegebene Knotensammlung ist stets live.

Eine Live‑Sammlung ist stets mit dem Dokument synchronisiert. Zum Beispiel, wenn Sie alle Abschnitte in einem Dokument auswählen und die Sammlung durchlaufen, um die Abschnitte zu löschen, wird der Abschnitt sofort aus der Sammlung entfernt, sobald er aus dem Dokument entfernt wird.

## Beispiele



Zeigt, wie man alle Kommentare eines Dokuments und deren Antworten ausgibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// Hat ein Kommentar keinen Vorgänger, ist er ein „Top‑Level“-Kommentar im Gegensatz zu einem Antwort‑Kommentar.
// Gibt alle Top‑Level‑Kommentare zusammen mit allen möglichen Antworten aus.
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


Zeigt, wie Bilder aus einem Dokument extrahiert und als einzelne Dateien im lokalen Dateisystem gespeichert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Holen Sie die Sammlung von Formen aus dem Dokument,
// und speichern Sie die Bilddaten jeder Form, die ein Bild enthält, als Datei im lokalen Dateisystem.
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
        // Die Bilddaten von Formen können Bilder in vielen möglichen Bildformaten enthalten.
        // Wir können für jedes Bild automatisch eine Dateierweiterung basierend auf seinem Format bestimmen.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```


Zeigt, wie man durch die Sammlung von Kindknoten eines Composite-Knotens traversiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Füge zwei Runs und eine Form als Kindknoten zum ersten Absatz dieses Dokuments hinzu.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Beachten Sie, dass die 'CustomNodeId' nicht in einer Ausgabedatei gespeichert wird und nur während der Lebensdauer des Knotens existiert.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Iterieren Sie durch die Sammlung unmittelbarer Kinder des Absatzes,
// und geben Sie alle Runs oder Shapes aus, die wir darin finden.
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


Zeigt, wie man Kindknoten in der Sammlung von Kindern eines [CompositeNode](../) hinzufügt, aktualisiert und löscht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ein leeres Dokument enthält standardmäßig einen Absatz.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Composite‑Knoten wie unser Absatz können andere Composite‑ und Inline‑Knoten als Kinder enthalten.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// Erstelle drei weitere Run‑Knoten.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// Der Dokumentkörper zeigt diese Runs nicht an, bis wir sie in einen Composite‑Knoten einfügen
// der selbst Teil des Knotensystems des Dokuments ist, wie wir es beim ersten Run getan haben.
// Wir können bestimmen, wo der Textinhalt von Knoten, die wir einfügen,
// im Dokument erscheint, indem wir einen Einfügeort relativ zu einem anderen Knoten im Absatz angeben.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// Füge den zweiten Run in den Absatz vor dem initialen Run ein.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Füge den dritten Run nach dem initialen Run ein.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// Füge den ersten Run am Anfang der Kindknoten‑Sammlung des Absatzes ein.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Wir können den Inhalt des Runs ändern, indem wir vorhandene Kindknoten bearbeiten und löschen.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```

## Siehe auch

* Class [NodeCollection](../../nodecollection/)
* Enum [NodeType](../../nodetype/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
