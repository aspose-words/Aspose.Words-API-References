---
title: Section Class
linktitle: Section
articleTitle: Section
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Section, ваш ключ к управлению отдельными разделами документа без усилий. Улучшите свой опыт редактирования документов сегодня!
type: docs
weight: 6560
url: /ru/net/aspose.words/section/
---
## Section class

Представляет один раздел в документе.

Чтобы узнать больше, посетите[Работа с разделами](https://docs.aspose.com/words/net/working-with-sections/) документальная статья.

```csharp
public sealed class Section : CompositeNode
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Section](section/)(*[DocumentBase](../documentbase/)*) | Инициализирует новый экземпляр класса Section. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | Возвращает[`Body`](../body/) дочерний узел раздела . |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первый дочерний элемент узла. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возврат`истинный` если у этого узла есть дочерние узлы. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | Предоставляет доступ к узлам верхних и нижних колонтитулов раздела. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возврат`истинный` так как этот узел может иметь дочерние узлы. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | ВозвратSection . |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | Возвращает объект, представляющий настройки страницы и свойства раздела. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | True, если раздел защищен для форм. Когда раздел защищен для форм, пользователи могут выбирать и изменять текст только в полях форм в Microsoft Word. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/)объект, представляющий часть документа, содержащуюся в этом узле. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя. |
| override [AcceptEnd](../../aspose.words/section/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) |  |
| override [AcceptStart](../../aspose.words/section/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Добавляет указанный узел в конец списка дочерних узлов для данного узла. |
| [AppendContent](../../aspose.words/section/appendcontent/)(*Section*) | Вставляет копию содержимого исходного раздела в конец данного раздела. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | Очищает раздел. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/#clearheadersfooters)() | Очищает верхние и нижние колонтитулы этого раздела. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/#clearheadersfooters_1)(*bool*) | Очищает верхние и нижние колонтитулы этого раздела. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | Создает дубликат этого раздела. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | Удаляет все фигуры (объекты рисования) из верхних и нижних колонтитулов этого раздела. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | Гарантирует, что раздел имеет[`Body`](./body/) с одним[`Paragraph`](../paragraph/) . |
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
| [PrependContent](../../aspose.words/section/prependcontent/)(*Section*) | Вставляет копию содержимого исходного раздела в начало этого раздела. |
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

`Section` может иметь один[`Body`](../body/) и максимум один[`HeaderFooter`](../headerfooter/) каждого[`HeaderFooterType`](../headerfootertype/) .[`Body`](../body/) и[`HeaderFooter`](../headerfooter/) nodes могут располагаться в любом порядке внутри`Section`.

Минимально допустимый раздел должен иметь[`Body`](../body/) с одним[`Paragraph`](../paragraph/).

Каждый раздел имеет свой собственный набор свойств, которые определяют размер страницы, ориентацию, поля и т. д.

Вы можете создать копию раздела, используя[`Clone`](../node/clone/). Копию можно вставить в тот же или другой документ.

Чтобы добавить, вставить или удалить целый раздел, включая разрыв раздела и свойства раздела , используйте методы[`Sections`](../document/sections/) объект.

Чтобы скопировать и вставить только содержимое раздела, за исключением раздела break и свойств раздела, используйте[`AppendContent`](./appendcontent/) и[`PrependContent`](./prependcontent/) методы.

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

* class [CompositeNode](../compositenode/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
