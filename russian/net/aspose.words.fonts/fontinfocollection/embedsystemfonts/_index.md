---
title: FontInfoCollection.EmbedSystemFonts
linktitle: EmbedSystemFonts
articleTitle: EmbedSystemFonts
second_title: Aspose.Words для .NET
description: Узнайте, как свойство FontInfoCollection EmbedSystemFonts улучшает ваши документы путем внедрения системных шрифтов. Узнайте его значение по умолчанию и преимущества!
type: docs
weight: 20
url: /ru/net/aspose.words.fonts/fontinfocollection/embedsystemfonts/
---
## FontInfoCollection.EmbedSystemFonts property

Указывает, следует ли встраивать системные шрифты в документ. Значение по умолчанию для этого свойства:`ЛОЖЬ`.

Эта опция работает только тогда, когда[`EmbedTrueTypeFonts`](../embedtruetypefonts/) опция установлена на`истинный`.

```csharp
public bool EmbedSystemFonts { get; set; }
```

## Примечания

Установка этого свойства в`истинный` полезно, если пользователь находится в восточноазиатской системе и хочет создать документ, который будет доступен для чтения другим пользователям, у которых нет шрифтов для этого языка в их системе. Например, пользователь японской системы может выбрать встраивание шрифтов в документ, чтобы японский документ можно было прочитать во всех системах.

Эта опция работает только для форматов DOC, DOCX и RTF.

## Примеры

Показывает, как сохранить документ со встроенными шрифтами TrueType.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");
```

### Смотрите также

* class [FontInfoCollection](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
