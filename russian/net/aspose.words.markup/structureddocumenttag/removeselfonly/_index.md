---
title: StructuredDocumentTag.RemoveSelfOnly
linktitle: RemoveSelfOnly
articleTitle: RemoveSelfOnly
second_title: Aspose.Words для .NET
description: Откройте для себя метод StructuredDocumentTag RemoveSelfOnly, чтобы без усилий удалить узел SDT, сохранив его содержимое в вашем документе. Повысьте эффективность редактирования!
type: docs
weight: 370
url: /ru/net/aspose.words.markup/structureddocumenttag/removeselfonly/
---
## StructuredDocumentTag.RemoveSelfOnly method

Удаляет только сам узел SDT, но сохраняет его содержимое внутри дерева документа.

```csharp
public void RemoveSelfOnly()
```

## Примеры

Показывает, как создать структурированный тег документа в текстовом поле и изменить его внешний вид.

```csharp
Document doc = new Document();

// Создайте структурированный тег документа, который будет содержать простой текст.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Задайте заголовок и цвет рамки, которая появляется при наведении курсора на тег структурированного документа в Microsoft Word.
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// Установите тег для этого структурированного тега документа, который можно получить
// как элемент XML с именем "tag" и указанной ниже строкой в атрибуте "@val".
tag.Tag = "MyPlainTextSDT";

// Каждый структурированный тег документа имеет случайный уникальный идентификатор.
Assert.IsTrue(tag.Id > 0);

// Устанавливаем шрифт для текста внутри структурированного тега документа.
tag.ContentsFont.Name = "Arial";

// Устанавливаем шрифт для текста в конце структурированного тега документа.
// Любой текст, который мы наберем в теле документа после выхода из тега с помощью клавиш со стрелками, будет использовать этот шрифт.
tag.EndCharacterFont.Name = "Arial Black";

// По умолчанию это значение false, и нажатие Enter внутри структурированного тега документа ничего не делает.
// Если установлено значение true, наш структурированный тег документа может иметь несколько строк.

// Установите свойство "Multiline" на "false", чтобы разрешить только содержимое
// этого структурированного тега документа, чтобы он охватывал одну строку.
// Установите свойство «Multiline» в значение «true», чтобы разрешить тегу содержать несколько строк содержимого.
tag.Multiline = true;

// Установите свойство «Внешний вид» на «SdtAppearance.Tags», чтобы отобразить теги вокруг содержимого.
 // По умолчанию структурированный тег документа отображается как BoundingBox.
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// Вставляем клон нашего структурированного тега документа в новый абзац.
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// Используйте метод «RemoveSelfOnly» для удаления структурированного тега документа, сохраняя его содержимое в документе.
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### Смотрите также

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
