---
title: FieldAutoNumLgl.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words для .NET
description: Узнайте, как настроить свойство FieldAutoNumLgl SeparatorCharacter, чтобы улучшить форматирование данных с помощью гибкого символа-разделителя.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldautonumlgl/separatorcharacter/
---
## FieldAutoNumLgl.SeparatorCharacter property

Возвращает или задает символ разделителя, который будет использоваться.

```csharp
public string SeparatorCharacter { get; set; }
```

## Примеры

Показывает, как организовать документ с использованием полей AUTONUMLGL.

```csharp
public void FieldAutoNumLgl()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // Поля AUTONUMLGL отображают число, которое увеличивается в каждом поле AUTONUMLGL в пределах текущего уровня заголовка.
    // Эти поля ведут отдельный подсчет для каждого уровня заголовка,
     // и каждое поле также отображает количество полей AUTONUMLGL для всех уровней заголовков ниже своего собственного.
    // Изменение количества для любого уровня заголовка сбрасывает количество для всех уровней выше этого уровня до 1.
    // Это позволяет нам организовать наш документ в виде структурного списка.
    // Это первое поле AUTONUMLGL на уровне заголовка 1, отображающее «1.» в документе.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // Это второе поле AUTONUMLGL на уровне заголовка 1, поэтому оно будет отображать «2.».
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // Это первое поле AUTONUMLGL на уровне заголовка 2,
    // а счетчик AUTONUMLGL для уровня заголовка ниже равен «2», поэтому будет отображаться «2.1.».
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // Это первое поле AUTONUMLGL на уровне заголовка 3.
    // Работает так же, как и поле выше, будет отображать «2.1.1.».
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // Это поле находится на уровне заголовка 2, и его соответствующее значение AUTONUMLGL равно 2, поэтому в поле будет отображаться «2.2.».
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // Увеличиваем счетчик AUTONUMLGL для уровня заголовка ниже этого
    // сбросил счетчик для этого уровня, так что в этом поле будет отображаться «2.2.1.».
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal).ToList())
    {
        // Символ-разделитель, который появляется в поле результата сразу после числа,
        // по умолчанию это точка. Если мы оставим это свойство пустым,
        // наше последнее поле AUTONUMLGL отобразит в документе «2.2.1.».
        Assert.IsNull(field.SeparatorCharacter);

        // Установка пользовательского символа-разделителя и удаление конечной точки
        // изменит внешний вид этого поля с "2.2.1." на "2:2:1".
        // Мы применим это ко всем полям, которые мы создали.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");
}

/// <summary>
/// Использует конструктор документов для вставки предложения, пронумерованного полем AUTONUMLGL.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // Этот текст будет относиться к полю auto num, расположенному выше.
    // Он свернется, если щелкнуть стрелку рядом с соответствующим полем AUTONUMLGL в Microsoft Word.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### Смотрите также

* class [FieldAutoNumLgl](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
