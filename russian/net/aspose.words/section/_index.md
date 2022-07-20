---
title: Section
second_title: Справочник по API Aspose.Words для .NET
description: Представляет один раздел в документе.
type: docs
weight: 5440
url: /ru/net/aspose.words/section/
---
## Section class

Представляет один раздел в документе.

```csharp
public sealed class Section : CompositeNode
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Section](section)(DocumentBase) | Инициализирует новый экземпляр класса Section. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Body](../../aspose.words/section/body) { get; } | Возвращает **Тело** дочерний узел раздела. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Получает все непосредственные дочерние узлы этого узла. |
| [Count](../../aspose.words/compositenode/count) { get; } | Получает количество непосредственных дочерних элементов этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Указывает идентификатор пользовательского узла. |
| virtual [Document](../../aspose.words/node/document) { get; } | Получает документ, которому принадлежит этот узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Получает первого потомка узла. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Возвращает true, если у этого узла есть дочерние узлы. |
| [HeadersFooters](../../aspose.words/section/headersfooters) { get; } | Предоставляет доступ к верхним и нижним колонтитулам раздела. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Получает последний дочерний элемент узла. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words/section/nodetype) { get; } | Возвращает **NodeType.Section** . |
| [PageSetup](../../aspose.words/section/pagesetup) { get; } | Возвращает объект, представляющий настройки страницы и свойства раздела. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms) { get; set; } | Истинно, если раздел защищен для форм. Когда раздел защищен для форм, пользователи могут выбирать и изменять текст только в полях формы в Microsoft Word. |
| [Range](../../aspose.words/node/range) { get; } | Возвращает **Диапазон** объект, представляющий часть документа, содержащегося в этом узле. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/section/accept)(DocumentVisitor) | Принимает посетителя. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [AppendContent](../../aspose.words/section/appendcontent)(Section) | Вставляет копию содержимого исходного раздела в конец этого раздела. |
| [ClearContent](../../aspose.words/section/clearcontent)() | Очищает раздел. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters)() | Очищает верхние и нижние колонтитулы этого раздела. |
| [Clone](../../aspose.words/section/clone#clone_1)() | Создает дубликат этого раздела. |
| [Clone](../../aspose.words/node/clone)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Зарезервировано для системного использования. IXPathNavigable. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes)() | Удаляет все фигуры (объекты рисования) из верхних и нижних колонтитулов этого раздела. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum)() | Гарантирует, что раздел имеет тело с одним абзацем. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Возвращает динамическую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Получает текст этого узла и всех его дочерних элементов. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Добавляет указанный узел в начало списка дочерних узлов для этого узла. |
| [PrependContent](../../aspose.words/section/prependcontent)(Section) | Вставляет копию содержимого исходного раздела в начало этого раздела. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Удаляет указанный дочерний узел. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag) узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Выбирает первый узел, соответствующий выражению XPath. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

**Раздел** может иметь один[`Body`](./body) и максимум один[`HeaderFooter`](../headerfooter) каждого[`HeaderFooterType`](../headerfootertype) . **Тело** а также **Верхний колонтитул** nodes может быть в любом порядке внутри **Раздел**.

Минимальный действительный раздел должен иметь **Тело** с одним **Параграф**.

Каждый раздел имеет собственный набор свойств, определяющих размер страницы, ориентацию, поля и т. д.

Вы можете создать копию раздела, используя[`Clone`](../node/clone). Копия может быть вставлена в тот же или другой документ.

Чтобы добавить, вставить или удалить весь раздел, включая разрыв раздела и свойства раздела , используйте методы класса **Разделы** объект.

Чтобы скопировать и вставить только содержимое раздела, исключая раздел break и свойства раздела, используйте **AppendContent** а также **PrependContent**методы.

### Примеры

Показывает, как создать документ Aspose.Words вручную.

```csharp
Document doc = new Document();

// Пустой документ содержит один раздел, одно тело и один абзац.
// Вызовите метод "RemoveAllChildren", чтобы удалить все эти узлы,
// и получаем узел документа без дочерних элементов.
doc.RemoveAllChildren();

// Этот документ теперь не имеет составных дочерних узлов, к которым мы можем добавить содержимое.
// Если мы хотим отредактировать его, нам нужно будет повторно заполнить его коллекцию узлов.
// Сначала создайте новый раздел, а затем добавьте его как дочерний к корневому узлу документа.
Section section = new Section(doc);
doc.AppendChild(section);

// Установите некоторые свойства настройки страницы для раздела.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Разделу нужно тело, которое будет содержать и отображать все его содержимое
// на странице между шапкой и нижним колонтитулом раздела.
Body body = new Body(doc);
section.AppendChild(body);

// Создать абзац, установить некоторые свойства форматирования, а затем добавить его в тело как дочерний элемент.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Наконец, добавьте содержимое для создания документа. Создать прогон,
// установить его внешний вид и содержимое, а затем добавить его как дочерний элемент к абзацу.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Смотрите также

* class [CompositeNode](../compositenode)
* пространство имен [Aspose.Words](../../aspose.words)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
