---
title: FieldOptions.IsBidiTextSupportedOnUpdate
second_title: Справочник по API Aspose.Words для .NET
description: FieldOptions свойство. Получает или задает значение указывающее полностью ли поддерживается двунаправленный текст во время обновления поля.
type: docs
weight: 130
url: /ru/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

Получает или задает значение, указывающее, полностью ли поддерживается двунаправленный текст во время обновления поля.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

### Примечания

Когда это свойство установлено в **истинный**, выполняются дополнительные шаги для создания результата поля, совместимого с письмом справа налево language (т. е. арабского или иврита), во время его обновления.

Когда это свойство установлено в **ЛОЖЬ** и используется язык справа налево, корректность поля result после его обновления не гарантируется.

Значение по умолчанию **ЛОЖЬ**.

### Примеры

Показывает, как использовать FieldOptions, чтобы убедиться, что обновление поля полностью поддерживает двунаправленный текст.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Убедитесь, что любая операция с полем, включающая текст с написанием справа налево, выполняется должным образом. 
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// Используйте конструктор документов, чтобы вставить поле, содержащее текст с направлением справа налево.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### Смотрите также

* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../fieldoptions/)
* сборка [Aspose.Words](../../../)


