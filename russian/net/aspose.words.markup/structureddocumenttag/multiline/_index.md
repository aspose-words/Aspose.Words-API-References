---
title: StructuredDocumentTag.Multiline
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTag свойство. Указывает является ли это СДТ позволяет использовать несколько строк текста.
type: docs
weight: 210
url: /ru/net/aspose.words.markup/structureddocumenttag/multiline/
---
## StructuredDocumentTag.Multiline property

Указывает, является ли это **СДТ** позволяет использовать несколько строк текста.

```csharp
public bool Multiline { get; set; }
```

### Примечания

Доступ к этому ресурсу будет работать только дляRichText иPlainText Тип SDT.

Для всех остальных типов SDT возникнет исключение.

### Примеры

Показывает, как создать тег структурированного документа в текстовом поле и изменить его внешний вид.

```csharp
Document doc = new Document();

// Создайте тег структурированного документа, который будет содержать обычный текст.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Установите заголовок и цвет рамки, которая появляется при наведении курсора мыши на тег структурированного документа в Microsoft Word.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Устанавливаем тег для этого тега структурированного документа, который можно получить
// как XML-элемент с именем "tag" со строкой ниже в атрибуте "@val".
tag.Tag = "MyPlainTextSDT";

// Каждый тег структурированного документа имеет случайный уникальный идентификатор.
Assert.That(tag.Id, Is.Positive);

// Установите шрифт для текста внутри тега структурированного документа.
tag.ContentsFont.Name = "Arial";

// Установите шрифт для текста в конце тега структурированного документа.
// Любой текст, который мы вводим в тело документа после перемещения из тега с помощью клавиш со стрелками, будет использовать этот шрифт.
tag.EndCharacterFont.Name = "Arial Black";

// По умолчанию это значение false, и нажатие клавиши Enter внутри тега структурированного документа ничего не делает.
// Если установлено значение true, наш тег структурированного документа может иметь несколько строк.

// Установите для свойства «Многострочный» значение «false», чтобы разрешить только содержимое
// этого тега структурированного документа, занимающего одну строку.
// Установите для свойства «Многострочный» значение «истина», чтобы тег мог содержать несколько строк содержимого.
tag.Multiline = true;

// Установите для свойства «Внешний вид» значение «SdtAppearance.Tags», чтобы отображать теги вокруг контента.
 // По умолчанию тег структурированного документа отображается как BoundingBox.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Вставляем клон нашего тега структурированного документа в новый абзац.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// Используйте метод «RemoveSelfOnly», чтобы удалить тег структурированного документа, сохранив его содержимое в документе.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### Смотрите также

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../structureddocumenttag/)
* сборка [Aspose.Words](../../../)


