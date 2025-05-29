---
title: ChmLoadOptions
linktitle: ChmLoadOptions
articleTitle: ChmLoadOptions
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор ChmLoadOptions для бесшовной инициализации. Задайте значения по умолчанию без усилий и улучшите производительность вашего приложения уже сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions constructor

Инициализирует новый экземпляр этого класса со значениями по умолчанию.

```csharp
public ChmLoadOptions()
```

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
