---
title: Class Section
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Section сорт. Представляет один раздел в документе.
type: docs
weight: 5730
url: /ru/net/aspose.words/section/
---
## Section class

Представляет один раздел в документе.

Чтобы узнать больше, посетите[Работа с разделами](https://docs.aspose.com/words/net/working-with-sections/) статья документации.

```csharp
public sealed class Section : CompositeNode
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Section](section/)(DocumentBase) | Инициализирует новый экземпляр класса Раздел. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | Возвращает[`Body`](../body/) дочерний узел раздела. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных дочерних элементов этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, которому принадлежит этот узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первого дочернего элемента узла. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возвращает`истинный` если у этого узла есть дочерние узлы. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | Обеспечивает доступ к узлам верхнего и нижнего колонтитула раздела. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возвращает`истинный` поскольку этот узел может иметь дочерние узлы. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последнего дочернего узла узла. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | ВозвращаетSection . |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | Возвращает объект, который представляет настройки страницы и свойства раздела. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | True, если раздел защищен для форм. Если раздел защищен для форм, пользователи могут выбирать и изменять текст только в полях формы в Microsoft Word. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/) объект, представляющий часть документа, содержащуюся в этом узле. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(DocumentVisitor) | Принимает посетителя. |
| override [AcceptEnd](../../aspose.words/section/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/section/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendContent](../../aspose.words/section/appendcontent/)(Section) | Вставляет копию содержимого исходного раздела в конец этого раздела. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | Очищает раздел. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/)() | Очищает верхние и нижние колонтитулы этого раздела. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | Создает дубликат этого раздела. |
| [Clone](../../aspose.words/node/clone/)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | Удаляет все фигуры (объекты рисования) из верхних и нижних колонтитулов этого раздела. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | Гарантирует, что в разделе есть[`Body`](./body/) с одним[`Paragraph`](../paragraph/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних элементов. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PrependContent](../../aspose.words/section/prependcontent/)(Section) | Вставляет копию содержимого исходного раздела в начало этого раздела. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя от родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/)узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Выбирает первый[`Node`](../node/) которое соответствует выражению XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

`Section` можно иметь один[`Body`](../body/) и максимум один[`HeaderFooter`](../headerfooter/) каждого[`HeaderFooterType`](../headerfootertype/) .[`Body`](../body/) и[`HeaderFooter`](../headerfooter/) nodes может быть внутри в любом порядке`Section`.

Минимальный допустимый раздел должен иметь[`Body`](../body/) с одним[`Paragraph`](../paragraph/).

Каждый раздел имеет свой собственный набор свойств, которые определяют размер страницы, ориентацию, поля и т. д.

Вы можете создать копию раздела, используя[`Clone`](../node/clone/). Копию можно вставить в тот же или другой документ.

Чтобы добавить, вставить или удалить целый раздел, включая разрыв раздела и свойства раздела , используйте методы класса[`Sections`](../document/sections/) объект.

Чтобы скопировать и вставить только содержимое раздела, исключая раздел Break и свойства раздела, используйте[`AppendContent`](./appendcontent/) и[`PrependContent`](./prependcontent/) методы.

### Примеры

Показывает, как вручную создать документ Aspose.Words.

```csharp
Document doc = new Document();

// Пустой документ содержит один раздел, одно тело и один абзац.
// Вызов метода «RemoveAllChildren», чтобы удалить все эти узлы,
// и в итоге получим узел документа без дочерних элементов.
doc.RemoveAllChildren();

// В этом документе теперь нет составных дочерних узлов, к которым мы можем добавлять контент.
// Если мы хотим его отредактировать, нам нужно будет заново заполнить его коллекцию узлов.
// Сначала создаем новый раздел, а затем добавляем его как дочерний к корневому узлу документа.
Section section = new Section(doc);
doc.AppendChild(section);

// Установите некоторые свойства настройки страницы для раздела.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Разделу необходимо тело, которое будет содержать и отображать все его содержимое
// на странице между заголовком и подвалом раздела.
Body body = new Body(doc);
section.AppendChild(body);

// Создайте абзац, установите некоторые свойства форматирования, а затем добавьте его как дочерний элемент к телу.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Наконец, добавим некоторый контент для оформления документа. Создать пробег,
// устанавливаем его внешний вид и содержимое, а затем добавляем его в качестве дочернего элемента к абзацу.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Смотрите также

* class [CompositeNode](../compositenode/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


