---
title: "Метод Aspose::Words::CompositeNode::GetChildNodes"
linktitle: "GetChildNodes"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::CompositeNode::GetChildNodes. Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу, в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words/compositenode/getchildnodes/
---
## CompositeNode::GetChildNodes method


Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::CompositeNode::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Указывает тип узлов для выбора. |
| isDeep | bool | **true** — выбрать из всех дочерних узлов рекурсивно; **false** — выбрать только среди непосредственных дочерних узлов. |

### ReturnValue

Живая коллекция дочерних узлов указанного типа.
## Примечания


Коллекция узлов, возвращаемая этим методом, всегда живая.

Живая коллекция всегда синхронизирована с документом. Например, если вы выбрали все разделы в документе и перебираете коллекцию, удаляя разделы, раздел удаляется из коллекции сразу же, когда он удаляется из документа.

## Примеры



Показывает, как вывести все комментарии документа и их ответы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// Если у комментария нет предка, он считается "верхнего уровня" комментарием, в отличие от комментария-ответа.
// Выведите все комментарии верхнего уровня вместе со всеми их ответами.
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


Показывает, как извлекать изображения из документа и сохранять их в локальную файловую систему как отдельные файлы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Получите коллекцию фигур из документа,
// и сохраните данные изображения каждой фигуры, содержащей изображение, в файл на локальной файловой системе.
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
        // Данные изображений фигур могут содержать изображения во множестве возможных форматов.
        // Мы можем автоматически определить расширение файла для каждого изображения, исходя из его формата.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```


Показывает, как пройтись по коллекции дочерних узлов составного узла.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Добавьте два фрагмента текста и одну фигуру в качестве дочерних узлов к первому абзацу этого документа.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Обратите внимание, что 'CustomNodeId' не сохраняется в выходной файл и существует только в течение жизни узла.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Итерируйтесь по коллекции непосредственных дочерних элементов абзаца,
// и выводите любые фрагменты текста или фигуры, которые мы находим внутри.
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


Показывает, как добавить, обновить и удалить дочерние узлы в коллекции детей [CompositeNode](../)'s.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Пустой документ по умолчанию содержит один абзац.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Составные узлы, такие как наш абзац, могут содержать другие составные и встроенные узлы в качестве дочерних.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// Создайте ещё три узла run.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// Тело документа не будет отображать эти run'ы, пока мы не вставим их в составной узел
// который сам является частью дерева узлов документа, как мы сделали с первым run.
// Мы можем определить, где будет находиться текстовое содержимое узлов, которые мы вставляем
// в документе, указав место вставки относительно другого узла в абзаце.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// Вставьте второй run в абзац перед начальным run.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Вставьте третий run после начального run.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// Вставьте первый run в начало коллекции дочерних узлов абзаца.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Мы можем изменить содержимое run, редактируя и удаляя существующие дочерние узлы.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```

## См. также

* Class [NodeCollection](../../nodecollection/)
* Enum [NodeType](../../nodetype/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
