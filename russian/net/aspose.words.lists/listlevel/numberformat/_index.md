---
title: NumberFormat
second_title: Справочник по API Aspose.Words для .NET
description: Возвращает или задает числовой формат для уровня списка.
type: docs
weight: 70
url: /ru/net/aspose.words.lists/listlevel/numberformat/
---
## ListLevel.NumberFormat property

Возвращает или задает числовой формат для уровня списка.

```csharp
public string NumberFormat { get; set; }
```

### Примечания

Среди обычных текстовых символов строка может содержать символы-заполнители от \x0000 до \x0008 представляет числа из соответствующих уровней списка.

Например, строка "\x0000.\x0001)" создаст метку списка , которая выглядит примерно как "1.5)". Цифра "1" - текущий номер из 1-го уровня списка, цифра "5" - текущий номер из 2-го уровня списка.

Null не допускается, но пустая строка означает, что число недействительно.

### Примеры

Показывает, как применять форматирование пользовательского списка к абзацам при использовании DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Список позволяет нам организовывать и оформлять наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа. 
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов. 
 // Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Метки уровня 1 будут отформатированы в соответствии со стилем абзаца «Заголовок 1» и будут иметь префикс.
 // Они будут выглядеть как "Приложение A", "Приложение B"...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

 // Метки уровня 2 будут отображать текущие числа первого и второго уровней списка и иметь начальные нули.
 // Если первый уровень списка находится на уровне 1, то метки списка из них будут выглядеть как "Раздел (1.01)", "Раздел (1.02)"...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

 // Обратите внимание, что более высокий уровень использует нумерацию UppercaseLetter.
 // Мы можем установить свойство "IsLegal", чтобы использовать арабские цифры для более высоких уровней списка.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

 // Метки уровня 3 будут представлять собой римские цифры в верхнем регистре с префиксом и суффиксом и будут перезапускаться для каждого элемента списка уровня 1.
 // Метки этих списков будут выглядеть как "-I-", "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

 // Сделать метки всех уровней списка полужирными.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

 // Применяем форматирование списка к текущему абзацу.
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

Показывает усовершенствованные способы настройки меток списков.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Список позволяет нам организовывать и оформлять наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа. 
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов. 
 // Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Метки уровня 1 будут отформатированы в соответствии со стилем абзаца «Заголовок 1» и будут иметь префикс.
 // Они будут выглядеть как "Приложение A", "Приложение B"...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

 // Метки уровня 2 будут отображать текущие числа первого и второго уровней списка и иметь начальные нули.
 // Если первый уровень списка находится на уровне 1, то метки списка из них будут выглядеть как "Раздел (1.01)", "Раздел (1.02)"...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

 // Обратите внимание, что более высокий уровень использует нумерацию UppercaseLetter.
 // Мы можем установить свойство "IsLegal", чтобы использовать арабские цифры для более высоких уровней списка.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

 // Метки уровня 3 будут представлять собой римские цифры в верхнем регистре с префиксом и суффиксом и будут перезапускаться для каждого элемента списка уровня 1.
 // Метки этих списков будут выглядеть как "-I-", "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

 // Сделать метки всех уровней списка полужирными.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

 // Применяем форматирование списка к текущему абзацу.
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

* class [ListLevel](../../listlevel)
* namespace [Aspose.Words.Lists](../../listlevel)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
