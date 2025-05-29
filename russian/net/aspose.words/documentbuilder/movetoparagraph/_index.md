---
title: DocumentBuilder.MoveToParagraph
linktitle: MoveToParagraph
articleTitle: MoveToParagraph
second_title: Aspose.Words для .NET
description: Легко перемещайтесь по документу с помощью метода MoveToParagraph в DocumentBuilder, позволяющего быстро перемещать курсор к любому абзацу в разделе.
type: docs
weight: 600
url: /ru/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

Перемещает курсор на абзац в текущем разделе.

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| paragraphIndex | Int32 | Индекс абзаца, к которому необходимо перейти. |
| characterIndex | Int32 | Индекс символа внутри абзаца. Отрицательное значение позволяет указать позицию от конца абзаца. Используйте -1 для перемещения в конец абзаца. |

## Примечания

Навигация осуществляется внутри текущей истории текущего раздела. То есть, если вы переместили курсор на основной заголовок первого раздела, то*paragraphIndex* указал индекс абзаца внутри header этого раздела.

Когда*paragraphIndex* больше или равно 0, он указывает индекс from начала раздела, где 0 — первый абзац. Когда*paragraphIndex* меньше 0, , то указан индекс с конца раздела, где -1 соответствует последнему абзацу.

## Примеры

Показывает, как переместить курсор конструктора на указанный абзац.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Создаем конструктор документов для редактирования документа. Курсор конструктора,
// это точка, в которую он вставит новые узлы, когда мы вызываем его методы построения документа,
// в настоящее время находится в начале документа.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// Перемещение курсора на другой абзац поместит курсор перед этим абзацем.
builder.MoveToParagraph(2, 0);
// Любой новый контент, который мы добавим, будет вставлен в эту точку.
builder.Writeln("This is a new third paragraph. ");
```

### Смотрите также

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
