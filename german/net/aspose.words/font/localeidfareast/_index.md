---
title: Font.LocaleIdFarEast
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Ruft die Gebietsschemakennung Sprache der formatierten asiatischen Zeichen ab oder legt sie fest.
type: docs
weight: 220
url: /de/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

Ruft die Gebietsschemakennung (Sprache) der formatierten asiatischen Zeichen ab oder legt sie fest.

```csharp
public int LocaleIdFarEast { get; set; }
```

### Bemerkungen

Die Liste der Gebietsschema-IDs finden Sie unter https://msdn.microsoft.com/en-us/library/cc233965.aspx

### Beispiele

Zeigt, wie Text in einer fernöstlichen Sprache eingefügt und formatiert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie Schriftarteinstellungen an, die der Document Builder auf jeden Text anwendet, den er einfügt.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Benennen Sie "FarEast"-Äquivalente für unsere Schriftart und unser Gebietsschema.
// Wenn der Builder asiatische Zeichen mit dieser Font-Konfiguration einfügt, wird jeder Lauf, der enthält
// Diese Zeichen zeigen sie mit der Schriftart/dem Gebietsschema "FarEast" anstelle der Standardeinstellung an.
// Dies könnte nützlich sein, wenn eine westliche Schriftart keine ideale Darstellung für asiatische Zeichen hat.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Dieser Text wird in der Standardschrift/dem Standardgebietsschema angezeigt.
builder.Writeln("Hello world!");

// Da es sich um asiatische Zeichen handelt, wendet dieser Lauf unsere "FarEast"-Font/Gebietsschema-Äquivalente an.
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


