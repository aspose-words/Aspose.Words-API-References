---
title: StructuredDocumentTag.StructuredDocumentTag
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTag строитель. Инициализирует новый экземпляр Тег структурированного документа класс.
type: docs
weight: 10
url: /ru/net/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag constructor

Инициализирует новый экземпляр **Тег структурированного документа** класс.

```csharp
public StructuredDocumentTag(DocumentBase doc, SdtType type, MarkupLevel level)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |
| type | SdtType | Тип узла SDT. |
| level | MarkupLevel | Уровень узла SDT в документе. |

### Примечания

Могут быть созданы следующие типы SDT:

* Checkbox
* DropDownList
* ComboBox
* Date
* BuildingBlockGallery
* Group
* Picture
* RichText
* PlainText

### Примеры

Покажите, как создать тег структурированного документа в виде флажка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) {Checked = true};

// Мы можем установить символы, используемые для представления отмеченного/не отмеченного состояния элемента управления содержимым флажка.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### Смотрите также

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [SdtType](../../sdttype/)
* enum [MarkupLevel](../../markuplevel/)
* class [StructuredDocumentTag](../)
* пространство имен [Aspose.Words.Markup](../../structureddocumenttag/)
* сборка [Aspose.Words](../../../)


