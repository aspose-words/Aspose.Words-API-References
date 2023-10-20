---
title: Font.NameFarEast
linktitle: NameFarEast
articleTitle: NameFarEast
second_title: Aspose.Words für .NET
description: Font NameFarEast eigendom. Gibt einen ostasiatischen Schriftartnamen zurück oder legt diesen fest in C#.
type: docs
weight: 260
url: /de/net/aspose.words/font/namefareast/
---
## Font.NameFarEast property

Gibt einen ostasiatischen Schriftartnamen zurück oder legt diesen fest.

```csharp
public string NameFarEast { get; set; }
```

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

* property [Name](../name/)
* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
