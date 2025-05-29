---
title: DocumentBase.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words для .NET
description: Легко импортируйте узлы из других документов, чтобы улучшить свой рабочий процесс с помощью метода ImportNode DocumentBase. Оптимизируйте управление документами сегодня!
type: docs
weight: 110
url: /ru/net/aspose.words/documentbase/importnode/
---
## ImportNode(*[Node](../../node/), bool*) {#importnode}

Импортирует узел из другого документа в текущий документ.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcNode | Node | Импортируемый узел. |
| isImportChildren | Boolean | `истинный` для рекурсивного импорта всех дочерних узлов; в противном случае,`ЛОЖЬ`. |

### Возвращаемое значение

Клонированный узел, принадлежащий текущему документу.

## Примечания

Этот метод используетUseDestinationStyles возможность разрешить форматирование.

Импорт узла создает копию исходного узла, принадлежащего импортирующему документу. Возвращенный узел не имеет родителя. Исходный узел не изменяется и не удаляется из исходного документа.

Прежде чем узел из другого документа может быть вставлен в этот документ, он должен быть импортирован. Во время импорта специфические для документа свойства, такие как ссылки на стили и списки, транслируются из исходного в импортирующий документ. После импорта узла его можно вставить в соответствующее место в документе с помощью[`InsertBefore`](../../compositenode/insertbefore/) или [`InsertAfter`](../../compositenode/insertafter/).

Если исходный узел уже принадлежит целевому документу, то просто создается глубокий клон исходного узла.

## Примеры

Показывает, как импортировать узел из одного документа в другой.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// У каждого узла есть родительский документ, который является документом, содержащим узел.
// Вставка узла в документ, к которому узел не принадлежит, вызовет исключение.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => dstDoc.AppendChild(srcDoc.FirstSection));

// Используйте метод ImportNode для создания копии узла, в которой будет находиться документ
// который вызвал метод ImportNode, установленный в качестве его нового владельца document.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true);

Assert.AreEqual(dstDoc, importedSection.Document);

// Теперь мы можем вставить узел в документ.
dstDoc.AppendChild(importedSection);

Assert.AreEqual("Destination document first paragraph text.\r\nSource document first paragraph text.\r\n",
    dstDoc.ToString(SaveFormat.Text));
```

### Смотрите также

* class [Node](../../node/)
* class [DocumentBase](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## ImportNode(*[Node](../../node/), bool, [ImportFormatMode](../../importformatmode/)*) {#importnode_1}

Импортирует узел из другого документа в текущий документ с возможностью управления форматированием.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcNode | Node | Узел для импорта. |
| isImportChildren | Boolean | `истинный` для рекурсивного импорта всех дочерних узлов; в противном случае,`ЛОЖЬ`. |
| importFormatMode | ImportFormatMode | Указывает, как объединить конфликтующие стили форматирования. |

### Возвращаемое значение

Клонированный импортированный узел. Узел принадлежит целевому документу, но не имеет родителя.

## Примечания

Эта перегрузка полезна для управления импортом стилей и форматирования списков.

Импорт узла создает копию исходного узла, принадлежащего импортирующему документу. Возвращенный узел не имеет родителя. Исходный узел не изменяется и не удаляется из исходного документа.

Прежде чем узел из другого документа может быть вставлен в этот документ, он должен быть импортирован. Во время импорта специфические для документа свойства, такие как ссылки на стили и списки, транслируются из исходного в импортирующий документ. После импорта узла его можно вставить в соответствующее место в документе с помощью[`InsertBefore`](../../compositenode/insertbefore/) или [`InsertAfter`](../../compositenode/insertafter/).

Если исходный узел уже принадлежит целевому документу, то просто создается глубокий клон исходного узла.

## Примеры

Показывает, как импортировать узел из исходного документа в целевой документ с определенными параметрами.

```csharp
// Создайте два документа и добавьте стиль символа в каждый документ.
// Настройте стили так, чтобы они имели одинаковое имя, но разное форматирование текста.
Document srcDoc = new Document();
Style srcStyle = srcDoc.Styles.Add(StyleType.Character, "My style");
srcStyle.Font.Name = "Courier New";
DocumentBuilder srcBuilder = new DocumentBuilder(srcDoc);
srcBuilder.Font.Style = srcStyle;
srcBuilder.Writeln("Source document text.");

Document dstDoc = new Document();
Style dstStyle = dstDoc.Styles.Add(StyleType.Character, "My style");
dstStyle.Font.Name = "Calibri";
DocumentBuilder dstBuilder = new DocumentBuilder(dstDoc);
dstBuilder.Font.Style = dstStyle;
dstBuilder.Writeln("Destination document text.");

// Импортируем раздел из целевого документа в исходный документ, что приводит к конфликту имен стилей.
// Если мы используем целевые стили, то импортируемый исходный текст с тем же именем стиля
// в качестве конечного текста будет принят конечный стиль.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// Если мы используем ImportFormatMode.KeepDifferentStyles, исходный стиль сохраняется,
// и конфликт имен разрешается путем добавления суффикса.
dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.KeepDifferentStyles);
Assert.AreEqual(dstStyle.Font.Name, dstDoc.Styles["My style"].Font.Name);
Assert.AreEqual(srcStyle.Font.Name, dstDoc.Styles["My style_0"].Font.Name);
```

### Смотрите также

* class [Node](../../node/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBase](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
