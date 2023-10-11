---
title: StructuredDocumentTag.Checked
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTag свойство. Получает/устанавливает текущее состояние флажка. СДТ . Значение по умолчанию для этого свойстваЛОЖЬ .
type: docs
weight: 60
url: /ru/net/aspose.words.markup/structureddocumenttag/checked/
---
## StructuredDocumentTag.Checked property

Получает/устанавливает текущее состояние флажка. **СДТ** . Значение по умолчанию для этого свойства:`ЛОЖЬ` .

```csharp
public bool Checked { get; set; }
```

### Примечания

Доступ к этому ресурсу будет работать только дляCheckbox Типы SDT.

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


