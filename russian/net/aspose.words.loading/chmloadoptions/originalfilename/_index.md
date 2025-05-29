---
title: ChmLoadOptions.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ChmLoadOptions OriginalFileName, легко задайте имя файла CHM для упрощенного доступа. Значение по умолчанию — null. Оптимизируйте свой опыт!
type: docs
weight: 20
url: /ru/net/aspose.words.loading/chmloadoptions/originalfilename/
---
## ChmLoadOptions.OriginalFileName property

Имя файла CHM. Значение по умолчанию:`нулевой` .

```csharp
public string OriginalFileName { get; set; }
```

## Примечания

Документы CHM могут содержать ссылки, ссылающиеся на тот же документ по имени файла. Aspose.Words поддерживает такие ссылки и обычно использует[`OriginalFileName`](../../../aspose.words/document/originalfilename/) для проверки, является ли файл, на который ссылается link , загружаемым файлом. Если документ загружается из потока, его исходное имя файла должно быть указано явно через это свойство, поскольку оно не может быть определено автоматически.

Если документ CHM загружен из файла и указано ненулевое значение для этого свойства, то значение будет иметь приоритет над фактическим именем файла, сохраненного в[`OriginalFileName`](../../../aspose.words/document/originalfilename/) .

## Примеры

Показывает, как разрешать URL-адреса вида «ms-its:myfile.chm::/index.htm».

```csharp
// Наш документ содержит URL-адреса типа "ms-its:amhelp.chm::....htm", но у него другое имя,
// поэтому ссылки на файлы не работают после сохранения в HTML.
// Чтобы избежать такого поведения, нам нужно определить исходное имя файла в «ChmLoadOptions».
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### Смотрите также

* class [ChmLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
