---
title: Class Paragraph
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Paragraph сорт. Представляет абзац текста.
type: docs
weight: 4390
url: /ru/net/aspose.words/paragraph/
---
## Paragraph class

Представляет абзац текста.

Чтобы узнать больше, посетите[Работа с абзацами](https://docs.aspose.com/words/net/working-with-paragraphs/) статья документации.

```csharp
public class Paragraph : CompositeNode
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Paragraph](paragraph/)(DocumentBase) | Инициализирует новый экземпляр`Paragraph` класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator/) { get; } | True, если этот разрыв абзаца является разделителем стилей. Разделитель стилей позволяет абзацу one состоять из частей, имеющих разные стили абзаца. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных дочерних элементов этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, которому принадлежит этот узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первого дочернего элемента узла. |
| [FrameFormat](../../aspose.words/paragraph/frameformat/) { get; } | Обеспечивает доступ к свойствам форматирования фрейма. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возвращает`истинный` если у этого узла есть дочерние узлы. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возвращает`истинный` поскольку этот узел может иметь дочерние узлы. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision/) { get; } | Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell/) { get; } | True, если этот абзац является последним абзацем в[`Cell`](../../aspose.words.tables/cell/) ; ложь в противном случае. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument/) { get; } | True, если этот абзац является последним абзацем в последнем разделе документа. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter/) { get; } | True, если этот абзац является последним абзацем в[`HeaderFooter`](../headerfooter/) (основной текстовый рассказ)[`Section`](../section/) ; ложь в противном случае. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection/) { get; } | True, если этот абзац является последним абзацем в[`Body`](../body/) (основной текстовый рассказ)[`Section`](../section/) ; ложь в противном случае. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision/) { get; } | Возвращает true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений. |
| [IsInCell](../../aspose.words/paragraph/isincell/) { get; } | True, если этот абзац является непосредственным дочерним элементом[`Cell`](../../aspose.words.tables/cell/) ; ложь в противном случае. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision/) { get; } | Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsListItem](../../aspose.words/paragraph/islistitem/) { get; } | Истинно, если абзац является элементом маркированного или нумерованного списка в исходной версии. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision/) { get; } | Возвращает`истинный` если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision/) { get; } | Возвращает`истинный` если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последнего дочернего узла узла. |
| [ListFormat](../../aspose.words/paragraph/listformat/) { get; } | Предоставляет доступ к свойствам форматирования списка абзаца. |
| [ListLabel](../../aspose.words/paragraph/listlabel/) { get; } | Получает[`ListLabel`](./listlabel/)объект, предоставляющий доступ к значению нумерации списка и форматированию для этого абзаца. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words/paragraph/nodetype/) { get; } | ВозвращаетParagraph . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont/) { get; } | Предоставляет доступ к форматированию шрифта символа разрыва абзаца. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat/) { get; } | Предоставляет доступ к свойствам форматирования абзаца. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentSection](../../aspose.words/paragraph/parentsection/) { get; } | Получает родительский элемент[`Section`](../section/) абзаца. |
| [ParentStory](../../aspose.words/paragraph/parentstory/) { get; } | Извлекает историю на уровне родительского раздела, которую можно[`Body`](../body/) или[`HeaderFooter`](../headerfooter/) . |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/) объект, представляющий часть документа, содержащуюся в этом узле. |
| [Runs](../../aspose.words/paragraph/runs/) { get; } | Предоставляет доступ к набору фрагментов текста внутри абзаца. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept/)(DocumentVisitor) | Принимает посетителя. |
| override [AcceptEnd](../../aspose.words/paragraph/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words/paragraph/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_1)(string) | Добавляет поле к этому абзацу. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield)(FieldType, bool) | Добавляет поле к этому абзацу. |
| [AppendField](../../aspose.words/paragraph/appendfield/#appendfield_2)(string, string) | Добавляет поле к этому абзацу. |
| [Clone](../../aspose.words/node/clone/)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops/)() | Возвращает массив всех позиций табуляции, примененных к этому абзацу, в том числе примененных косвенно с помощью стилей или списков. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| override [GetText](../../aspose.words/paragraph/gettext/)() | Получает текст этого абзаца, включая символ конца абзаца. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_1)(string, Node, bool) | Вставляет поле в этот абзац. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield)(FieldType, bool, Node, bool) | Вставляет поле в этот абзац. |
| [InsertField](../../aspose.words/paragraph/insertfield/#insertfield_2)(string, string, Node, bool) | Вставляет поле в этот абзац. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting/)() | Объединяет прогоны с тем же форматированием в абзаце. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
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

`Paragraph` является узлом уровня блока и может быть дочерним классом, производным от [`Story`](../story/) или[`InlineStory`](../inlinestory/).

`Paragraph` может содержать любое количество узлов и закладок встроенного уровня.

Полный список дочерних узлов, которые могут встречаться внутри абзаца, состоит из .[`BookmarkStart`](../bookmarkstart/) ,[`BookmarkEnd`](../bookmarkend/) , [`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) , [`FieldEnd`](../../aspose.words.fields/fieldend/) ,[`FormField`](../../aspose.words.fields/formfield/) , [`Comment`](../comment/) ,[`Footnote`](../../aspose.words.notes/footnote/) , [`Run`](../run/) ,[`SpecialChar`](../specialchar/) , [`Shape`](../../aspose.words.drawing/shape/) ,[`GroupShape`](../../aspose.words.drawing/groupshape/) , [`SmartTag`](../../aspose.words.markup/smarttag/).

Действительный абзац в Microsoft Word всегда заканчивается символом разрыва абзаца, а минимальный допустимый абзац состоит только из разрыва абзаца.`Paragraph` Класс автоматически добавляет соответствующий символ разрыва абзаца в конец , и этот символ не является частью дочерних узлов класса.`Paragraph` , следовательно а`Paragraph` может быть пустым.

Не включайте конец абзаца[`ParagraphBreak`](../controlchar/paragraphbreak/) или конец ячейки[`Cell`](../controlchar/cell/) символы внутри текста абзаца, так как это может сделать абзац недействительным при открытии документа в Microsoft Word.

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


