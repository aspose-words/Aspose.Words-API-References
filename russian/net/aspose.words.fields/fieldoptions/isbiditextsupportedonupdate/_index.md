---
title: FieldOptions.IsBidiTextSupportedOnUpdate
linktitle: IsBidiTextSupportedOnUpdate
articleTitle: IsBidiTextSupportedOnUpdate
second_title: Aspose.Words для .NET
description: FieldOptions IsBidiTextSupportedOnUpdate свойство. Получает или задает значение указывающее полностью ли поддерживается двунаправленный текст во время обновления поля или нет на С#.
type: docs
weight: 150
url: /ru/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

Получает или задает значение, указывающее, полностью ли поддерживается двунаправленный текст во время обновления поля или нет.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

## Примечания

Когда для этого свойства установлено значение`истинный`, выполняются дополнительные шаги для получения результата поля, совместимого с языком с написанием справа налево (т. е. арабского или иврита), во время его обновления.

Когда для этого свойства установлено значение`ЛОЖЬ` и используется язык с письмом справа налево, корректность поля result после его обновления не гарантируется.

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как использовать FieldOptions, чтобы гарантировать, что обновление полей полностью поддерживает двунаправленный текст.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Убедитесь, что любая полевая операция, включающая текст с письмом справа налево, выполняется должным образом.
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// Используйте конструктор документов, чтобы вставить поле, содержащее текст, написанный справа налево.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### Смотрите также

* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
