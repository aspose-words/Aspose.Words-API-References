---
title: Style.BuiltIn
second_title: Справочник по API Aspose.Words для .NET
description: Style свойство. True если этот стиль является одним из встроенных стилей MS Word.
type: docs
weight: 40
url: /ru/net/aspose.words/style/builtin/
---
## Style.BuiltIn property

True, если этот стиль является одним из встроенных стилей MS Word.

```csharp
public bool BuiltIn { get; }
```

### Примеры

Показывает, как отличить пользовательские стили от встроенных.

```csharp
Document doc = new Document();

// Когда мы создаем документ с помощью Microsoft Word или программно с помощью Aspose.Words,
// документ будет содержать набор стилей, которые можно применить к его тексту и изменить его внешний вид.
// Мы можем получить доступ к этим встроенным стилям через коллекцию «Стили» документа.
// Все эти стили будут иметь флаг «BuiltIn», установленный в значение «true».
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// Создаем собственный стиль и добавляем его в коллекцию.
// Пользовательские стили, подобные этому, будут иметь флаг «BuiltIn», установленный в значение «false».
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### Смотрите также

* class [Style](../)
* пространство имен [Aspose.Words](../../style/)
* сборка [Aspose.Words](../../../)


