---
title: OoxmlSaveOptions.KeepLegacyControlChars
linktitle: KeepLegacyControlChars
articleTitle: KeepLegacyControlChars
second_title: Aspose.Words для .NET
description: OoxmlSaveOptions KeepLegacyControlChars свойство. Сохраняет исходное представление устаревших управляющих символов на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars/
---
## OoxmlSaveOptions.KeepLegacyControlChars property

Сохраняет исходное представление устаревших управляющих символов.

```csharp
public bool KeepLegacyControlChars { get; set; }
```

## Примеры

Показывает, как поддерживать устаревшие управляющие символы при преобразовании в формат .docx.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// Когда мы сохраняем документ в формате OOXML, мы можем создать объект OoxmlSaveOptions
// а затем передаем его методу сохранения документа, чтобы изменить способ сохранения документа.
// Установите для свойства KeepLegacyControlChars значение true, чтобы сохранить
// устаревший символ «ShortDateTime» при сохранении.
// Установите для свойства «KeepLegacyControlChars» значение «false», чтобы удалить
// устаревший символ «ShortDateTime» из выходного документа.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### Смотрите также

* class [OoxmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
