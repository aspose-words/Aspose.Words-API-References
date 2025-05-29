---
title: Body Class
linktitle: Body
articleTitle: Body
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Body — ваш основной инструмент для простого управления текстом разделов и повышения эффективности обработки документов.
type: docs
weight: 220
url: /ru/net/aspose.words/body/
---
## Body class

Представляет контейнер для основного текста раздела.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) документальная статья.

```csharp
public class Body : Story
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Body](body/)(*[DocumentBase](../documentbase/)*) | Инициализирует новый экземпляр`Body` класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первый дочерний элемент узла. |
| [FirstParagraph](../../aspose.words/story/firstparagraph/) { get; } | Получает первый абзац в истории. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возврат`истинный` если у этого узла есть дочерние узлы. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возврат`истинный` так как этот узел может иметь дочерние узлы. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [LastParagraph](../../aspose.words/story/lastparagraph/) { get; } | Получает последний абзац в истории. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| override [NodeType](../../aspose.words/body/nodetype/) { get; } | ВозвратBody . |
| [Paragraphs](../../aspose.words/story/paragraphs/) { get; } | Получает коллекцию абзацев, которые являются непосредственными дочерними элементами истории. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentSection](../../aspose.words/body/parentsection/) { get; } | Получает родительский раздел этой истории. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/)объект, представляющий часть документа, содержащуюся в этом узле. |
| [StoryType](../../aspose.words/story/storytype/) { get; } | Получает тип этой истории. |
| [Tables](../../aspose.words/story/tables/) { get; } | Получает коллекцию таблиц, которые являются непосредственными дочерними элементами истории. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/body/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя. |
| override [AcceptEnd](../../aspose.words/body/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя для посещения конца тела документа. |
| override [AcceptStart](../../aspose.words/body/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя для посещения начала тела документа. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Добавляет указанный узел в конец списка дочерних узлов для данного узла. |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(*string*) | Метод быстрого доступа, который создает[`Paragraph`](../paragraph/) объект с необязательным текстом и добавляет его в конец этого объекта. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | Удаляет все фигуры из текста этой истории. |
| [EnsureMinimum](../../aspose.words/body/ensureminimum/)() | Если последний дочерний элемент не является абзацем, создает и добавляет один пустой абзац. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Получает первого предка указанного[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля по дочерним узлам этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних узлов. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Добавляет указанный узел в начало списка дочерних узлов для данного узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Удаляет указанный дочерний узел. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/) узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Выбирает первый[`Node`](../node/) что соответствует выражению XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

## Примечания

`Body` может содержать[`Paragraph`](../paragraph/) и[`Стол`](../../aspose.words.tables/table/) дочерние узлы.

`Body` является узлом уровня раздела и может быть только дочерним узлом[`Section`](../section/) . Может быть только один`Body` в[`Section`](../section/).

Минимально допустимый`Body` должен содержать по крайней мере один[`Paragraph`](../paragraph/).

## Примеры

Показывает, как создать документ Aspose.Words вручную.

```csharp
Document doc = new Document();

// Пустой документ содержит один раздел, одно тело и один абзац.
// Вызываем метод "RemoveAllChildren", чтобы удалить все эти узлы,
// и в итоге получаем узел документа без дочерних элементов.
doc.RemoveAllChildren();

// В этом документе теперь нет составных дочерних узлов, в которые мы можем добавлять контент.
// Если мы хотим его отредактировать, нам нужно будет заново заполнить его коллекцию узлов.
// Сначала создадим новый раздел, а затем добавим его как дочерний элемент к корневому узлу документа.
Section section = new Section(doc);
doc.AppendChild(section);

// Задайте некоторые свойства настройки страницы для раздела.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Разделу необходимо тело, которое будет содержать и отображать все его содержимое
// на странице между верхним и нижним колонтитулами раздела.
Body body = new Body(doc);
section.AppendChild(body);

// Создаем абзац, задаем некоторые свойства форматирования, а затем добавляем его в качестве дочернего элемента к телу.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Наконец, добавьте немного контента для документа. Создайте запуск,
// задаем его внешний вид и содержимое, а затем добавляем его как дочерний элемент к абзацу.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Смотрите также

* class [Story](../story/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
