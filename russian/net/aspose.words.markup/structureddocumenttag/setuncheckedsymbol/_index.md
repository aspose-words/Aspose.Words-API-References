---
title: StructuredDocumentTag.SetUncheckedSymbol
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTag метод. Устанавливает символ используемый для обозначения неотмеченного состояния элемента управления содержимым флажка.
type: docs
weight: 390
url: /ru/net/aspose.words.markup/structureddocumenttag/setuncheckedsymbol/
---
## StructuredDocumentTag.SetUncheckedSymbol method

Устанавливает символ, используемый для обозначения неотмеченного состояния элемента управления содержимым флажка.

```csharp
public void SetUncheckedSymbol(int characterCode, string fontName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| characterCode | Int32 | Код символа для указанного символа. |
| fontName | String | Имя шрифта, содержащего символ. |

### Примечания

Доступ к этому методу будет работать только дляCheckbox Типы СДТ.

Для всех остальных типов SDT возникнет исключение.

### Примеры

Покажите, как создать структурированный тег документа в виде флажка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) {Checked = true};

// Мы можем установить символы, используемые для представления отмеченного/неотмеченного состояния элемента управления содержимым флажка.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### Смотрите также

* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../structureddocumenttag/)
* сборка [Aspose.Words](../../../)


