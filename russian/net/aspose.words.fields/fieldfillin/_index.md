---
title: FieldFillIn
second_title: Справочник по API Aspose.Words для .NET
description: Реализует поле FILLIN.
type: docs
weight: 1740
url: /ru/net/aspose.words.fields/fieldfillin/
---
## FieldFillIn class

Реализует поле FILLIN.

```csharp
public class FieldFillIn : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldFillIn](fieldfillin)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DefaultResponse](../../aspose.words.fields/fieldfillin/defaultresponse) { get; set; } | Получает или задает ответ пользователя по умолчанию (начальное значение содержится в окне подсказки). |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format) { get; } | Получает[`FieldFormat`](../fieldformat) объект, предоставляющий типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Получает или задает LCID поля. |
| [PromptOnceOnMailMerge](../../aspose.words.fields/fieldfillin/promptonceonmailmerge) { get; set; } | Получает или задает, должен ли ответ пользователя быть получен один раз за операцию слияния. |
| [PromptText](../../aspose.words.fields/fieldfillin/prompttext) { get; set; } | Получает или задает текст подсказки (заголовок окна подсказки). |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Получает или задает текст, который находится между разделителем поля и концом поля. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
| [Start](../../aspose.words.fields/field/start) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает **нулевой** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Выполняет развязку поля. |
| [Update](../../aspose.words.fields/field/update)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примечания

Предлагает пользователю ввести текст.

### Примеры

Показывает, как использовать поле FILLIN для запроса ответа у пользователя.

```csharp
public void FieldFillIn()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Вставить поле FILLIN. Когда мы вручную обновляем это поле в Microsoft Word,
    // это предложит нам ввести ответ. После этого поле отобразит ответ в виде текста.
    FieldFillIn field = (FieldFillIn)builder.InsertField(FieldType.FieldFillIn, true);
    field.PromptText = "Please enter a response:";
    field.DefaultResponse = "A default response.";

    // Мы также можем использовать эти поля, чтобы запросить у пользователя уникальный ответ для каждой страницы
    // создано во время слияния почты, выполненного с помощью Microsoft Word.
    field.PromptOnceOnMailMerge = true;

    Assert.AreEqual(" FILLIN  \"Please enter a response:\" \\d \"A default response.\" \\o", field.GetFieldCode());

    FieldMergeField mergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
    mergeField.FieldName = "MergeField";

    // Если мы выполняем слияние программно, мы можем использовать настраиваемый ответчик приглашения
    // для автоматического редактирования ответов для полей FILLIN, которые встречаются при слиянии.
    doc.FieldOptions.UserPromptRespondent = new PromptRespondent();
    doc.MailMerge.Execute(new [] { "MergeField" }, new object[] { "" });

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.FILLIN.docx");

/// <summary>
/// Добавляет строку к ответу по умолчанию для каждого поля FILLIN во время слияния.
/// </summary>
private class PromptRespondent : IFieldUserPromptRespondent
{
    public string Respond(string promptText, string defaultResponse)
    {
        return "Response modified by PromptRespondent. " + defaultResponse;
    }
}
```

### Смотрите также

* class [Field](../field)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
