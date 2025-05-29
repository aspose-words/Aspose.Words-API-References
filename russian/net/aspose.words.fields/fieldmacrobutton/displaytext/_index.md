---
title: FieldMacroButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words для .NET
description: Узнайте, как настроить свойство FieldMacroButton DisplayText для улучшенного выполнения макроса. Установите идеальный текст кнопки для бесшовных пользовательских команд!
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldmacrobutton/displaytext/
---
## FieldMacroButton.DisplayText property

Возвращает или задает текст, который будет отображаться в качестве «кнопки», выбранной для запуска макроса или команды.

```csharp
public string DisplayText { get; set; }
```

## Примеры

Показывает, как использовать поля MACROBUTTON, чтобы иметь возможность запускать макросы документа одним щелчком мыши.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// Вставьте поле MACROBUTTON и укажите один из макросов документа по имени в свойстве MacroName.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// Используйте свойство для ссылки на «ViewZoom200», макрос, поставляемый с Microsoft Word.
// Все остальные макросы можно найти через Вид -> Макросы (раскрывающийся список) -> Просмотреть макросы.
// В этом меню выберите «Команды Word» из раскрывающегося списка «Макросы в:».
// Если наш документ содержит пользовательский макрос с тем же именем, что и у стандартного макроса,
// наш макрос будет тем, который запустит поле MACROBUTTON.
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.GetFieldCode());

// Сохраните документ как тип документа с поддержкой макросов.
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### Смотрите также

* class [FieldMacroButton](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
