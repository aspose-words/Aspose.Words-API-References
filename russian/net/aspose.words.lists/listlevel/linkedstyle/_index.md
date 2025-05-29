---
title: ListLevel.LinkedStyle
linktitle: LinkedStyle
articleTitle: LinkedStyle
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ListLevel LinkedStyle, которое позволяет легко управлять стилями абзацев для списков и настраивать их, улучшая форматирование и удобочитаемость документа.
type: docs
weight: 60
url: /ru/net/aspose.words.lists/listlevel/linkedstyle/
---
## ListLevel.LinkedStyle property

Возвращает или задает стиль абзаца, связанный с этим уровнем списка.

```csharp
public Style LinkedStyle { get; set; }
```

## Примечания

Это свойство`нулевой` когда уровень списка не связан со стилем абзаца. Это свойство может быть установлено в`нулевой`.

## Примеры

Демонстрирует расширенные способы настройки меток списков.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Список позволяет нам организовывать и украшать наборы абзацев с помощью префиксных символов и отступов.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом в списке.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Метки уровня 1 будут отформатированы в соответствии со стилем абзаца «Заголовок 1» и будут иметь префикс.
// Они будут выглядеть как «Приложение А», «Приложение Б»...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Метки уровня 2 будут отображать текущие номера первого и второго уровней списка и иметь начальные нули.
// Если первый уровень списка равен 1, то метки списка будут выглядеть как «Раздел (1.01)», «Раздел (1.02)»...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Обратите внимание, что на более высоком уровне используется нумерация заглавными буквами.
// Мы можем установить свойство «IsLegal» для использования арабских цифр для более высоких уровней списка.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Метки уровня 3 будут представлять собой заглавные римские цифры с префиксом и суффиксом и будут перезапускаться для каждого элемента списка уровня 1.
// Эти метки списка будут выглядеть как "-I-", "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Сделать метки всех уровней списка жирными.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// Применить форматирование списка к текущему абзацу.
builder.ListFormat.List = list;

// Создаем элементы списка, которые будут отображать все три уровня нашего списка.
for (int n = 0; n < 2; n++)
{
    for (int i = 0; i < 3; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }
}

builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.CreateListRestartAfterHigher.docx");
```

### Смотрите также

* class [Style](../../../aspose.words/style/)
* class [ListLevel](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
