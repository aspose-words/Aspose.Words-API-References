---
title: Paragraph Class
linktitle: Paragraph
articleTitle: Paragraph
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Paragraph, который поможет вам легко управлять абзацами текста и форматировать их, расширяя возможности обработки документов.
type: docs
weight: 5120
url: /ru/net/aspose.words/paragraph/
---
## Paragraph class

Представляет абзац текста.

Чтобы узнать больше, посетите[Работа с абзацами](https://docs.aspose.com/words/net/working-with-paragraphs/) документальная статья.

```csharp
public class Paragraph : CompositeNode
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Paragraph](paragraph/)(*[DocumentBase](../documentbase/)*) | Инициализирует новый экземпляр`Paragraph` класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | True, если этот разрыв абзаца является разделителем стилей. Разделитель стилей позволяет одному абзацу состоять из частей, имеющих разные стили абзацев. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первый дочерний элемент узла. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | Предоставляет доступ к свойствам форматирования фрейма. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возврат`истинный` если у этого узла есть дочерние узлы. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возврат`истинный` так как этот узел может иметь дочерние узлы. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | Возвращает значение true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | Истина, если этот абзац является последним абзацем в[`Cell`](../../aspose.words.tables/cell/) ; в противном случае ложно. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | Истина, если этот абзац является последним абзацем в последнем разделе документа. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | Истина, если этот абзац является последним абзацем в[`HeaderFooter`](../headerfooter/) (основной текст рассказа)[`Section`](../section/) ; в противном случае ложно. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | Истина, если этот абзац является последним абзацем в[`Body`](../body/) (основной текст рассказа)[`Section`](../section/) ; в противном случае ложно. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | Возвращает значение true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | Истина, если этот абзац является непосредственным потомком[`Cell`](../../aspose.words.tables/cell/) ; в противном случае ложно. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | Возвращает значение true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | Истинно, если абзац является элементом маркированного или нумерованного списка в исходной редакции. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | Возврат`истинный` если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | Возврат`истинный` если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | Предоставляет доступ к свойствам форматирования списка абзаца. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | Получает[`ListLabel`](./listlabel/)объект, который обеспечивает доступ к значению нумерации списка и форматированию для этого абзаца. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | ВозвратParagraph . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | Предоставляет доступ к форматированию шрифта символа разрыва абзаца. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | Предоставляет доступ к свойствам форматирования абзаца. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | Возвращает родителя[`Section`](../section/) абзаца. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | Извлекает историю уровня родительского раздела, которая может быть[`Body`](../body/) или[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/)объект, представляющий часть документа, содержащуюся в этом узле. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | Предоставляет доступ к набору фрагментов текста внутри абзаца. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя. |
| override [AcceptEnd](../../aspose.words/paragraph/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя для посещения конца абзаца документа. |
| override [AcceptStart](../../aspose.words/paragraph/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя для посещения начала абзаца документа. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Добавляет указанный узел в конец списка дочерних узлов для данного узла. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(*string*) | Добавляет поле к этому абзацу. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool*) | Добавляет поле к этому абзацу. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(*string, string*) | Добавляет поле к этому абзацу. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Получает первого предка указанного[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | Возвращает массив всех позиций табуляции, примененных к данному абзацу, включая примененные косвенно стилями или списками. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля по дочерним узлам этого узла. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | Получает текст этого абзаца, включая символ конца абзаца. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(*string, [Node](../node/), bool*) | Вставляет поле в этот абзац. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(*[FieldType](../../aspose.words.fields/fieldtype/), bool, [Node](../node/), bool*) | Вставляет поле в этот абзац. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(*string, string, [Node](../node/), bool*) | Вставляет поле в этот абзац. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | Объединяет фрагменты с одинаковым форматированием в абзаце. |
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

`Paragraph` является узлом блочного уровня и может быть дочерним классом производных от [`Story`](../story/) или[`InlineStory`](../inlinestory/).

`Paragraph` может содержать любое количество встроенных узлов и закладок.

Полный список дочерних узлов, которые могут встречаться внутри абзаца, состоит из [`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) , [`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../run/) ,[`SpecialChar`](../specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`SmartTag`](../../aspose.words.markup/smarttag/).

Допустимый абзац в Microsoft Word всегда заканчивается символом разрыва абзаца и минимальный допустимый абзац состоит только из символа разрыва абзаца.`Paragraph` Класс автоматически добавляет соответствующий символ разрыва абзаца в конец , и этот символ не является частью дочерних узлов`Paragraph` , поэтому а`Paragraph` может быть пустым.

Не включайте конец абзаца.[`ParagraphBreak`](../controlchar/paragraphbreak/) или конец ячейки[`Cell`](../controlchar/cell/) символы внутри текста абзаца, так как это может сделать абзац недействительным при открытии документа в Microsoft Word.

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
