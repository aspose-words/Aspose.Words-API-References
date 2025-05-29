---
title: Run Class
linktitle: Run
articleTitle: Run
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Run — мощный класс для управления последовательностями символов с единообразным форматированием шрифтов, повышающий эффективность обработки документов.
type: docs
weight: 5560
url: /ru/net/aspose.words/run/
---
## Run class

Представляет серию символов с одинаковым форматированием шрифта.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) документальная статья.

```csharp
public class Run : Inline
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Run](run/#constructor)(*[DocumentBase](../documentbase/)*) | Инициализирует новый экземпляр`Run` класс. |
| [Run](run/#constructor_1)(*[DocumentBase](../documentbase/), string*) | Инициализирует новый экземпляр**Бегать** класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| [Font](../../aspose.words/inline/font/) { get; } | Предоставляет доступ к форматированию шрифта этого объекта. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Возврат`истинный` если этот узел может содержать другие узлы. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Возвращает значение true, если этот объект был удален в Microsoft Word при включенном отслеживании изменений. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Возвращает значение true, если форматирование объекта было изменено в Microsoft Word при включенном отслеживании изменений. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Возвращает значение true, если этот объект был вставлен в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Возврат`истинный` если этот объект был перемещен (удален) в Microsoft Word при включенном отслеживании изменений. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Возврат`истинный` если этот объект был перемещен (вставлен) в Microsoft Word при включенном отслеживании изменений. |
| [IsPhoneticGuide](../../aspose.words/run/isphoneticguide/) { get; } | Возвращает логическое значение, указывающее, является ли прогон фонетическим руководством. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| override [NodeType](../../aspose.words/run/nodetype/) { get; } | ВозвратRun . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Возвращает родителя[`Paragraph`](../paragraph/) этого узла. |
| [PhoneticGuide](../../aspose.words/run/phoneticguide/) { get; } | Получает[`PhoneticGuide`](./phoneticguide/) объект. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../range/)объект, представляющий часть документа, содержащуюся в этом узле. |
| [Text](../../aspose.words/run/text/) { get; set; } | Получает или задает текст запуска. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words/run/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Принимает посетителя. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Получает первого предка указанного[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| override [GetText](../../aspose.words/run/gettext/)() | Получает текст запуска. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родителя. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

## Примечания

Весь текст документа хранится в виде фрагментов.

`Run` может быть только ребенком[`Paragraph`](../paragraph/) или встроенный[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/).

## Примеры

Показывает, как отформатировать фрагмент текста, используя его свойство шрифта.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

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

Показывает, как добавлять, обновлять и удалять дочерние узлы в коллекции дочерних узлов CompositeNode.

```csharp
Document doc = new Document();

// Пустой документ по умолчанию имеет один абзац.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Составные узлы, такие как наш абзац, могут содержать другие составные и встроенные узлы в качестве дочерних.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Создаем еще три узла запуска.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Тело документа не будет отображать эти прогоны, пока мы не вставим их в составной узел
// который сам по себе является частью дерева узлов документа, как мы это делали при первом запуске.
// Мы можем определить, где находится текстовое содержимое узлов, которые мы вставляем
// появляется в документе, указывая место вставки относительно другого узла в абзаце.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Вставьте вторую строку в абзац перед первой строкой.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Вставьте третий запуск после первого запуска.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Вставляем первую строку в начало коллекции дочерних узлов абзаца.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Мы можем изменить содержимое прогона, редактируя и удаляя существующие дочерние узлы.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Смотрите также

* class [Inline](../inline/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
