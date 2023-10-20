---
title: FileFormatInfo.IsEncrypted
linktitle: IsEncrypted
articleTitle: IsEncrypted
second_title: Aspose.Words для .NET
description: FileFormatInfo IsEncrypted свойство. Возвращаетистинный если документ зашифрован и для открытия требуется пароль на С#.
type: docs
weight: 30
url: /ru/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

Возвращает`истинный` если документ зашифрован и для открытия требуется пароль.

```csharp
public bool IsEncrypted { get; }
```

## Примечания

Это свойство существует, чтобы помочь вам сортировать зашифрованные документы от незашифрованных. Если вы попытаетесь загрузить зашифрованный документ с помощью Aspose.Words без указания пароля, будет выдано исключение . Вы можете использовать это свойство, чтобы определить, требует ли документ пароля , и выполнить какое-либо действие перед загрузкой документа, например, запросить у пользователя пароль.

## Примеры

Показывает, как использовать класс FileFormatUtil для определения формата и шифрования документа.

```csharp
Document doc = new Document();

// Настраиваем объект SaveOptions для шифрования документа
// с паролем, когда мы его сохраняем, а затем сохраняем документ.
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
