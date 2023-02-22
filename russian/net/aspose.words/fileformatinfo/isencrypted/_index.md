---
title: FileFormatInfo.IsEncrypted
second_title: Справочник по API Aspose.Words для .NET
description: FileFormatInfo свойство. Возвращает значение true если документ зашифрован и для его открытия требуется пароль.
type: docs
weight: 30
url: /ru/net/aspose.words/fileformatinfo/isencrypted/
---
## FileFormatInfo.IsEncrypted property

Возвращает значение true, если документ зашифрован и для его открытия требуется пароль.

```csharp
public bool IsEncrypted { get; }
```

### Примечания

Это свойство помогает сортировать зашифрованные документы от незашифрованных. Если вы попытаетесь загрузить зашифрованный документ с помощью Aspose.Words без указания пароля, будет выдано исключение . Вы можете использовать это свойство, чтобы определить, требует ли документ пароль , и выполнить какое-либо действие перед загрузкой документа, например запросить у пользователя пароль.

### Примеры

Показывает, как использовать класс FileFormatUtil для определения формата и шифрования документа.

```csharp
Document doc = new Document();

// Настроить объект SaveOptions для шифрования документа
// с паролем, когда мы его сохраняем, а затем сохраняем документ.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Проверяем тип файла нашего документа и его статус шифрования.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

### Смотрите также

* class [FileFormatInfo](../)
* пространство имен [Aspose.Words](../../fileformatinfo/)
* сборка [Aspose.Words](../../../)


