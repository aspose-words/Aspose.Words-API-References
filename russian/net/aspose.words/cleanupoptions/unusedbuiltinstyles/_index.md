---
title: CleanupOptions.UnusedBuiltinStyles
linktitle: UnusedBuiltinStyles
articleTitle: UnusedBuiltinStyles
second_title: Aspose.Words для .NET
description: CleanupOptions UnusedBuiltinStyles свойство. Указывает что не используетсяBuiltIn стили следует удалить из document на С#.
type: docs
weight: 30
url: /ru/net/aspose.words/cleanupoptions/unusedbuiltinstyles/
---
## CleanupOptions.UnusedBuiltinStyles property

Указывает, что не используется[`BuiltIn`](../../style/builtin/) стили следует удалить из document.

```csharp
public bool UnusedBuiltinStyles { get; set; }
```

## Примеры

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

* class [CleanupOptions](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
