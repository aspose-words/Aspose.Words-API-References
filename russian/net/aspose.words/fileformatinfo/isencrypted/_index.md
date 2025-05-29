---
title: FileFormatInfo.IsEncrypted
linktitle: IsEncrypted
articleTitle: IsEncrypted
second_title: Aspose.Words для .NET
description: Узнайте, защищен ли ваш документ, с помощью свойства FileFormatInfo IsEncrypted — возвращает значение true для зашифрованных файлов, для доступа к которым требуется пароль.
type: docs
weight: 40
url: /ru/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

Возврат`истинный` если документ зашифрован и для его открытия требуется пароль.

```csharp
public bool IsEncrypted { get; }
```

## Примечания

Это свойство существует, чтобы помочь вам отсортировать зашифрованные документы от незашифрованных. Если вы попытаетесь загрузить зашифрованный документ с помощью Aspose.Words без предоставления пароля, будет выдано исключение . Вы можете использовать это свойство, чтобы определить, требуется ли документу пароль , и предпринять некоторые действия перед загрузкой документа, например, запросить у пользователя пароль.

## Примеры

Показывает, как использовать класс FileFormatUtil для определения формата документа и шифрования.

```csharp
Document doc = new Document();

// Настройте объект SaveOptions для шифрования документа
// с паролем при сохранении, а затем сохраняем документ.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Проверяем тип файла нашего документа и статус его шифрования.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

### Смотрите также

* class [FileFormatInfo](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
