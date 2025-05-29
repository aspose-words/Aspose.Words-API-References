---
title: CleanupOptions.UnusedStyles
linktitle: UnusedStyles
articleTitle: UnusedStyles
second_title: Aspose.Words для .NET
description: Оптимизируйте свои документы с помощью свойства UnusedStyles в CleanupOptions, гарантируя удаление неиспользуемых стилей для более чистого и быстро загружаемого контента. Значение по умолчанию — true.
type: docs
weight: 50
url: /ru/net/aspose.words/cleanupoptions/unusedstyles/
---
## CleanupOptions.UnusedStyles property

Указывает, следует ли удалять неиспользуемые стили из документа. Значение по умолчанию:`истинный` .

```csharp
public bool UnusedStyles { get; set; }
```

## Примеры

Показывает, как удалить все неиспользуемые пользовательские стили из документа.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// В сочетании со встроенными стилями документ теперь имеет восемь стилей.
// Пользовательский стиль помечается как «используемый», пока в документе есть какой-либо текст
// отформатировано в этом стиле. Это означает, что 4 добавленных нами стиля в настоящее время не используются.
Assert.AreEqual(8, doc.Styles.Count);

// Применить пользовательский стиль символов, а затем пользовательский стиль списка. Это пометит их как «используемые».
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Теперь есть один неиспользуемый стиль символа и один неиспользуемый стиль списка.
// Метод Cleanup(), настроенный с помощью объекта CleanupOptions, может определять неиспользуемые стили и удалять их.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // Удаление каждого узла, к которому применен пользовательский стиль, снова помечает его как «неиспользуемый».
// Повторно запустите метод очистки, чтобы удалить их.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### Смотрите также

* class [CleanupOptions](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
