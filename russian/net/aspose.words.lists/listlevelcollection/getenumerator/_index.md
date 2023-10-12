---
title: ListLevelCollection.GetEnumerator
second_title: Справочник по API Aspose.Words для .NET
description: ListLevelCollection метод. Получает объект перечислителя который будет перечислять уровни в этом списке.
type: docs
weight: 30
url: /ru/net/aspose.words.lists/listlevelcollection/getenumerator/
---
## ListLevelCollection.GetEnumerator method

Получает объект перечислителя, который будет перечислять уровни в этом списке.

```csharp
public IEnumerator<ListLevel> GetEnumerator()
```

### Примеры

Показывает усовершенствованные способы настройки меток списков.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Список позволяет нам организовывать и украшать наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство ListFormat конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Метки уровня 1 будут отформатированы в соответствии со стилем абзаца «Заголовок 1» и будут иметь префикс.
// Они будут выглядеть как «Приложение A», «Приложение B»...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Метки уровня 2 будут отображать текущие номера первого и второго уровней списка и иметь ведущие нули.
// Если первый уровень списка равен 1, то метки списков из них будут выглядеть как «Раздел (1.01)», «Раздел (1.02)»...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Обратите внимание, что на более высоком уровне используется нумерация UppercaseLetter.
// Мы можем установить свойство IsLegal для использования арабских цифр для более высоких уровней списка.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Метки уровня 3 будут представлять собой римские цифры в верхнем регистре с префиксом и суффиксом и будут перезапускаться для каждого элемента списка уровня 1.
// Эти метки списка будут выглядеть как "-I-", "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Сделайте метки всех уровней списка жирными.
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

* class [ListLevel](../../listlevel/)
* class [ListLevelCollection](../)
* пространство имен [Aspose.Words.Lists](../../listlevelcollection/)
* сборка [Aspose.Words](../../../)


