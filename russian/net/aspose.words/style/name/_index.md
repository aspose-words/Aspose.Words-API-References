---
title: Style.Name
second_title: Справочник по API Aspose.Words для .NET
description: Style свойство. Получает или задает имя стиля.
type: docs
weight: 130
url: /ru/net/aspose.words/style/name/
---
## Style.Name property

Получает или задает имя стиля.

```csharp
public string Name { get; set; }
```

### Примечания

Не может быть пустой строки.

Если в коллекции уже есть стиль с таким именем, то этот стиль его переопределит. Все затронутые узлы будут ссылаться на новый стиль.

### Примеры

Показывает, как получить доступ к коллекции стилей документа.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Перечисляем и перечисляем все стили, которые по умолчанию содержит документ, созданный с помощью Aspose.Words.
using (IEnumerator<Style> stylesEnum = doc.Styles.GetEnumerator())
{
    while (stylesEnum.MoveNext())
    {
        Style curStyle = stylesEnum.Current;
        Console.WriteLine($"Style name:\t\"{curStyle.Name}\", of type \"{curStyle.Type}\"");
        Console.WriteLine($"\tSubsequent style:\t{curStyle.NextParagraphStyleName}");
        Console.WriteLine($"\tIs heading:\t\t\t{curStyle.IsHeading}");
        Console.WriteLine($"\tIs QuickStyle:\t\t{curStyle.IsQuickStyle}");

        Assert.AreEqual(doc, curStyle.Document);
    }
}
```

Показывает, как клонировать стиль документа.

```csharp
Document doc = new Document();

// Метод AddCopy создает копию указанного стиля и
// автоматически генерирует новое имя для стиля, например «Заголовок 1_0».
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

// Используйте свойство «Name» стиля, чтобы изменить идентифицирующее имя стиля.
newStyle.Name = "My Heading 1";

// Наш документ теперь имеет два одинаково выглядящих стиля с разными именами.
// Изменение настроек одного из стилей не влияет на другой.
newStyle.Font.Color = Color.Red;

Assert.AreEqual("My Heading 1", newStyle.Name);
Assert.AreEqual("Heading 1", doc.Styles["Heading 1"].Name);

Assert.AreEqual(doc.Styles["Heading 1"].Type, newStyle.Type);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Name, newStyle.Font.Name);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Size, newStyle.Font.Size);
Assert.AreNotEqual(doc.Styles["Heading 1"].Font.Color, newStyle.Font.Color);
```

### Смотрите также

* class [Style](../)
* пространство имен [Aspose.Words](../../style/)
* сборка [Aspose.Words](../../../)


