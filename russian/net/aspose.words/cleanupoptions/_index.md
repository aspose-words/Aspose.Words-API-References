---
title: Class CleanupOptions
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.CleanupOptions сорт. Позволяет указать параметры очистки документа.
type: docs
weight: 210
url: /ru/net/aspose.words/cleanupoptions/
---
## CleanupOptions class

Позволяет указать параметры очистки документа.

Чтобы узнать больше, посетите[Очистить документ](https://docs.aspose.com/words/net/clean-up-a-document/) статья документации.

```csharp
public class CleanupOptions
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [CleanupOptions](cleanupoptions/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DuplicateStyle](../../aspose.words/cleanupoptions/duplicatestyle/) { get; set; } | Получает/устанавливает флаг, указывающий, следует ли удалять повторяющиеся стили из документа. Значение по умолчанию:`ЛОЖЬ` . |
| [UnusedBuiltinStyles](../../aspose.words/cleanupoptions/unusedbuiltinstyles/) { get; set; } | Указывает, что не используется[`BuiltIn`](../style/builtin/) стили следует удалить из document. |
| [UnusedLists](../../aspose.words/cleanupoptions/unusedlists/) { get; set; } | Указывает, следует ли удалять из документа неиспользуемый список и определения списков. Значение по умолчанию:`истинный` . |
| [UnusedStyles](../../aspose.words/cleanupoptions/unusedstyles/) { get; set; } | Указывает, следует ли удалять неиспользуемые стили из документа. Значение по умолчанию:`истинный` . |

### Примеры

Показывает, как удалить из документа все неиспользуемые пользовательские стили.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// В сочетании со встроенными стилями документ теперь имеет восемь стилей.
// Пользовательский стиль помечается как «использованный», пока в документе есть какой-либо текст
// отформатировано в этом стиле. Это означает, что 4 добавленных нами стиля в настоящее время не используются.
Assert.AreEqual(8, doc.Styles.Count);

// Применяем пользовательский стиль символов, а затем пользовательский стиль списка. При этом они будут помечены как «использованные».
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Теперь есть один неиспользуемый стиль символов и один неиспользуемый стиль списка.
// Метод Cleanup(), настроенный с помощью объекта CleanupOptions, может нацеливаться на неиспользуемые стили и удалять их.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // Удаление каждого узла, к которому применен пользовательский стиль, снова помечает его как «неиспользуемый».
// Повторно запускаем метод очистки, чтобы удалить их.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


