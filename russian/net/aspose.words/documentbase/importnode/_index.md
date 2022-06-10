---
title: ImportNode
second_title: Справочник по API Aspose.Words для .NET
description: Импортирует узел из другого документа в текущий документ.
type: docs
weight: 100
url: /ru/net/aspose.words/documentbase/importnode/
---
## ImportNode(Node, bool) {#importnode}

Импортирует узел из другого документа в текущий документ.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcNode | Node | Импортируемый узел. |
| isImportChildren | Boolean | True для рекурсивного импорта всех дочерних узлов; в противном случае ложно. |

### Возвращаемое значение

Клонированный узел, принадлежащий текущему документу.

### Примечания

Этот метод используетUseDestinationStylesвозможность разрешить форматирование.

При импорте узла создается копия исходного узла, принадлежащая импортирующему документу. Возвращенный узел не имеет родителя. Исходный узел не изменяется и не удаляется из исходного документа.

Прежде чем узел из другого документа можно будет вставить в этот документ, его необходимо импортировать. Во время импорта специфичные для документа свойства, такие как ссылки на стили и списки, переводятся из оригинала в импортируемый документ. После импорта узла его можно вставить в соответствующее место документа с помощьюУзел)или [`InsertAfter`](../../compositenode/insertafter).

Если исходный узел уже принадлежит целевому документу, то создается просто глубокий клон исходного узла.

### Примеры

Показывает, как импортировать узел из одного документа в другой.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// У каждого узла есть родительский документ, который является документом, содержащим узел.
// Вставка узла в документ, которому этот узел не принадлежит, вызовет исключение.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => { dstDoc.AppendChild(srcDoc.FirstSection); });

// Используйте метод ImportNode для создания копии узла, в котором будет документ
// который вызвал метод ImportNode, установленный в качестве его нового документа-владельца.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true);

Assert.AreEqual(dstDoc, importedSection.Document);

// Теперь мы можем вставить узел в документ.
dstDoc.AppendChild(importedSection);

Assert.AreEqual("Destination document first paragraph text.\r\nSource document first paragraph text.\r\n",
    dstDoc.ToString(SaveFormat.Text));
```

### Смотрите также

* class [Node](../../node)
* class [DocumentBase](../../documentbase)
* пространство имен [Aspose.Words](../../documentbase)
* сборка [Aspose.Words](../../../)

---

## ImportNode(Node, bool, ImportFormatMode) {#importnode_1}

Импорт узла из другого документа в текущий документ с возможностью управления форматированием.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcNode | Node | Импортируемый узел. |
| isImportChildren | Boolean | True для рекурсивного импорта всех дочерних узлов; в противном случае ложно. |
| importFormatMode | ImportFormatMode | Указывает, как объединить конфликтующее форматирование стилей. |

### Возвращаемое значение

Клонированный импортированный узел. Узел принадлежит целевому документу, но не имеет родителя.

### Примечания

Эта перегрузка полезна для управления импортом стилей и форматирования списка.

При импорте узла создается копия исходного узла, принадлежащая импортирующему документу. Возвращенный узел не имеет родителя. Исходный узел не изменяется и не удаляется из исходного документа.

Прежде чем узел из другого документа можно будет вставить в этот документ, его необходимо импортировать. Во время импорта специфичные для документа свойства, такие как ссылки на стили и списки, переводятся из оригинала в импортируемый документ. После импорта узла его можно вставить в соответствующее место документа с помощьюУзел)или [`InsertAfter`](../../compositenode/insertafter).

Если исходный узел уже принадлежит целевому документу, то создается просто глубокий клон исходного узла.

### Примеры

Показывает, как импортировать узел из исходного документа в целевой документ с определенными параметрами.

```csharp
// Создадим два документа и добавим стиль символа в каждый документ.
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

// Импорт раздела из целевого документа в исходный документ, вызывая конфликт имен стилей.
// Если мы используем конечные стили, то импортированный исходный текст с тем же именем стиля
// поскольку текст назначения примет стиль назначения.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// Если мы используем ImportFormatMode.KeepDifferentStyles, исходный стиль сохраняется,
// и конфликт имен разрешается добавлением суффикса.
dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.KeepDifferentStyles);
Assert.AreEqual(dstStyle.Font.Name, dstDoc.Styles["My style"].Font.Name);
Assert.AreEqual(srcStyle.Font.Name, dstDoc.Styles["My style_0"].Font.Name);
```

### Смотрите также

* class [Node](../../node)
* enum [ImportFormatMode](../../importformatmode)
* class [DocumentBase](../../documentbase)
* пространство имен [Aspose.Words](../../documentbase)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
