---
title: DocumentBuilder.MoveToParagraph
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Перемещает курсор на абзац текущего раздела.
type: docs
weight: 570
url: /ru/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

Перемещает курсор на абзац текущего раздела.

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| paragraphIndex | Int32 | Индекс абзаца, к которому необходимо перейти. |
| characterIndex | Int32 | Индекс символа внутри абзаца. Отрицательное значение позволяет указать позицию от конца абзаца. Используйте -1, чтобы перейти к концу абзаца. |

### Примечания

Навигация осуществляется внутри текущей истории текущего раздела. То есть, если вы переместили курсор на основной заголовок первого раздела, , то*paragraphIndex*указал индекс абзаца внутри header этого раздела.

Когда*paragraphIndex* больше или равно 0, он указывает индекс from начала раздела, где 0 соответствует первому абзацу. Когда*paragraphIndex* меньше 0, указан индекс с конца раздела, где -1 является последним абзацем.

### Примеры

Показывает, как переместить позицию курсора построителя в указанный абзац.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Создаем построитель документов для редактирования документа. Курсор строителя,
// это точка, в которой он будет вставлять новые узлы, когда мы вызываем его методы построения документа,
// сейчас находится в начале документа.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// Перемещение этого курсора в другой абзац поместит этот курсор перед этим абзацем.
builder.MoveToParagraph(2, 0);
// Любой новый контент, который мы добавляем, будет вставлен в этот момент.
builder.Writeln("This is a new third paragraph. ");
```

### Смотрите также

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


