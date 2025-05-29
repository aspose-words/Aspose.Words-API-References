---
title: PclSaveOptions.AddPrinterFont
linktitle: AddPrinterFont
articleTitle: AddPrinterFont
second_title: Aspose.Words для .NET
description: Откройте для себя метод PclSaveOptions AddPrinterFont для эффективной загрузки и управления шрифтами принтеров от производителей для повышения производительности печати.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions.AddPrinterFont method

Добавляет информацию о шрифте, загруженном в принтер производителем.

```csharp
public void AddPrinterFont(string fontFullName, string fontPclName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontFullName | String | Полное название шрифта (например, «Times New Roman Bold Italic»). |
| fontPclName | String | Название шрифта, используемого в документе Pcl. |

## Примечания

Согласно спецификации Pcl, в любой принтер должно быть встроено 52 шрифта. Однако производители могут добавлять в свои устройства и другие шрифты.

## Примеры

Показывает, как заставить принтер заменить все экземпляры определенного шрифта другим шрифтом.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// При печати этого документа принтер будет использовать шрифт «Courier New»
// для доступа к местам, где в нашем документе использовался шрифт «Courier».
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### Смотрите также

* class [PclSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
