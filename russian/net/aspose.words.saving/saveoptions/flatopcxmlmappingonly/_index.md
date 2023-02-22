---
title: SaveOptions.FlatOpcXmlMappingOnly
second_title: Справочник по API Aspose.Words для .NET
description: SaveOptions свойство. Получает или задает значение определяющее какие форматы документов разрешено отображатьXmlMapping . Только по умолчаниюFlatOpc формат документа разрешен для сопоставления.
type: docs
weight: 90
url: /ru/net/aspose.words.saving/saveoptions/flatopcxmlmappingonly/
---
## SaveOptions.FlatOpcXmlMappingOnly property

Получает или задает значение, определяющее, какие форматы документов разрешено отображать[`XmlMapping`](../../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Только по умолчаниюFlatOpc формат документа разрешен для сопоставления.

```csharp
public bool FlatOpcXmlMappingOnly { get; set; }
```

### Примечания

Эта опция сочетается с[`FlatOpcXmlMappingOnly`](../../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) . Обычно вам нужно установить для них обоих значение false, чтобы разрешить сопоставление произвольного формата документа.

### Примеры

Показывает, как привязать теги структурированного документа к любому формату.

```csharp
// Если true - SDT будет содержать необработанный текст HTML.
// Если false - сопоставленный HTML будет проанализирован, и результирующий документ будет вставлен в содержимое SDT.
LoadOptions loadOptions = new LoadOptions { FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly };
Document doc = new Document(MyDir + "Structured document tag with HTML content.docx", loadOptions);

SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);
saveOptions.FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly;

doc.Save(ArtifactsDir + "LoadOptions.FlatOpcXmlMappingOnly.pdf", saveOptions);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../saveoptions/)
* сборка [Aspose.Words](../../../)


