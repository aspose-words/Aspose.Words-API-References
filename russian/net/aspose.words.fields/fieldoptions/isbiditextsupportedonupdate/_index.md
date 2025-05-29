---
title: FieldOptions.IsBidiTextSupportedOnUpdate
linktitle: IsBidiTextSupportedOnUpdate
articleTitle: IsBidiTextSupportedOnUpdate
second_title: Aspose.Words для .NET
description: Узнайте, включена ли поддержка двунаправленного текста в FieldOptions. Легко управляйте обновлениями текста для улучшенной многоязычной функциональности.
type: docs
weight: 150
url: /ru/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

Возвращает или задает значение, указывающее, полностью ли поддерживается двунаправленный текст во время обновления поля.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

## Примечания

Когда это свойство установлено в`истинный`, выполняются дополнительные шаги для получения результата поля language , совместимого с написанием справа налево (т. е. арабским или ивритом), во время его обновления.

Когда это свойство установлено в`ЛОЖЬ` и используется язык с написанием справа налево, корректность поля result после его обновления не гарантируется.

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как использовать FieldOptions, чтобы гарантировать полную поддержку двунаправленного текста при обновлении полей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Убедитесь, что любая операция с полем, включающая текст с направлением справа налево, выполняется так, как ожидается.
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// Используйте конструктор документов для вставки поля, содержащего текст с написанием справа налево.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### Смотрите также

* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
