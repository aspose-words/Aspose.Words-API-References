---
title: FieldAutoNumLgl.SeparatorCharacter
second_title: Справочник по API Aspose.Words для .NET
description: FieldAutoNumLgl свойство. Получает или задает используемый символразделитель.
type: docs
weight: 30
url: /ru/net/aspose.words.fields/fieldautonumlgl/separatorcharacter/
---
## FieldAutoNumLgl.SeparatorCharacter property

Получает или задает используемый символ-разделитель.

```csharp
public string SeparatorCharacter { get; set; }
```

### Примеры

Показывает, как организовать документ с помощью полей AUTONUMLGL.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // В полях AUTONUMLGL отображается число, которое увеличивается в каждом поле AUTONUMLGL в пределах его текущего уровня заголовка.
    // Эти поля ведут отдельный счет для каждого уровня заголовка,
     // и каждое поле также отображает количество полей AUTONUMLGL для всех уровней заголовков ниже его собственного.
    // Изменение счетчика для любого уровня заголовка сбрасывает счетчики для всех уровней выше этого уровня до 1.
    // Это позволяет нам организовать наш документ в виде списка структуры.
    // Это первое поле AUTONUMLGL на уровне заголовка 1, отображающее «1». в документе.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // Это второе поле AUTONUMLGL на уровне заголовка 1, поэтому оно будет отображать «2.».
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // Это первое поле AUTONUMLGL на уровне заголовка 2,
    // и счетчик AUTONUMLGL для уровня заголовка ниже него равен "2", поэтому он будет отображать "2.1.".
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // Это первое поле AUTONUMLGL с уровнем заголовка 3.
    // Работая так же, как поле выше, оно будет отображать «2.1.1.».
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // Это поле находится на уровне заголовка 2, и его соответствующий счетчик AUTONUMLGL равен 2, поэтому в поле будет отображаться «2.2.».
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // Увеличение счетчика AUTONUMLGL для уровня заголовка ниже этого
    // сбросил счётчик для этого уровня, так что в этом поле будет отображаться «2.2.1.».
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal))
    {
        // Символ-разделитель, который появляется в поле результата сразу после числа,
        // по умолчанию является точкой. Если мы оставим это свойство нулевым,
        // наше последнее поле AUTONUMLGL будет отображать «2.2.1». в документе.
        Assert.IsNull(field.SeparatorCharacter);

        // Установка пользовательского символа-разделителя и удаление завершающей точки
        // изменит внешний вид этого поля с «2.2.1». до "2:2:1".
        // Мы применим это ко всем полям, которые мы создали.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");

/// <summary>
/// Использует конструктор документов для вставки предложения, пронумерованного полем AUTONUMLGL.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // Этот текст будет принадлежать правовому полю auto num над ним.
    // Он свернется, когда мы щелкнем стрелку рядом с соответствующим полем AUTONUMLGL в Microsoft Word.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### Смотрите также

* class [FieldAutoNumLgl](../)
* пространство имен [Aspose.Words.Fields](../../fieldautonumlgl/)
* сборка [Aspose.Words](../../../)


