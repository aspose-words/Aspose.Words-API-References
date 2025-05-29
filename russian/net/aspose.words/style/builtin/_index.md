---
title: Style.BuiltIn
linktitle: BuiltIn
articleTitle: BuiltIn
second_title: Aspose.Words для .NET
description: Узнайте, является ли стиль встроенной опцией в MS Word. Улучшите дизайн вашего документа с помощью нашего всеобъемлющего руководства по встроенным стилям Word!
type: docs
weight: 40
url: /ru/net/aspose.words/style/builtin/
---
## Style.BuiltIn property

Истина, если этот стиль является одним из встроенных стилей в MS Word.

```csharp
public bool BuiltIn { get; }
```

## Примеры

Показывает, как отличить пользовательские стили от встроенных.

```csharp
Document doc = new Document();

// Когда мы создаем документ с помощью Microsoft Word или программно с помощью Aspose.Words,
// документ будет содержать набор стилей, которые можно применить к тексту для изменения его внешнего вида.
// Мы можем получить доступ к этим встроенным стилям через коллекцию «Стили» документа.
// Все эти стили будут иметь флаг «BuiltIn», установленный на «true».
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// Создайте собственный стиль и добавьте его в коллекцию.
 // Такие пользовательские стили, как этот, будут иметь флаг «BuiltIn», установленный на «false».
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### Смотрите также

* class [Style](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
