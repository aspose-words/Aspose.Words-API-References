---
title: Document.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: Aspose.Words для .NET
description: Узнайте, содержит ли ваш документ макросы проекта VBA с помощью свойства HasMacros. Повысьте автоматизацию и эффективность ваших рабочих процессов сегодня!
type: docs
weight: 200
url: /ru/net/aspose.words/document/hasmacros/
---
## Document.HasMacros property

Возврат`истинный` если документ имеет проект VBA (макросы).

```csharp
public bool HasMacros { get; }
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

* method [RemoveMacros](../removemacros/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
