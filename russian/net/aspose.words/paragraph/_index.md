---
title: Paragraph
second_title: Справочник по API Aspose.Words для .NET
description: Представляет абзац текста.
type: docs
weight: 4100
url: /ru/net/aspose.words/paragraph/
---
## Paragraph class

Представляет абзац текста.

```csharp
public class Paragraph : CompositeNode
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Paragraph](paragraph)(DocumentBase) | Инициализирует новый экземпляр класса **Paragraph** . |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator) { get; } | Истинно, если этот разрыв абзаца является разделителем стилей. Разделитель стилей позволяет одному абзацу состоять из частей с разными стилями абзаца. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Получает все непосредственные дочерние узлы данного узла. |
| [Count](../../aspose.words/compositenode/count) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Указывает идентификатор пользовательского узла. |
| virtual [Document](../../aspose.words/node/document) { get; } | Получает документ, которому принадлежит данный узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Получает первый потомок узла. |
| [FrameFormat](../../aspose.words/paragraph/frameformat) { get; } | Предоставляет доступ к свойствам форматирования абзаца. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Возвращает true, если у этого узла есть дочерние узлы. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision) { get; } | Возвращает true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell) { get; } | Истинно, если этот абзац является последним абзацем в[`Cell`](../../aspose.words.tables/cell); ложно в противном случае. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument) { get; } | Истинно, если этот абзац является последним абзацем в последнем разделе документа. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter) { get; } | Истинно, если этот абзац является последним абзацем в **HeaderFooter** (основной текст) статьи **Раздел** ; ложно в противном случае. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection) { get; } | Истинно, если этот абзац является последним абзацем в **Body** (основной текст) статьи **Раздел** ; ложно в противном случае. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision) { get; } | Возвращает true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений. |
| [IsInCell](../../aspose.words/paragraph/isincell) { get; } | Истинно, если этот абзац является непосредственным потомком[`Cell`](../../aspose.words.tables/cell); ложно в противном случае. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision) { get; } | Возвращает true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsListItem](../../aspose.words/paragraph/islistitem) { get; } | Истинно, если абзац является элементом маркированного или нумерованного списка в исходной редакции. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision) { get; } | Возвращает **true** , если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision) { get; } | Возвращает **true** , если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Получает последний потомок узла. |
| [ListFormat](../../aspose.words/paragraph/listformat) { get; } | Предоставляет доступ к свойствам форматирования списка абзаца. |
| [ListLabel](../../aspose.words/paragraph/listlabel) { get; } | Получает объект[`ListLabel`](./listlabel), предоставляющий доступ к значению нумерации и форматированию списка для этого абзаца. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words/paragraph/nodetype) { get; } | Возвращает **NodeType.Paragraph** . |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont) { get; } | Предоставляет доступ к форматированию шрифта символа разрыва абзаца. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat) { get; } | Предоставляет доступ к свойствам форматирования абзаца. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Получает непосредственного родителя этого узла. |
| [ParentSection](../../aspose.words/paragraph/parentsection) { get; } | Извлекает родителя[`Section`](../section)абзаца. |
| [ParentStory](../../aspose.words/paragraph/parentstory) { get; } | Извлекает историю уровня родительского раздела, которая может быть[`Body`](../body)или[`HeaderFooter`](../headerfooter). |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range) { get; } | Возвращает объект **Range** , представляющий часть документа, содержащуюся в этом узле. |
| [Runs](../../aspose.words/paragraph/runs) { get; } | Предоставляет доступ к типизированному набору фрагментов текста внутри абзаца. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept)(DocumentVisitor) | Принимает посетителя. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [AppendField](../../aspose.words/paragraph/appendfield#appendfield_1)(string) | Добавляет поле к этому абзацу. |
| [AppendField](../../aspose.words/paragraph/appendfield#appendfield)(FieldType, bool) | Добавляет поле к этому абзацу. |
| [AppendField](../../aspose.words/paragraph/appendfield#appendfield_2)(string, string) | Добавляет поле к этому абзацу. |
| [Clone](../../aspose.words/node/clone)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Зарезервировано для системного использования. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Получает первого предка указанного[`NodeType`](../nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Возвращает динамическую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops)() | Возвращает массив всех позиций табуляции, примененных к этому абзацу, в том числе примененных косвенно стилями или списками. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| override [GetText](../../aspose.words/paragraph/gettext)() | Получает текст этого абзаца, включая символ конца абзаца. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Вставляет указанный узел сразу после указанного опорного узла. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [InsertField](../../aspose.words/paragraph/insertfield#insertfield_1)(string, Node, bool) | Вставляет поле в этот абзац. |
| [InsertField](../../aspose.words/paragraph/insertfield#insertfield)(FieldType, bool, Node, bool) | Вставляет поле в этот абзац. |
| [InsertField](../../aspose.words/paragraph/insertfield#insertfield_2)(string, string, Node, bool) | Вставляет поле в этот абзац. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting)() | Соединения выполняются с одинаковым форматированием в абзаце. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Добавляет указанный узел в начало списка дочерних узлов для этого узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Удаляет указанный дочерний узел. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag)узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Выбирает первый узел, соответствующий выражению XPath. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

[`Paragraph`](../paragraph)блок- level node и может быть потомком классов, производных от [`Story`](../story)или[`InlineStory`](../inlinestory).

[`Paragraph`](../paragraph)может содержать любое количество узлов и закладок встроенного уровня.

Полный список дочерних узлов, которые могут встречаться внутри абзаца, состоит из [`BookmarkStart`](../bookmarkstart),[`BookmarkEnd`](../bookmarkend), [`FieldStart`](../../aspose.words.fields/fieldstart),[`FieldSeparator`](../../aspose.words.fields/fieldseparator), [`FieldEnd`](../../aspose.words.fields/fieldend),[`FormField`](../../aspose.words.fields/formfield), [`Comment`](../comment),[`Footnote`](../../aspose.words.notes/footnote), [`Run`](../run),[`SpecialChar`](../specialchar), [`Shape`](../../aspose.words.drawing/shape),[`GroupShape`](../../aspose.words.drawing/groupshape), [`SmartTag`](../../aspose.words.markup/smarttag).

Действительный абзац в Microsoft Word всегда заканчивается символом разрыва абзаца, а минимальный допустимый абзац состоит только из разрыва абзаца. Класс **Paragraph** автоматически добавляет соответствующий символ разрыва абзаца в конце и этот символ не является частью дочерние узлы абзаца , поэтому a **абзаца** могут быть пустым.

Не включать конец абзаца[`ControlChar.ParagraphBreak`](../controlchar/paragraphbreak) или конец ячейки[`ControlChar.Cell`](../controlchar/cell) символов внутри текста абзац, так как это может сделать абзац недействительным при открытии документа в Microsoft Word.

### Примеры

Показывает, как создать документ Aspose.Words вручную.

```csharp
Document doc = new Document();

 // Пустой документ содержит один раздел, одно тело и один абзац.
 // Вызовите метод "RemoveAllChildren", чтобы удалить все эти узлы, 
 // и получаем узел документа без дочерних элементов.
doc.RemoveAllChildren();

 // У этого документа теперь нет составных дочерних узлов, к которым мы можем добавить содержимое.
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

 // Создаем абзац, устанавливаем некоторые свойства форматирования, а затем добавляем его как дочерний элемент к телу.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

 // Наконец, добавьте содержимое для создания документа. Создайте прогон, 
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
