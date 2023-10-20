---
title: Font.LocaleIdFarEast
linktitle: LocaleIdFarEast
articleTitle: LocaleIdFarEast
second_title: Aspose.Words für .NET
description: Font LocaleIdFarEast eigendom. Ruft die Gebietsschemakennung Sprache der formatierten asiatischen Zeichen ab oder legt diese fest in C#.
type: docs
weight: 220
url: /de/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

Ruft die Gebietsschemakennung (Sprache) der formatierten asiatischen Zeichen ab oder legt diese fest.

```csharp
public int LocaleIdFarEast { get; set; }
```

## Bemerkungen

Die Liste der Gebietsschema-IDs finden Sie unter https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Beispiele

Zeigt, wie man Text in einer fernöstlichen Sprache einfügt und formatiert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie Schriftarteinstellungen an, die der Dokumentersteller auf jeden eingefügten Text anwendet.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Benennen Sie „FarEast“-Äquivalente für unsere Schriftart und unser Gebietsschema.
// Wenn der Builder mit dieser Schriftartkonfiguration asiatische Zeichen einfügt, wird jeder Lauf ausgeführt, der Folgendes enthält
// Diese Zeichen werden mit der Schriftart/Gebietsschema „FarEast“ anstelle der Standardeinstellung angezeigt.
// Dies könnte nützlich sein, wenn eine westliche Schriftart keine ideale Darstellung für asiatische Zeichen bietet.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Dieser Text wird in der Standardschriftart/-umgebung angezeigt.
builder.Writeln("Hello world!");

// Da es sich um asiatische Zeichen handelt, werden bei diesem Lauf unsere „FarEast“-Schriftart/Gebietsschema-Äquivalente angewendet.
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
